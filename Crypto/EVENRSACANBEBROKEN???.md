Link thử thách: https://play.picoctf.org/practice/challenge/470?category=2&page=1
<img width="694" height="475" alt="image" src="https://github.com/user-attachments/assets/dafdb15f-47b6-413a-b506-d2e4441effc5" />

Dùng netcat kết nói tới đường link trên máy ảo ta nhận dữ liệu:
N = 24639889678093942666654710819185887860738504258701587340817006401175715704382430093504966854410348818655328625000997278105969760386971372384895385144061018
e = 65537
ciphertext = 13341950591187920968898200295150855201570169442807636456044959704998404995434936945942885773828868016494684305862144048916368831890942573800306878779189569

Tiến hành tải file của đề ta được 1 file có tên là encrypt.py mở file lên và bắt đầu phân tích kết hợp với dữ kiện mà ta đã có khi kết nối> Ta cùng phân tích code:

from sys import exit
from Crypto.Util.number import bytes_to_long, inverse
from setup import get_primes

e = 65537

def gen_key(k):                        // Tạo khóa. Hàm lấy hai số nguyên tố lớp p và q từ một module bên ngoài
    """
    Generates RSA key with k bits
    """
    p,q = get_primes(k//2)
    N = p*q
    d = inverse(e, (p-1)*(q-1))

    return ((N,e), d)

def encrypt(pubkey, m):
    N,e = pubkey
    return pow(bytes_to_long(m.encode('utf-8')), e, N)

def main(flag):
    pubkey, _privkey = gen_key(1024)
    encrypted = encrypt(pubkey, flag) 
    return (pubkey[0], encrypted)

if __name__ == "__main__":
    flag = open('flag.txt', 'r').read()
    flag = flag.strip()
    N, cypher  = main(flag)
    print("N:", N)
    print("e:", e)
    print("cyphertext:", cypher)
    exit()

-  Viết scrypt giải:
  Tạo 1 file code python trên máy ảo nano en.py
# Dữ liệu từ đề bài của bạn
N = 24639889678093942666654710819185887860738504258701587340817006401175715704382430093504966854410348818655328625000997278105969760386971372384895385144061018
e = 65537
ciphertext = 13341950591187920968898200295150855201570169442807636456044959704998404995434936945942885773828868016494684305862144048916368831890942573800306878779189569

# Thừa số bạn đã tìm được
p = 12319944839046971333327355409592943930369252129350793670408503200587857852191215046752483427205174409327664312500498639052984880193485686192447692572030509
q = 2

# Hàm tính Nghịch đảo nhân Modulo (Thay thế cho Crypto.Util.number.inverse)
def extended_gcd(a, b):
    if a == 0:
        return b, 0, 1
    d, x1, y1 = extended_gcd(b % a, a)
    x = y1 - (b // a) * x1
    y = x1
    return d, x, y

def mod_inverse(a, m):
    d, x, y = extended_gcd(a, m)
    if d != 1:
        raise Exception('Nghịch đảo modulo không tồn tại')
    return x % m

# Hàm chuyển số thành chữ (Thay thế cho long_to_bytes)
def n_to_bytes(n):
    return n.to_bytes((n.bit_length() + 7) // 8, 'big')

# QUY TRÌNH GIẢI MÃ
phi = (p - 1) * (q - 1)
d = mod_inverse(e, phi)
m = pow(ciphertext, d, N)

print("-" * 30)
try:
    print("Flag giải được:", n_to_bytes(m).decode())
except:
    print("Kết quả (dạng bytes):", n_to_bytes(m))
print("-" * 30)

