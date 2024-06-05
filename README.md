![image](https://github.com/produman66/kysspython/assets/115027939/6220d22e-e7bc-4182-b53b-56990596ae57)# kysspython

# 5 Задача

![image](https://github.com/produman66/kysspython/assets/115027939/6288ecea-135b-4a93-84f8-fd4ef8abf1f8)

```python
def main(x):
    total = 0
    for i in range(len(x)):
        cur = x[i]
        total += (int(cur**3 + 32 + 74 * cur**2)) ** 6
    return total
```

```python
def main(x):
  total = 0
  for i in range(1, len(x)+1):
    cur = x[len(x) - i]
    total += (1 - cur ** 3 - 16 * (cur ** 2))
  return total
```
# 6 Задача
![image](https://github.com/produman66/kysspython/assets/115027939/ed32ac4f-5312-4d09-9289-d6cd360c3473)

![image](https://github.com/produman66/kysspython/assets/115027939/fb0778dd-8072-4811-b3f4-e304113fa467)

```python
import math


def main(H):
    Z = {8*h - h**3 for h in H if -57 < h < 90}
    d = {h for h in H if (h < 50) != (h > -48)}
    psi = {math.ceil(z/3)+abs(z) for z in Z}
    a = len(d)
    b = sum(delta * p for delta in d for p in psi)
    return a + b
```

# 7 Задача
![image](https://github.com/produman66/kysspython/assets/115027939/02f6186d-2197-4093-89af-3e87aa54faf4)

```python
def x1(x, left, mid, right):
    if x[1] == "NUMPY":
        return right
    elif x[1] == "PIKE":
        return mid
    elif x[1] == "CUDA":
        return left


def x2(x, left, mid, right):
    if x[2] == 2008:
        return right
    elif x[2] == 1987:
        return mid
    elif x[2] == 2013:
        return left


def x3(x, left, mid, right):
    if x[3] == 1994:
        return right
    elif x[3] == 2005:
        return mid
    elif x[3] == 1959:
        return left


def x4(x, left, mid, right):
    if x[4] == 2010:
        return right
    elif x[4] == 1970:
        return mid
    elif x[4] == 1996:
        return left


def main(x):
    return x1(x, x2(x,
                    x3(x, x4(x, 0, 1, 2),
                       3, x4(x, 4, 5, 6)), 7, 8), 9, 10)
```


# 8 Задача

![image](https://github.com/produman66/kysspython/assets/115027939/f16544e9-d28c-4156-8b5c-1493fdb21c44) 
```python
def main(x):
    n1 = x[0][1]
    n2 = x[1][1]
    n3 = x[2][1]
    n4 = x[3][1]
    y = 0
    y = y | n1
    n2 = n2 << 6
    y = y | n2
    n3 = n3 << 11
    y = y | n3
    n4 = n4 << 19
    y = y | n4
    return hex(y)
```

![image](https://github.com/produman66/kysspython/assets/115027939/aece8f4c-1346-4cc4-95a6-11d23e07076e)
```python
# ИКБО-05-22 вариант-38
def create_hex_mask(num_bits):
    # Вычисляем максимальное значение для заданного количества бит
    max_value = (1 << num_bits) - 1
    return max_value

def main(n):
    # Extract the bit fields using appropriate masks
    W1 = (n >> 0) & create_hex_mask(10)    # bits 0-9, mask is 0x3FF (10 bits)
    W3 = (n >> 13) & create_hex_mask(7)    # bits 13-19, mask is 0x7F (7 bits)
    W4 = (n >> 20) & create_hex_mask(7)    # bits 20-26, mask is 0x7F (7 bits)
    W5 = (n >> 27) & create_hex_mask(3)    # bits 27-29, mask is 0x7 (3 bits)
    W6 = (n >> 30) & create_hex_mask(4)    # bits 30-33, mask is 0xF (4 bits)

    # Convert to hexadecimal strings
    W1_hex = hex(W1)
    W3_hex = hex(W3)
    W4_hex = hex(W4)
    W5_hex = hex(W5)
    W6_hex = hex(W6)

    # Create the result list of tuples
    result = [('W1', W1_hex), ('W3', W3_hex), ('W4', W4_hex), ('W5', W5_hex), ('W6', W6_hex)]

    return result

# Tests
print(main(6608546738))   # Expected: [('W1', '0x2ce'), ('W3', '0x2a'), ('W4', '0x3e'), ('W5', '0x2'), ('W6', '0x1')]
print(main(11577784042))  # Expected: [('W1', '0x202'), ('W3', '0x74'), ('W4', '0x0'), ('W5', '0x3'), ('W6', '0x2')]
```

![image](https://github.com/produman66/kysspython/assets/115027939/490bed3f-52de-40d2-a054-83a57f84a61c)
```python
#ИКБО-05-22 Вариант 39
def main(n):
    # Extract the bit fields
    P1 = (n >> 0) & 0b111111      # bits 0-6
    P2 = (n >> 6) & 0b1        # bits 7-11
    P3 = (n >> 7) & 0b11111          # bits 12-13
    P4 = (n >> 12) & 0b111111111    # bits 14-21
    result = (P2 << 0) | (P3 << 1) | (P1 << 6) | (P4 << 13)
    return str(result)

# Tests
print(main(451670))
print(main(626892))
print(main(766015))
```







