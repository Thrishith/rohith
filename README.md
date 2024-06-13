def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

nterms = 10

if nterms <= 0:
    print("Please enter a positive integer")
else:
    print("Fibonacci sequence:")
    for i in range(nterms):
        print(fibonacci(i))


def order(n):
    count = 0
    while n != 0:
        count += 1
        n //= 10
    return count

def is_armstrong(n, order_val):
    if n == 0:
        return 0
    else:
        return ((n % 10) ** order_val + is_armstrong(n // 10, order_val))

num = int(input("Enter a number: "))
order_val = order(num)

if num == is_armstrong(num, order_val):
    print(num, "is an Armstrong number.")
else:
    print(num, "is not an Armstrong number.")


    def gcd_recursive(a, b):
    if b == 0:
        return a
    else:
        return gcd_recursive(b, a % b)

num1 = 48
num2 = 18

result = gcd_recursive(num1, num2)
print(f"The GCD of {num1} and {num2} is: {result}")


def find_largest_element(arr):
    max_element = arr[0]
    for i in range(1, len(arr)):
        if arr[i] > max_element:
            max_element = arr[i]
    return max_element

# Example
array = [10, 5, 20, 8]
largest_element = find_largest_element(array)
print("The largest element in the array is:", largest_element)

