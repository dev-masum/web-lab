**✅ Problem No:** 2  

**Problem Name:** Write a program for finding the sum of all numbers in a given list.

**Source Code:**  

```python
def calculate_sum(numbers):
    total = 0
    for num in numbers:
        total += num
    return total

try:
    user_input = input("Enter numbers separated by spaces: ")
    
    number_list = list(map(int, user_input.split()))

    result = calculate_sum(number_list)
    print("The sum of the numbers is:", result)

except ValueError:
    print("Error: Please enter only integers separated by spaces.")

except Exception as e:
    print(f"An unexpected error occurred: {e}")

```

**✅ Problem No:** 3  

**Problem Name:** Write a program to solve Tower of Hanoi problem.

**Source Code:**  

```python
def tower_of_hanoi(n, source, auxiliary, destination):
    if n == 1:
        print(f"Move disk 1 from {source} to {destination}")
        return
    tower_of_hanoi(n - 1, source, destination, auxiliary)
    print(f"Move disk {n} from {source} to {destination}")
    tower_of_hanoi(n - 1, auxiliary, source, destination)

# Take input from the user
try:
    disks = int(input("Enter the number of disks: "))
    if disks <= 0:
        print("Number of disks must be greater than 0.")
    else:
        print("\nSteps to solve Tower of Hanoi:")
        tower_of_hanoi(disks, 'A', 'B', 'C')
except ValueError:
    print("Please enter a valid integer.")
```
