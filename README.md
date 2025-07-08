# Rhombix-task-1
# Fibonacci Series Generator
# By Manahil Fatima (Intern at Rhombix Technologies)

def fibonacci_series(n):
    # Start with the first two Fibonacci numbers
    fib = [0, 1]

    # Generate the next numbers in the series
    for i in range(2, n):
        next_number = fib[i - 1] + fib[i - 2]
        fib.append(next_number)

    return fib[:n]  # Return only the required terms

# Main program
try:
    # Ask the user for number of terms
    terms = int(input("Enter the number of terms: "))

    if terms <= 0:
        print("Please enter a positive integer.")
    else:
        print(f"\nFibonacci Series up to {terms} terms:")
        series = fibonacci_series(terms)
        print(series)

except ValueError:
    print("Invalid input! Please enter a valid integer.")
