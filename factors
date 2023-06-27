import sys

def factorize_number(n):
    factors = []
    i = 2
    while i * i <= n:
        if n % i:
            i += 1
        else:
            n //= i
            factors.append((i, n))
    return factors

def factorize_file(filename):
    with open(filename, 'r') as file:
        for line in file:
            number = int(line.strip())
            factor_pairs = factorize_number(number)
            for factor_pair in factor_pairs:
                print(f"{number}={factor_pair[0]}*{factor_pair[1]}")

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: python factors.py <file>")
    else:
        filename = sys.argv[1]
        factorize_file(filename)

