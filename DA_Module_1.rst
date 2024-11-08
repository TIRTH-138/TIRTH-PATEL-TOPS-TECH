1. What are the type of application?
-> Types of Applications:
    - Web Applications
    - Desktop Gui Applications
    - Command-Line Applications
    - Data Science and Machine Learning
    - Game Devlopment
    - Automation & Scripting
    - Network Programming
    - Iot Applications
    - Embedded System
    - Web Scrapping
    - Mobile Applications
    - Blockchain
    - AI & Deep Learning
    - Scientific Applications
    - Database Applications                                 

2. What is programming?
-> Programming is the process of creating a set of instructions that a computer can follow to perform specific tasks. These instructions, written in a programming language, tell the computer how to process data, make decisions, and execute operations.

3. What is Python?
-> Python is a high-level, interpreted programming language known for its simplicity and readability. It was created by Guido van Rossum and first released in 1991. Python is designed to be easy to learn and use, making it a popular choice for beginners and experienced developers alike. and Pyhton is Case-Sensitive language.

.. code:: ipython3

    # 4. Write a Python program to check if a number is positive, negative or Zero.
    
    #Function to check the number 
    def check_number(num):
        if num > 0:
            return "The number is positve" 
        elif num < 0:
            return "The number is negative"
        else:
            return "The number is zero"
    
    # input from user   
    number = float(input("Enter a Number:"))
    
    # Output Result
    result = check_number(number)
    print(result)


.. parsed-literal::

    Enter a Number: 5
    

.. parsed-literal::

    The number is positve
    

.. code:: ipython3

    # 5. Write a Python program to get the Factorial number of given numbers.
    
    # Function to calculate factorial
    def factorial(n):
        if n==0 or n==1:
            return 1
        else:
            return n*factorial(n-1)
    
    # Input from user
    number = int(input("Enter a number:"))
    
    # Checking if the input is valid 
    if number < 0:
        print("factorial is not defined for negative numbers: ")
    else:
    # Output the factorial result
        result = factorial(number)
        print(result)


.. parsed-literal::

    Enter a number: 13
    

.. parsed-literal::

    6227020800
    

.. code:: ipython3

    # 6. Write a Python program to get the Fibonacci series of given range.
    
    # Function to generate fibonacci series up to n terms
    def fibonacci_series(n):
        fib_sequence = []
        a, b = 0, 1
        while len(fib_sequence) < n:
            fib_sequence.append(a)
            a,b = b, a + b
        return fib_sequence    
    
    # input: Range for fibonacci series
    n = int(input("Enter a number:"))
    
    # Output: Fibonacci series
    fib_sequence = fibonacci_series(n)
    print(fib_sequence)


.. parsed-literal::

    Enter a number: 13
    

.. parsed-literal::

    [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144]
    

7. How memory is managed in Python?
-> Memory Management in Python:
    - Automatic Management: Python uses an automatic memory management system with a private heap where all objects and data structures are stored.

    - Reference Counting: Python tracks the number of references to each object. When an object’s reference count drops to zero, memory is freed.

    - Garbage Collection: Python’s garbage collector handles cyclic references (objects referring to each other) to reclaim memory that reference                                  counting alone can’t manage.

    - Object-Specific Allocators: Python has specialized memory allocators (like pymalloc) for efficient management of small objects.
      Memory Optimization: Techniques like small object pooling and interning reduce memory usage for frequently used immutable objects.

8. What is the purpose continuing statement in Python?
-> The continue statement in Python is used within loops to skip the current iteration and move to the next iteration. When a continue statement is encountered, the remaining code inside the loop for that specific iteration ignored, and the loop proceeds with the next iteration based on the loop's condition.   

-> Purpose of continue:
    - Control Flow Management: It allows for more refined control over the execution of loop iterations by enabling specific conditions to bypass                                       certain actions without exiting the loop entirely.

    - Efficiency: By skipping unnecessary iterations or computations, it can make the loop execution more efficient, particularly when dealing with                        large datasets or complex conditions.

    - Code Clarity: It can help improve code readability by clearly indicating that certain conditions should lead to skipping the remainder of the loop                     for that iteration, rather than using nested conditionals.


.. code:: ipython3

    # 9. Write python program that swap two number with temp variable and without temp variable.
    
    # Swap two numbers using a temporary variable
    def swap_with_temp(t, r):
        temp = t
        t = r
        r = temp
        return t, r
    
    # Swap two numbers without using a temporary variable
    def swap_without_temp(t, r):
        t = t + r
        r = t - r
        t = t - r
        return t, r
    
    # Main function to test the swapping functions
    def main():
        num1 = 5
        num2 = 10
    
        print("Original numbers:")
        print(f"num1 = {num1}, num2 = {num2}")
    
    # Swap with temp variable
        num1, num2 = swap_with_temp(num1, num2)
        print("After swapping with temp variable:")
        print(f"num1 = {num1}, num2 = {num2}")
    
    # Swap back to original values for the next method
        num1, num2 = swap_with_temp(num1, num2)
    
    # Swap without temp variable
        num1, num2 = swap_without_temp(num1, num2)
        print("After swapping without temp variable:")
        print(f"num1 = {num1}, num2 = {num2}")
    
    if __name__ == "__main__":
        main()


.. parsed-literal::

    Original numbers:
    num1 = 5, num2 = 10
    After swapping with temp variable:
    num1 = 10, num2 = 5
    After swapping without temp variable:
    num1 = 10, num2 = 5
    

.. code:: ipython3

    # 10. Write a Python program to find whether a given number is even or odd, print out an appropriate message to the user.
    
    # Function to check if a number is even or odd  
    def check_even_odd(number):
        if number % 2 == 0:
            print(f"{number} is even number.")
        else:
            print(f"{number} is odd number.")
    
    # Input from the user
    num = int(input("Enter a number:"))
    check_even_odd(num)


.. parsed-literal::

    Enter a number: 4
    

.. parsed-literal::

    4 is even number.
    

.. code:: ipython3

    # 11. Write a Python program to test whether a passed letter is a vowel or not.
    
    # Function to check if the letter is a vowel
    def check_vowel(letter):
        vowels = 'aeiouAEIOU'  # List of vowels (both lowercase and uppercase)
        if letter in vowels:
            print(f"{letter} is a vowel.")
        else:
            print(f"{letter} is not a vowel.")
    
    # Input from the user
    char = input("Enter a letter:")
    
    # Check if input is a single character
    if len(char) == 1 and char.isalpha():
        check_vowel(char)
    else:
        print("Please enter a single letter.")
    


.. parsed-literal::

    Enter a letter: A
    

.. parsed-literal::

    A is a vowel.
    

.. code:: ipython3

    # 12. Write a Python program to sum of three given integers. However, if two values are equal sum will be zero.
    
    # Function to calculate the sum of three integers 
    def sum_three_integers(a,b,c):
        if a == b or a == c or b == c:
            return 0 
        else:
            return a + b + c
    
    # Input from user
    num1 = int(input("Enter the first integer:"))
    num2 = int(input("Enter the second integer:"))
    num3 = int(input("Enter the third integer:"))
    
    # Calculate and print the result
    result = sum_three_integers(num1, num2, num3)
    print(f"The result is: {result}")


.. parsed-literal::

    Enter the first integer: 1
    Enter the second integer: 2
    Enter the third integer: 3
    

.. parsed-literal::

    The result is: 6
    

.. code:: ipython3

    # 13. Write a Python program that will return true if the two giveninteger values are equal or their sum or difference is 5.
    
    # Function to check the conditions
    def check_values(a,b):
        if a == b or (a + b == 5) or (abs(a - b) == 5):
            return True
        else:
            return False 
    
    # Input from the user
    num1 = int(input("Enter the first integer:"))
    num2 = int(input("Enter the second integer:"))
    
    # Check and print the result
    result = check_values(num1,num2)
    print(f"The result is: {result}")


.. parsed-literal::

    Enter the first integer: 10
    Enter the second integer: 5
    

.. parsed-literal::

    The result is: True
    

.. code:: ipython3

    # 14. Write a python program to sum of the first n positive integers.
    
    def sum_of_integers(n):
        # Using the formula: sum = n*(n + 1) // 2
        return n*(n + 1) // 2
    
    # Input from user
    n = int(input("Enter a positive integer:"))
    print(f"The sum of the first {n} positive integers is: {sum_of_integers(n)}")


.. parsed-literal::

    Enter a positive integer: 3
    

.. parsed-literal::

    The sum of the first 3 positive integers is: 6
    

.. code:: ipython3

    # 15. Write a Python program to calculate the length of a string.
    
    # Get the string from the user
    string = input("Enter a string:")
    
    # Using len() function to calculate the length the string 
    len_of_string = len(string)
    
    # Display the length of the string 
    print(f"The length of the string is: {len_of_string}")


.. parsed-literal::

    Enter a string: I learn the Python language for Data Analytics.
    

.. parsed-literal::

    The length of the string is: 47
    

.. code:: ipython3

    # 16. Write a Python program to count the number of characters (character frequency) in a string
    
    # Python program to count character frequency in a string
    
    # Input: Get the string from the user
    input_string = input("Enter a string: ")
    
    # Create a dictionary to store character frequency
    char_frequency = {}
    
    # Loop through each character in the string
    for char in input_string:
        # If the character is already in the dictionary, increment its count
        if char in char_frequency:
            char_frequency[char] += 1
        else:
            # If not, add it to the dictionary with a count of 1
            char_frequency[char] = 1
    
    # Output: Display the character frequency
    print("Character frequency in the string:")
    for char, frequency in char_frequency.items():
        print(f"'{char}': {frequency}", end = " | ")
    


.. parsed-literal::

    Enter a string:  Python is easy to learn language.
    

.. parsed-literal::

    Character frequency in the string:
    'P': 1 | 'y': 2 | 't': 2 | 'h': 1 | 'o': 2 | 'n': 3 | ' ': 5 | 'i': 1 | 's': 2 | 'e': 3 | 'a': 4 | 'l': 2 | 'r': 1 | 'g': 2 | 'u': 1 | '.': 1 | 

17. What are negative indexes and why are they used?
-> Negative indexes in Python allow you to access elements from the end of a sequence (like lists, strings, or tuples). Instead of starting at 0 for the    first element, negative indexes start at -1 for the last element. For example, in a list my_list, my_list[-1] gives you the last element, and            my_list[-2] gives you the second-to-last element.

-> Uses of Negative Indexes:

    - Convenience: They enable easy access to elements at the end without needing to calculate the length of the sequence.
    - Clarity: They make code more readable. For example, my_list[-1] clearly indicates you want the last item, compared to calculating its index with                  len(my_list) - 1.
    - Slicing: They can be used in slicing to extract portions of a sequence from the end, such as my_list[-3:], which returns the last three elements.
               Overall, negative indexes enhance code simplicity and readability when dealing with sequences.

.. code:: ipython3

    # 18. Write a Python program to count occurrences of a substring in a string.
    
    # Input: Get the main string and the substring from the user
    main_string = input("Enter the main string: ")
    substring = input("Enter the substring to count: ")
    
    # Count the occurrences of the substring in the main string
    count = main_string.count(substring)
    
    # Output: Display the result
    print(f"The substring '{substring}' occurs {count} times in the main string.")


.. parsed-literal::

    Enter the main string:  Python is best language.
    Enter the substring to count:  Python
    

.. parsed-literal::

    The substring 'Python' occurs 1 times in the main string.
    

.. code:: ipython3

    # 19. Write a Python program to count the occurrences of each word in a 
    
    # Input: Get the string from the user
    input_string = input("Enter a string: ")
    
    # Split the string into words
    words = input_string.split()
    
    # Create a dictionary to store word frequency
    word_count = {}
    
    # Loop through each word in the list
    for word in words:
        # If the word is already in the dictionary, increment its count
        if word in word_count:
            word_count[word] += 1
        else:
            # If not, add it to the dictionary with a count of 1
            word_count[word] = 1
    
    # Output: Display the word frequency
    print("Word frequency in the string:")
    for word, count in word_count.items():
        print(f"'{word}': {count}", end=" | ")


.. parsed-literal::

    Enter a string:  I am Python language and Python is best language.
    

.. parsed-literal::

    Word frequency in the string:
    'I': 1 | 'am': 1 | 'Python': 2 | 'language': 1 | 'and': 1 | 'is': 1 | 'best': 1 | 'language.': 1 | 

.. code:: ipython3

    # 20. Write a Python program to get a single string from two given strings, separated by a space and swap the first two characters of each string. 
    
    # Input: Get two strings from the user
    string1 = input("Enter the first string: ")
    string2 = input("Enter the second string: ")
    
    # Swap the first two characters of each string
    # Ensure both strings have at least 2 characters
    if len(string1) > 1 and len(string2) > 1:
        swapped_string1 = string2[:2] + string1[2:]
        swapped_string2 = string1[:2] + string2[2:]
        
        # Combine the swapped strings with a space in between
        result = swapped_string1 + " " + swapped_string2
    else:
        result = "Strings are too short to swap first two characters."
    
    # Output: Display the final combined string
    print("Result:", result)


.. parsed-literal::

    Enter the first string:  Python is best language. 
    Enter the second string:  I am learning data analytics from tops technologies.
    

.. parsed-literal::

    Result: I thon is best language.  Pyam learning data analytics from tops technologies.
    

.. code:: ipython3

    # 21. Write a Python program to add 'in' at the end of a given string (length should be at least 3). If the given string already ends with 'ing' then add 'ly' instead if the string length of the given string is less than 3, leave it unchanged. 
    
    def modify_string(s):
        if len(s) < 3:
            return s
        elif s.endswith('ing'):
            return s + 'ly'
        else:
            return s + 'in'
    
    # Test cases
    print(modify_string("run"))  
    print(modify_string("playing"))  
    print(modify_string("go"))  


.. parsed-literal::

    runin
    playingly
    go
    

.. code:: ipython3

    # 22. Write a Python function to reverses a string if its length is a multiple of 4. 
    
    def reverse_str(s):
        if len(s) % 4 == 0:
            return s[::-1]
        else:
            return s
    
    # Test cases
    print("len of str is 4:",reverse_str("abcd")) 
    print("len of str is 5:",reverse_str("hello")) 
    print("len of str if 6:",reverse_str("python"))  


.. parsed-literal::

    len of str is 4: dcba
    len of str is 5: hello
    len of str if 6: python
    

.. code:: ipython3

    # 23. Write a Python program to get a string made of the first 2 and the last 2 chars from a given a string. If the string length is less than 2, return instead of the empty string.
    
    def first_last_chars(s):
        if len(s) < 2:
            return ''
        else:
            return s[:2] + s[-2:]
    
    # Test cases
    print(first_last_chars("spring"))  
    print(first_last_chars("hello"))   
    print(first_last_chars("a"))       
    print(first_last_chars("abcd"))    


.. parsed-literal::

    spng
    helo
    
    abcd
    

.. code:: ipython3

    # 24. Write a Python function to insert a string in the middle of a string. 
    
    def insert_string_middle(original, insert):
        return original[:5] + " " + insert + " " + original[-5:]
    
    # Example usage:
    original_string = "HelloWorld"
    string_to_insert = "Python"
    result = insert_string_middle(original_string, string_to_insert)
    print(result)  


.. parsed-literal::

    Hello Python World
    

25. What is list? How will you reverse a list?
-> A list is a data structure used to store an ordered collection of elements, which can be of various data types. Lists are mutable, meaning their         elements can be modified after creation.

-> To reverse a list:
1. Use the reverse() method to reverse it in place.
   
   Example: 
           Input: my_list = [1, 2, 3, 4, 5]
                  my_list.reverse()
                  print(my_list)
           Output: [5, 4, 3, 2, 1]

2. Use slicing ([::-1]) to create a reversed copy.
   
   Example: 
           Input: my_list = [1, 2, 3, 4, 5]
                  reversed_list = my_list[::-1]
                  print(reversed_list)
           Output: [5, 4, 3, 2, 1]   

3. Use the reversed() function to get an iterator and convert it to a list if needed.

   Example: 
           Input: my_list = [1, 2, 3, 4, 5]
                  reversed_list = list(reversed(my_list))
                  print(reversed_list)
           Output: [5, 4, 3, 2, 1]

26. How will you remove last object from a list?
-> To remove the last object from a list in Python, you can use the pop() method. This method removes and returns the last item of the list.
   Example:
           Input: my_list = [1, 2, 3, 4, 5]
                  my_list.pop()
                  print(my_list)
           Output: [1, 2, 3, 4]

27. Suppose list1 is [2, 33, 222, 14, and 25], what is list1 [-1]? 
-> In Python, using a negative index accesses elements from the end of the list. Specifically, list1[-1] refers to the last element of the list.
   Example:
           Input: list1 = [2, 33, 222, 14, 25]
                  list[-1]
           Output: 25  

28. Differentiate between append () and extend () methods? 
-> The append() and extend() methods in Python are both used to add elements to a list, but they behave differently:

-> append()
   1. Purpose: Adds a single element to the end of a list.
   2. Behavior: The element added can be of any data type(including another list), but it is treated as a single entity.
   3. Example:
              Input: my_list = [1, 2, 3]
                     my_list.append(4)
                     my_list.append([5, 6])
                     print(my_list)
              Output: [1, 2, 3, 4, [5, 6]]

-> extend()
   1. Purpose: Adds multiple elements to the end of a list.
   2. Behavior: The elements from the iterable (e.g., another list) are unpacked and added individually to the list.
   3. Example: 
              Input: my_list = [1, 2, 3]
                     my_list.extend(4)
                     my_list.extend([4, 5])
                     print(my_list)
              Output: [1, 2, 3, 4, 5]

-> Summary
   :- Use append() to add a single item, which could be a list itself.
   :- Use extend() to add multiple items from an iterable, expanding the list.

.. code:: ipython3

    # 29. Write a Python function to get the largest number, smallest num and sum of all from a list. 
    
    def get_list_stats(numbers):
        if not numbers:  # Check if the list is empty
            return None, None, 0
    
        largest = max(numbers)  # Get the largest number
        smallest = min(numbers)  # Get the smallest number
        total_sum = sum(numbers)  # Get the sum of all numbers
    
        return largest, smallest, total_sum
    
    # Example usage
    numbers = [10, 20, 5, 40, 15]
    print("Largest number:", largest)
    print("Smallest number:", smallest)
    print("Sum of all numbers:", total_sum)
    


.. parsed-literal::

    Largest number: 40
    Smallest number: 5
    Sum of all numbers: 90
    

30. How will you compare two lists? 
-> To compare two lists in Python, you can use the following methods:
   
   1. Equality Comparison (==): Checks if two lists have the same elements in the same order.
         Example: list1 == list2
   
   2. Element-wise Comparison with all(): Compares each corresponding element of two lists.
         Example: all(a == b for a, b in zip(list1, list2))

   3. Unordered Comparison with set(): Checks if two lists contain the same unique elements, regardless of order.
         Example: set(list1) == set(list2)

   4. Length Comparison: Compares the lengths of two lists to see if they have the same number of elements.
         Example: len(list1) == len(list2)

-> These methods allow you to check for equality, size, and order of elements in lists effectively.

.. code:: ipython3

    # 31. Write a Python program to count the number of strings where the string length is 2 or more and the first and last character are same from a given list of strings. 
    
    def count_strings(strings):
        count = 0
        for string in strings:
            if len(string) >= 2 and string[0] == string[-1]:
                count += 1
        return count
    
    # Example usage:
    strings_list = ['abc', 'xyz', 'aba', '1221', 'aa', 'abba', 'defed']
    result = count_strings(strings_list)
    print(f"The number of strings with matching first and last characters is: {result}")


.. parsed-literal::

    The number of strings with matching first and last characters is: 5
    

.. code:: ipython3

    # 32. Write a Python program to remove duplicates from a list. 
    
    def remove_duplicates(input_list):
        return list(set(input_list))
    
    # Example usage:
    my_list = [1, 2, 2, 3, 4, 4, 5, 6, 6, 7]
    result = remove_duplicates(my_list)
    print(f"List after removing duplicates: {result}")


.. parsed-literal::

    List after removing duplicates: [1, 2, 3, 4, 5, 6, 7]
    

.. code:: ipython3

    # 33. Write a Python program to check a list is empty or not. 
    
    def is_list_empty(input_list):
        return len(input_list) == 0
    
    # Example usage:
    my_list = []
    if is_list_empty(my_list):
        print("The list is empty.")
    else:
        print("The list is not empty.")


.. parsed-literal::

    The list is empty.
    

.. code:: ipython3

    # 34. Write a Python function that takes two lists and returns true if they have at least one common member.
    
    def have_common_member(list1, list2):
        # Convert both lists to sets and check if they have an intersection
        return bool(set(list1) & set(list2))
    
    # Example usage:
    list1 = [1, 2, 3, 4]
    list2 = [4, 5, 6, 7]
    
    print(have_common_member(list1, list2))  # Output: True


.. parsed-literal::

    True
    

.. code:: ipython3

    # 35. Write a Python program to generate and print a list of first and last 5 elements where the values are square of numbers between 1 and 30. 
    
    def generate_squares():
        # Generate the list of squares of numbers between 1 and 30
        squares = [x**2 for x in range(1, 31)]
        
        # Print the first and last 5 elements
        result = squares[:5] + squares[-5:]
        return result
    
    # Example usage
    print(generate_squares())


.. parsed-literal::

    [1, 4, 9, 16, 25, 676, 729, 784, 841, 900]
    

.. code:: ipython3

    # 36. Write a Python function that takes a list and returns a new list with unique elements of the first list. 
    
    def get_unique_elements(input_list):
        return list(set(input_list))
    
    # Example usage
    original_list = [1, 2, 2, 3, 4, 4, 5, 5, 5]
    unique_list = get_unique_elements(original_list)
    print(unique_list)


.. parsed-literal::

    [1, 2, 3, 4, 5]
    

.. code:: ipython3

    # 37. Write a Python program to convert a list of characters into a string. 
    
    # Define a list of characters
    char_list = ['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
    
    # Convert the list of characters into a string
    result_string = ''.join(char_list)
    
    # Print the result
    print("The converted string is:", result_string)


.. parsed-literal::

    The converted string is: Hello World
    

.. code:: ipython3

    # 38. Write a Python program to select an item randomly from a list. 
    
    import random
    
    # Define a list of items
    items = [1, 2, 3, 4, 5, "apple", "banana", "cherry"]
    
    # Select a random item from the list
    random_item = random.choice(items)
    
    # Print the selected item
    print("The randomly selected item is:", random_item)


.. parsed-literal::

    The randomly selected item is: 4
    

.. code:: ipython3

    # 39. Write a Python program to find the second smallest number in a list. 
    
    # Define a list of numbers
    numbers = [10, 5, 3, 8, 6, 3, 12]
    
    # Remove duplicates by converting the list to a set, then convert back to a sorted list
    unique_numbers = sorted(set(numbers))
    
    # Check if there are at least two unique numbers
    if len(unique_numbers) < 2:
        print("There is no second smallest number.")
    else:
        # The second smallest number is at index 1 in the sorted list
        second_smallest = unique_numbers[1]
        print("The second smallest number is:", second_smallest)


.. parsed-literal::

    The second smallest number is: 5
    

.. code:: ipython3

    # 40. Write a Python program to get unique values from a list 
    
    # Define a list with some duplicate values
    my_list = [1, 2, 2, 3, 4, 4, 5, 6, 6]
    
    # Use set() to get unique values
    unique_values = list(set(my_list))
    
    # Print the unique values
    print("The unique values are:", unique_values)


.. parsed-literal::

    The unique values are: [1, 2, 3, 4, 5, 6]
    

.. code:: ipython3

    # 41. Write a Python program to check whether a list contains a sub list 
    
    # Define a main list and a sublist
    main_list = [1, 2, 3, 4, 5, 6, 7]
    sub_list = [3, 4, 5]
    
    # Check if the sublist is in the main list
    def contains_sublist(main_list, sub_list):
        # Get the length of both lists
        len_main = len(main_list)
        len_sub = len(sub_list)
    
        # Loop through the main list and check for the sublist
        for i in range(len_main - len_sub + 1):
            if main_list[i:i + len_sub] == sub_list:
                return True
        return False
    
    # Call the function and print the result
    if contains_sublist(main_list, sub_list):
        print("The main list contains the sublist.")
    else:
        print("The main list does not contain the sublist.")


.. parsed-literal::

    The main list contains the sublist.
    

.. code:: ipython3

    # 42. Write a Python program to split a list into different variables 
    
    # Define a list with multiple elements
    my_list = [1, 2, 3, 4, 5]
    
    # Unpack the list elements into different variables
    a, b, c, d, e = my_list
    
    # Print each variable to confirm
    print("a =", a)
    print("b =", b)
    print("c =", c)
    print("d =", d)
    print("e =", e)


.. parsed-literal::

    a = 1
    b = 2
    c = 3
    d = 4
    e = 5
    

43. What is tuple? Difference between list and tuple. 

-> A tuple is a built-in data structure in Python that allows you to store a collection of items. It is similar to a list, but it has some important        characteristics that set it apart.

-> Key Characteristics of Tuples:
     1. Ordered: The elements in a tuple are arranged in a specific sequence. Each element can be accessed using an index.
     2. Immutable: Once a tuple is created, its contents cannot be changed. You cannot add, remove, or modify the elements.
     3. Heterogeneous: A tuple can contain items of different data types, such as integers, strings, and even other collections like lists or tuples.

-> Difference Between List and Tuple
____________________________________________________________________________________________________________________________________  
|Feature	 |                List	                                      |                        Tuple                           |
|____________|____________________________________________________________|________________________________________________________|
|Syntax	     |   Created using square brackets []	                      |  Created using parentheses ()                          |
|------------|------------------------------------------------------------|--------------------------------------------------------|
|Mutability	 |   Mutable (can be modified after creation)	              |  Immutable (cannot be modified after creation)         |
|------------|------------------------------------------------------------|--------------------------------------------------------|
|Methods	 |   Supports many methods (e.g., adding, removing elements)  |	 Supports fewer methods (mostly accessing elements)    |
|------------|------------------------------------------------------------|--------------------------------------------------------|
|Performance |   Generally slower due to mutability	                      |  Typically faster because of immutability              |
|------------|------------------------------------------------------------|--------------------------------------------------------|
|Use Case	 |   Ideal for collections that may change	                  |  Ideal for fixed collections that should not change    |
|____________|____________________________________________________________|________________________________________________________|

.. code:: ipython3

    # 44. Write a Python program to create a tuple with different data types. 
    
    # Creating a tuple with different data types
    my_tuple = (1, "Hello", 3.14, True, None)
    
    # Printing the tuple
    print("Tuple with different data types:")
    print(my_tuple)
    
    # Accessing elements of the tuple
    print("\nAccessing elements:")
    print("Integer:", my_tuple[0])
    print("String:", my_tuple[1])
    print("Float:", my_tuple[2])
    print("Boolean:", my_tuple[3])
    print("NoneType:", my_tuple[4])
    
    # Tuple length
    print("\nLength of the tuple:", len(my_tuple))


.. parsed-literal::

    Tuple with different data types:
    (1, 'Hello', 3.14, True, None)
    
    Accessing elements:
    Integer: 1
    String: Hello
    Float: 3.14
    Boolean: True
    NoneType: None
    
    Length of the tuple: 5
    

.. code:: ipython3

    # 45. Write a Python program to unzip a list of tuples into individual lists. 
    
    # List of tuples
    tuple_list = [(1, 'apple'), (2, 'banana'), (3, 'cherry'), (4, 'date')]
    
    # Unzipping the list of tuples
    list1, list2 = zip(*tuple_list)
    
    # Converting the results to lists
    list1 = list(list1)
    list2 = list(list2)
    
    # Printing the individual lists
    print("List 1:", list1)
    print("List 2:", list2)


.. parsed-literal::

    List 1: [1, 2, 3, 4]
    List 2: ['apple', 'banana', 'cherry', 'date']
    

.. code:: ipython3

    # 46. Write a Python program to convert a list of tuples into a dictionary. 
    
    # List of tuples
    tuple_list = [('a', 1), ('b', 2), ('c', 3), ('d', 4)]
    
    # Converting the list of tuples into a dictionary
    dictionary = dict(tuple_list)
    
    # Printing the resulting dictionary
    print("Dictionary:", dictionary)


.. parsed-literal::

    Dictionary: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
    

47. How will you create a dictionary using tuples in python? 
-> A dictionary in Python is a collection of key-value pairs. To create a dictionary from a list of tuples, each tuple should contain two elements: the     first element will be the key and the second element will be the value.
        -> Example 1: Using the dict() function
           -> You can use the built-in dict() function to convert a list of tuples into a dictionary.
               Input:
                   # Step 1: Define a list of tuples
                   tuple_list = [('apple', 1), ('banana', 2), ('cherry', 3)]

                   # Step 2: Convert the list of tuples into a dictionary
                   fruit_dict = dict(tuple_list)

                   # Step 3: Print the dictionary
                   print("Fruit Dictionary:", fruit_dict)
               Output:
                   Fruit Dictionary: {'apple': 1, 'banana': 2, 'cherry': 3}

        -> Example 2: Using a Loop
            -> Alternatively, you can create a dictionary by looping through the list of tuples.
                Input: 
                    # Step 1: Define a list of tuples
                    tuple_list = [('apple', 1), ('banana', 2), ('cherry', 3)]

                    # Step 2: Initialize an empty dictionary
                    fruit_dict = {}

                    # Step 3: Loop through the list of tuples
                    for key, value in tuple_list:
                    fruit_dict[key] = value  # Assign key-value pairs to the dictionary

                    # Step 4: Print the dictionary
                    print("Fruit Dictionary:", fruit_dict)
                Output:
                    Fruit Dictionary: {'apple': 1, 'banana': 2, 'cherry': 3}

-> Conclusion:
    -> Both methods are effective for creating a dictionary from tuples. The dict() function is more concise, while the loop method provides more               control and can be modified easily for additional logic if needed. Use the method that best suits your assignment requirements!

.. code:: ipython3

    # 48. Write a Python script to sort (ascending and descending) a dictionary by value. 
    
    # Sample dictionary
    my_dict = {'apple': 5, 'banana': 2, 'cherry': 7, 'date': 1}
    
    # Sorting the dictionary by value in ascending order
    sorted_asc = dict(sorted(my_dict.items(), key=lambda item: item[1]))
    
    # Sorting the dictionary by value in descending order
    sorted_desc = dict(sorted(my_dict.items(), key=lambda item: item[1], reverse=True))
    
    # Printing the results
    print("Sorted Dictionary (Ascending):", sorted_asc)
    print("Sorted Dictionary (Descending):", sorted_desc)


.. parsed-literal::

    Sorted Dictionary (Ascending): {'date': 1, 'banana': 2, 'apple': 5, 'cherry': 7}
    Sorted Dictionary (Descending): {'cherry': 7, 'apple': 5, 'banana': 2, 'date': 1}
    

.. code:: ipython3

    # 49. Write a Python script to concatenate following dictionaries to create a new one. 
    
    # Dictionaries to concatenate
    dict1 = {'a': 1, 'b': 2}
    dict2 = {'c': 3, 'd': 4}
    dict3 = {'e': 5, 'f': 6}
    
    # Concatenate dictionaries
    new_dict = {**dict1, **dict2, **dict3}
    
    print("Concatenated dictionary:", new_dict)


.. parsed-literal::

    Concatenated dictionary: {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5, 'f': 6}
    

.. code:: ipython3

    # 50. Write a Python script to check if a given key already exists in a dictionary. 
    
    # Sample dictionary
    my_dict = {'a': 1, 'b': 2, 'c': 3}
    
    # Key to check
    key_to_check = 'b'
    
    # Check if the key exists
    if key_to_check in my_dict:
        print(f"The key '{key_to_check}' exists in the dictionary.")
    else:
        print(f"The key '{key_to_check}' does not exist in the dictionary.")


.. parsed-literal::

    The key 'b' exists in the dictionary.
    

51. How Do You Traverse Through a Dictionary Object in Python? 
-> Traversing a dictionary in Python means going through each item it contains, which can be done in a few different ways. Here’s an easy-to-understand     guide for your assignment.

-> What is a Dictionary?
    -> A dictionary in Python stores data as key-value pairs. 
        -> Example: 
            -> Input: my_dict = {'name': 'Tirth', 'age': 22, 'city': 'Ahmedabad'}
            -> In this dictionary: 'name', 'age', and 'city' are keys
                                   'Tirth', 22, and 'Ahmedabda' are values

-> Ways to Traverse a Dictionary
    -> You can loop through dictionaries in three main ways:
        1. Loop Through the Keys Only:
          -> To get just the keys from a dictionary, you can use a for loop like this:
          -> Input: for key in my_dict:
                        print("Key:", key)
          -> Explanation: This loop goes through each key in the dictionary. 
          -> Output: Key: name
                     Key: age
                     Key: city

        2. Loop Through the Values Only:
          -> If you want only the values, use .values():
          -> Input: for value in my_dict.values():
                        print("Value:", value)
          -> Explanation: Here, we’re getting each value (like 'Alice', 25, etc.) in the dictionary. 
          -> Output: Value: Alice
                     Value: 25
                     Value: New York
        
        3. Loop Through Both Keys and Values
          -> To get both the key and the value together, use .items():
          -> Input: for key, value in my_dict.items():
                        print("Key:", key, "Value:", value)
          -> Explanation: This goes through each key-value pair. 
          -> Output: Key: name Value: Alice
                     Key: age Value: 25
                     Key: city Value: New York

-> Summary
        Keys only: for key in my_dict
        Values only: for value in my_dict.values()
        Both keys and values: for key, value in my_dict.items()

52. How Do You Check the Presence of a Key in A Dictionary? 
-> To check if a key exists in a dictionary in Python, you can use a simple approach with the in keyword. Here’s a straightforward explanation for your     assignment.

-> Why Check for a Key?
    -> In Python, dictionaries store data as key-value pairs. Before you try to access the value of a key, it's a good idea to check if that keyexists.         If the key isn't there, you might get an error.

-> How to Check if a Key Exists
    -> The easiest way to check for a key in a dictionary is to use the in keyword.

-> Example
    -> # Sample dictionary
       my_dict = {'name': 'Alice', 'age': 25, 'city': 'New York'}

       # Key to check
       key_to_check = 'age'

       # Checking if the key exists
       if key_to_check in my_dict:
           print(f"The key '{key_to_check}' is present in the dictionary.")
       else:
           print(f"The key '{key_to_check}' is not present in the dictionary.")

    -> Explanation
        -> in keyword: 
            :- key_to_check in my_dict checks if the key ('age' in this case) exists in my_dict.
            :- If the key is found, it will print a message confirming its presence. If not, it will print that the key is not present.
    
    -> Output: The key 'age' is present in the dictionary.

-> Summary
    -> To check for a key:
        :- Use if key in dictionary for a quick check.
        :- Output will tell you if the key is there or not.

.. code:: ipython3

    # 53. Write a Python script to print a dictionary where the keys are numbers between 1 and 15. 
    
    # Creating the dictionary with keys from 1 to 15 and values as the square of each key
    number_dict = {key: key**2 for key in range(1, 16)}
    
    # Printing the dictionary
    print("Dictionary with keys 1 to 15 and their squares as values:")
    print(number_dict)


.. parsed-literal::

    Dictionary with keys 1 to 15 and their squares as values:
    {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100, 11: 121, 12: 144, 13: 169, 14: 196, 15: 225}
    

.. code:: ipython3

    # 54. Write a Python program to check multiple keys exists in a dictionary.
    
    # Sample dictionary
    my_dict = {'name': 'Alice', 'age': 25, 'city': 'New York'}
    
    # Keys to check
    keys_to_check = ['name', 'age']
    
    # Check if all keys are in the dictionary
    if (key in my_dict for key in keys_to_check):
        print("All keys exist in the dictionary.")
    else:
        print("Not all keys exist in the dictionary.")


.. parsed-literal::

    All keys exist in the dictionary.
    

.. code:: ipython3

    # 55. Write a Python script to merge two Python dictionaries 
     
    # Two sample dictionaries
    dict1 = {'a': 1, 'b': 2}
    dict2 = {'c': 3, 'd': 4}
    
    # Method 1: Using the | operator (Python 3.9 and above)
    merged_dict = dict1 | dict2
    print("Merged dictionary using '|':", merged_dict)
    
    # Method 2: Using update() method (Compatible with earlier versions)
    # This will update dict1 to include keys and values from dict2
    dict1.update(dict2)
    print("Merged dictionary using update():", dict1)


.. parsed-literal::

    Merged dictionary using '|': {'a': 1, 'b': 2, 'c': 3, 'd': 4}
    Merged dictionary using update(): {'a': 1, 'b': 2, 'c': 3, 'd': 4}
    

.. code:: ipython3

    # 56. Write a Python program to map two lists into a dictionary - Sample output: Counter ({'a': 400, 'b': 400,’d’: 400, 'c': 300}).
    
    # Two sample lists
    keys = ['a', 'b', 'c', 'd']
    values = [400, 400, 300, 400]
    
    # Mapping lists into a dictionary
    mapped_dict = dict(zip(keys, values))
    
    print("Mapped dictionary:", mapped_dict)


.. parsed-literal::

    Mapped dictionary: {'a': 400, 'b': 400, 'c': 300, 'd': 400}
    

.. code:: ipython3

    # 57. Write a Python program to find the highest 3 values in a dictionary.
    
    def find_highest_three_values(input_dict):
        # Check if the dictionary has less than 3 items
        if len(input_dict) < 3:
            return "The dictionary must have at least three items."
    
        # Get the three highest values
        highest_values = sorted(input_dict.values(), reverse=True)[:3]
        return highest_values
    
    # Example usage
    sample_dict = {
        'a': 10,
        'b': 20,
        'c': 30,
        'd': 25,
        'e': 15
    }
    
    result = find_highest_three_values(sample_dict)
    print("The highest three values are:", result)


.. parsed-literal::

    The highest three values are: [30, 25, 20]
    

.. code:: ipython3

    # 58. Write a Python program to combine values in python list of dictionaries.
    #     Sample data: [{'item': 'item1', 'amount': 400}, {'item': 'item2', 'amount':300}, {'item': 'item1', 'amount': 750}]
    #     Expected Output: Counter ({'item1': 1150, 'item2': 300})
    
    from collections import Counter
    
    def combine_values(data):
        # Initialize a Counter to hold the combined amounts
        combined = Counter()
    
        # Iterate through each dictionary in the list
        for entry in data:
            item = entry['item']
            amount = entry['amount']
            combined[item] += amount
    
        return combined
    
    # Sample data
    sample_data = [
        {'item': 'item1', 'amount': 400},
        {'item': 'item2', 'amount': 300},
        {'item': 'item1', 'amount': 750}
    ]
    
    # Combine the values
    result = combine_values(sample_data)
    print("Counter:", result)


.. parsed-literal::

    Counter: Counter({'item1': 1150, 'item2': 300})
    

.. code:: ipython3

    # 59. Write a Python program to create a dictionary from a string. Note: Track the count of the letters from the string. 
    
    def count_letters(input_string):
        # Initialize an empty dictionary to store the counts
        letter_count = {}
    
        # Iterate through each character in the string
        for char in input_string:
            # Convert to lowercase to count letters case-insensitively
            char = char.lower()
            
            # Check if the character is a letter
            if char.isalpha():
                # Increment the count for the character
                if char in letter_count:
                    letter_count[char] += 1
                else:
                    letter_count[char] = 1
    
        return letter_count
    
    # Example usage
    sample_string = "Hello, World!"
    result = count_letters(sample_string)
    print("Letter count:", result)


.. parsed-literal::

    Letter count: {'h': 1, 'e': 1, 'l': 3, 'o': 2, 'w': 1, 'r': 1, 'd': 1}
    

.. code:: ipython3

    # 60. Sample string: 'w3resource' Expected output: {'3': 1,’s’: 1, 'r': 2, 'u': 1, 'w': 1, 'c': 1, 'e': 2, 'o': 1}
    
    # Sample string
    input_string = 'w3resource'
    
    # Initialize an empty dictionary to store the counts
    char_count = {}
    
    # Iterate through each character in the string
    for char in input_string:
        # Increment the count for the character
        if char in char_count:
            char_count[char] += 1
        else:
            char_count[char] = 1
    
    # Output the character count
    print("Character count:", char_count)


.. parsed-literal::

    Character count: {'w': 1, '3': 1, 'r': 2, 'e': 2, 's': 1, 'o': 1, 'u': 1, 'c': 1}
    

.. code:: ipython3

    # 61. Write a Python function to calculate the factorial of a number (a non negative integer) 
    
    def factorial(n):
        # Check if the input is a non-negative integer
        if n < 0:
            raise ValueError("Input must be a non-negative integer.")
        if n == 0 or n == 1:
            return 1
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result
    
    # Example usage
    number = int(input("Enter a number:"))
    print(f"The factorial of {number} is {factorial(number)}.")


.. parsed-literal::

    Enter a number: 5
    

.. parsed-literal::

    The factorial of 5 is 120.
    

.. code:: ipython3

    # 62. Write a Python function to check whether a number is in a given range.
    
    def is_in_range(num, start, end):    
        return start <= num <= end
    
    # Example usage
    number = 10
    range_start = 5
    range_end = 15
    
    if is_in_range(number, range_start, range_end):
        print(f"{number} is in the range [{range_start}, {range_end}].")
    else:
        print(f"{number} is not in the range [{range_start}, {range_end}].")


.. parsed-literal::

    10 is in the range [5, 15].
    

.. code:: ipython3

    # 63. Write a Python function to check whether a number is perfect or not. 
    
    def is_perfect(number):
        # A number must be greater than 1 to be considered perfect
        if number < 1:
            return False
        
        # Find divisors and sum them
        divisors_sum = sum([i for i in range(1, number) if number % i == 0])
        
        # Check if the sum of divisors equals the number
        return divisors_sum == number
    
    # Example usage:
    num = 6
    if is_perfect(num):
        print(f"{num} is a perfect number.")
    else:
        print(f"{num} is not a perfect number.")


.. parsed-literal::

    6 is a perfect number.
    

.. code:: ipython3

    # 64. Write a Python function that checks whether a passed string is palindrome or not.
    
    def is_palindrome(string):
        # Convert string to lowercase to ignore case sensitivity
        string = string.lower()
        # Remove any spaces from the string
        string = string.replace(" ", "")
        # Check if the string is equal to its reverse
        return string == string[::-1]
    
    # Test the function
    input_string = "racecar"
    print(is_palindrome(input_string))  # Output: True


.. parsed-literal::

    True
    

65. How Many Basic Types of Functions Are Available in Python? 
-> In Python, there are two basic types of functions:

    1. Built-in Functions
        -> These are functions that are already defined in Python and can be used directly without needing to write any code for them.
        -> Examples include print(), len(), type(), input(), and sum().
        -> Built-in functions are part of the Python language itself, so you don’t have to define them to use them.
    -> Example: 
        -> Input: print("Hello, World!")  # 'print()' is a built-in function
                  length = len("Python")  # 'len()' gives the length of the string

    2. User-defined Functions
        -> These are functions that you create yourself to perform specific tasks.
        -> You define these functions using the def keyword, followed by the function name and any parameters it needs.
        -> User-defined functions are useful when you need to repeat certain operations multiple times in your code.
    -> Example:
        -> Input: def greet(name):
                  return f"Hello, {name}!"
                  print(greet("Alice"))

-> Summary
    -> Built-in Functions: Ready-made functions provided by Python (like print() and len()).
    -> User-defined Functions: Functions that you create yourself for specific tasks.

66. How can you pick a random item from a list or tuple? 
-> To pick a random item from a list or tuple in Python, you can use the choice() function from the random module. This is a built-in function in Python    that helps you choose a random element from a sequence (like a list or tuple).

-> How to Pick a Random Item Step-by-Step
    -> Import the random module at the beginning of your program. The random module has functions to work with random values.
    -> Use random.choice() and pass the list or tuple you want to choose from as an argument. This function will then pick one item randomly from that          list or tuple.

-> Example:
    -> Input: import random

              # Example list and tuple
              my_list = [10, 20, 30, 40, 50]
              my_tuple = ('apple', 'banana', 'cherry', 'date')
            
              # Picking a random item from the list
              random_item_from_list = random.choice(my_list)
              print("Random item from list:", random_item_from_list)
            
              # Picking a random item from the tuple
              random_item_from_tuple = random.choice(my_tuple)
              print("Random item from tuple:", random_item_from_tuple)

    -> Output: Random item from list: 30
               Random item from tuple: banana

-> Summary
    -> Using random.choice() is an easy way to pick a random item from any list or tuple in Python. Just remember to import the random module first!

67. How can you pick a random item from a range? 
-> To pick a random item from a range in Python, you can use the randrange() function from the random module. This function allows you to select a          random number within a specified range.

-> Steps to Pick a Random Item from a Range
    -> Import the random module at the start of your program.
    -> Use random.randrange(start, stop) where start is the beginning of the range, and stop is the end. This will pick a random number between start           and stop - 1 (it doesn’t include the stop value itself).

-> Example: 
       -> Input: import random

                 # Define the range
                 start = 1
                 stop = 10
        
                 # Pick a random number from the range 1 to 9 (stop is exclusive)
                 random_number = random.randrange(start, stop)
                 print("Random item from the range:", random_number)

        -> Output: Random item from the range: 5

-> Summary 
-> To pick a random item from a range:
       -> Use random.randrange(start, stop) after importing the random module.
       -> Remember, the stop value is not included, so it picks a random number from start to stop - 1.

68. How can you get a random number in python? 
-> To get a random number in Python, you can use the random module, which comes built-in with Python. Here are a few easy ways to get random numbers:

    1. Getting a Random Integer in a Range
        -> If you want a random integer between two numbers (say between 1 and 10), you can use the randint function.
            -> Example
                -> Input: import random
                          random_number = random.randint(1, 10)
                          print(random_number)
                -> Explanation: This will give you a random integer between 1 and 10, including both 1 and 10.

    2. Getting a Random Decimal Number Between 0 and 1
        -> If you want a random decimal (or floating-point number) between 0 and 1, you can use the random function.
            -> Example
                -> Input: import random
                          random_decimal = random.random()
                          print(random_decimal)
                -> Explanation: This will give you a random decimal number between 0 and 1. Each time you run it, you'll get a different decimal.

    3. Getting a Random Decimal Number in a Range
        -> To get a random decimal number within a specific range (for example, between 5.5 and 10.5), you can use the uniform function.
            -> Example
                -> Input: import random
                          random_decimal_range = random.uniform(5.5, 10.5)
                          print(random_decimal_range)
                -> Explanation: This will give you a random decimal number between 5.5 and 10.5, including both 5.5 and 10.5.

-> Summary
    -> randint(a, b) for a random integer between a and b.
    -> random() for a random decimal between 0 and 1.
    -> uniform(a, b) for a random decimal between a and b.
    -> Using any of these methods is simple and will give you different random numbers each time you run them!

69. How will you set the starting value in generating random numbers?

-> To set the starting value (or seed) when generating random numbers in Python, you can use the seed function from the random module. Setting a seed       ensures that you get the same "random" numbers each time you run your code, which is helpful for testing and debugging.
    -> Example
        -> Input: import random
                  # Set the seed to a specific value, e.g., 42
                  random.seed(42)

                  # Now generate random numbers
                  print(random.randint(1, 10))
                  print(random.random())
        -> In this example, setting random.seed(42) means that each time you run the code, it will produce the same "random" numbers. You can replace 42            with any integer to get a different sequence of numbers.

-> Why Use a Seed?
    -> Reproducibility: When you set a seed, you can recreate the same sequence of random numbers. This is helpful in experiments and simulations where                          you want consistent results.
    -> Testing: Setting a seed helps you test code with predictable outcomes, making it easier to identify issues.
   
-> Without setting a seed, the numbers generated by random will be different each time you run the program, which is usually the default and desired        behavior for most applications.

70. How will you randomize the items of a list in place? 
-> To randomize the items in a list (also known as shuffling the list) in Python, you can use the shuffle function from the random module. This function    changes the order of the list items randomly "in place," which means the original list itself is modified and no new list is created.
    -> Example
    -> Here’s an example to shuffle a list of numbers:
        -> Input: import random

                  # Original list
                  my_list = [1, 2, 3, 4, 5]

                  # Shuffle the list
                  random.shuffle(my_list)

                  print(my_list)

-> Explanation:
    -> random.shuffle(my_list) will rearrange the items in my_list randomly.
    -> Since shuffle works "in place," it modifies my_list directly instead of creating a new list.
    -> Each time you run this code, my_list will have a different random order.

-> Important Points
    -> In-place modification: shuffle changes the order of items directly in the original list.
    -> Random order: Each time you shuffle, the order will be different.    

-> This is useful when you need to randomize data, like shuffling a deck of cards or creating random quizzes.

71. What is File function in python? What are keywords to create and write file. 
-> In Python, the "File" function usually refers to working with files using built-in functions that allow you to create, read, write, and close files.     Here’s an easy explanation of how it works:

-> File Handling in Python
    -> Python provides built-in functions to open and handle files. The main function used is open(), which opens a file so you can perform various             operations like reading or writing. When you’re done, you should always close the file using the close() method.

-> Keywords and Functions to Create and Write to a File
    1. Creating a File
        -> Use the open() function with the mode "w" or "a" to create a new file.
        -> "w" (write mode): Creates a new file if it doesn’t exist, or overwrites the file if it does exist.
        -> "a" (append mode): Creates a new file if it doesn’t exist, or adds data to the end of an existing file.
            -> Example
                -> Input: # Creating a new file in write mode
                          file = open("example.txt", "w")

    2. Writing to a File
        -> Use the write() method to add text to the file.
        -> If you use "w" mode, it will overwrite any existing content. If you use "a" mode, it will add (append) to the existing content.
            -> Example
                -> Input: # Writing text to the file
                          file.write("Hello, this is a test.")

    3. Closing the File
        -> After performing all operations, close the file using close(). This ensures all data is saved and frees up system resources.
            -> Example
                -> Input: # Closing the file
                          file.close()

-> Summary of Important Keywords
    -> open(): Opens a file.
    -> "w": Write mode, creates a file if it doesn’t exist or overwrites it.
    -> "a": Append mode, creates a file if it doesn’t exist or appends to the end if it does.
    -> write(): Writes text to the file.
    -> close(): Closes the file.

.. code:: ipython3

    # 72. Write a Python program to read an entire text file. 
    
    # Program to read an entire text file
    
    # Step 1: Open the file in read mode
    # Replace 'filename.txt' with the name of the file you want to read
    file = open('C:\\Users\\TIRTH PATEL\\Desktop\\tirth.txt', 'r')
    
    # Step 2: Read the entire content of the file
    content = file.read()
    
    # Step 3: Print the content to display it
    print(content)
    
    # Step 4: Close the file to free up resources
    file.close()


.. parsed-literal::

    Hello, My name is tirth.
    

.. code:: ipython3

    # 73. Write a Python program to append text to a file and display the text. 
    
    # Function to append text to a file and display its content
    def append_and_display(file_name, text_to_append):
        # Open the file in append mode and write the text
        with open(file_name, 'a') as file:
            file.write(text_to_append + '\n')  # Add a newline after appending text
    
        # Open the file in read mode to display its content
        with open(file_name, 'r') as file:
            content = file.read()
    
        # Display the content
        print("Updated File Content:")
        print(content)
    
    # Example usage
    file_name = 'Tirth_append.txt'
    text_to_append = "My favourite game is Volleyball."
    append_and_display(file_name, text_to_append)


.. parsed-literal::

    Updated File Content:
    I am learning Data Analytics in Tops Technologies.
    Hello, My name is Tirth Patel.
    I am B.com Graduated.
    My experience in marketing field of 1.5 year.
    My favourite game is Volleyball.
    
    

.. code:: ipython3

    # 74. Write a Python program to read first n lines of a file. 
    
    # Function to read the first n lines of a file
    def read_first_n_lines(file_name, n):
        with open(file_name, 'r') as file:
            # Use a loop to read and print the first n lines
            for i in range(n):
                line = file.readline()
                # If there are fewer than n lines, break the loop when no more lines are found
                if not line:
                    break
                print(line.strip())  # Print each line without extra newline
    
    # Example usage
    file_name = 'Tirth_append.txt'
    n = 5  # Number of lines to read
    read_first_n_lines(file_name, n)


.. parsed-literal::

    I am learning Data Analytics in Tops Technologies.
    Hello, My name is Tirth Patel.
    I am B.com Graduated.
    My experience in marketing field of 1.5 year.
    My favourite game is Volleyball.
    

.. code:: ipython3

    # 75. Write a Python program to read last n lines of a file.
    
    from collections import deque
    
    # Function to read the last n lines of a file
    def read_last_n_lines(file_name, n):
        with open(file_name, 'r') as file:
            # Use deque to keep only the last n lines in memory
            last_n_lines = deque(file, maxlen=n)
        
        # Print the last n lines
        for line in last_n_lines:
            print(line.strip())  # Print each line without extra newline
    
    # Example usage
    file_name = 'Tirth_append.txt'
    n = 5  # Number of lines to read from the end
    read_last_n_lines(file_name, n)


.. parsed-literal::

    I am learning Data Analytics in Tops Technologies.
    Hello, My name is Tirth Patel.
    I am B.com Graduated.
    My experience in marketing field of 1.5 year.
    My favourite game is Volleyball.
    

.. code:: ipython3

    # 76. Write a Python program to read a file line by line and store it into a list 
    
    # Function to read file and store lines in a list
    def read_file_to_list(filename):
        lines = []
        try:
            with open(filename, 'r') as file:
                lines = file.readlines()
                lines = [line.strip() for line in lines]  # Remove any trailing newline characters
        except FileNotFoundError:
            print(f"The file '{filename}' was not found.")
        return lines
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your file name
    lines_list = read_file_to_list(filename)
    print(lines_list)


.. parsed-literal::

    ['I am learning Data Analytics in Tops Technologies.', 'Hello, My name is Tirth Patel.', 'I am B.com Graduated.', 'My experience in marketing field of 1.5 year.', 'My favourite game is Volleyball.']
    

.. code:: ipython3

    # 77. Write a Python program to read a file line by line store it into a variable. 
    
    # Function to read file and store content in a variable
    def read_file_to_variable(filename):
        content = ""
        try:
            with open(filename, 'r') as file:
                content = file.read()  # Read all lines at once
        except FileNotFoundError:
            print(f"The file '{filename}' was not found.")
        return content
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your file name
    file_content = read_file_to_variable(filename)
    print(file_content)


.. parsed-literal::

    I am learning Data Analytics in Tops Technologies.
    Hello, My name is Tirth Patel.
    I am B.com Graduated.
    My experience in marketing field of 1.5 year.
    My favourite game is Volleyball.
    
    

.. code:: ipython3

    # 78. Write a python program to find the longest words. 
    
    # Function to find the longest word in a file
    def find_longest_word(filename):
        with open(filename, 'r') as file:
            words = file.read().split()
        longest_word = max(words, key=len)
        return longest_word
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your file name
    print("Longest word:", find_longest_word(filename))


.. parsed-literal::

    Longest word: Technologies.
    

.. code:: ipython3

    # 79. Write a Python program to count the number of lines in a text file. 
    
    # Function to count the number of lines in a file
    def count_lines(filename):
        with open(filename, 'r') as file:
            lines = file.readlines()
        return len(lines)
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your file name
    print("Number of lines:", count_lines(filename))


.. parsed-literal::

    Number of lines: 5
    

.. code:: ipython3

    # 80. Write a Python program to count the frequency of words in a file. 
    
    # Function to count word frequency in a file
    from collections import Counter
    
    def count_word_frequency(filename):
        with open(filename, 'r') as file:
            words = file.read().lower().split()  # Convert to lowercase and split into words
        word_count = Counter(words)
        return word_count
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your file name
    word_frequencies = count_word_frequency(filename)
    print("Word frequencies:", word_frequencies)


.. parsed-literal::

    Word frequencies: Counter({'my': 3, 'i': 2, 'am': 2, 'in': 2, 'is': 2, 'learning': 1, 'data': 1, 'analytics': 1, 'tops': 1, 'technologies.': 1, 'hello,': 1, 'name': 1, 'tirth': 1, 'patel.': 1, 'b.com': 1, 'graduated.': 1, 'experience': 1, 'marketing': 1, 'field': 1, 'of': 1, '1.5': 1, 'year.': 1, 'favourite': 1, 'game': 1, 'volleyball.': 1})
    

.. code:: ipython3

    # 81. Write a Python program to write a list to a file. 
    
    # Function to write a list to a file
    def write_list_to_file(filename, items):
        with open(filename, 'w') as file:
            for item in items:
                file.write(f"{item}\n")
    
    # Example usage
    filename = 'Tirth_append.txt'  # Replace with your desired file name
    my_list = ["apple", "banana", "cherry", "date"]
    write_list_to_file(filename, my_list)
    print(f"List written to {filename}")


.. parsed-literal::

    List written to Tirth_append.txt
    

.. code:: ipython3

    # 82. Write a Python program to copy the contents of a file to another file. 
    
    # Function to copy contents of one file to another
    def copy_file(source_file, destination_file):
        with open(source_file, 'r') as src, open(destination_file, 'w') as dest:
            dest.write(src.read())
    
    # Example usage
    source_file = 'Tirth_append.txt'  # Replace with your source file name
    destination_file = 'Tirth_append1.txt'  # Replace with your destination file name
    copy_file(source_file, destination_file)
    print(f"Contents copied from {source_file} to {destination_file}")


.. parsed-literal::

    Contents copied from Tirth_append.txt to Tirth_append1.txt
    

83. Explain Exception handling? What is an Error in Python? 
-> Exception handling in Python is a mechanism to manage errors during the execution of a program, allowing the code to respond gracefully instead of       abruptly stopping. This is accomplished using the try, except, else, and finally blocks. Here’s a breakdown:
    -> try block: Code that might cause an exception is placed here. Python will try to execute this code.
    -> except block: If an exception occurs in the try block, the code in the except block executes. This helps to handle errors without crashing the                         program.
    -> else block: Code in the else block runs if no exception was raised in the try block.
    -> finally block: This block always runs, regardless of whether an exception occurred, and is commonly used for cleanup actions.                                            (e.g., closing files).

-> Example
    -> Input: try:
                  result = 10 / 0
              except ZeroDivisionError:
                  print("Cannot divide by zero!")
              else:
                  print("Division successful:", result)
              finally:
                  print("Execution completed.")
    -> In this example:
        -> If there’s a division by zero, the except block will handle the ZeroDivisionError.
        -> If no error occurs, the else block executes.
        -> The finally block will always run, regardless of an exception.

-> What is an Error in Python?
-> An error in Python is an issue in a program that prevents it from running correctly. Errors can be classified as:
    -> Syntax Errors: Errors in the syntax of the code, such as missing colons or incorrect indentation. These are detected before execution.
        -> Example: print("Hello World" (missing closing parenthesis)
    -> Exceptions: Errors that occur during execution. Python provides various built-in exceptions, such as ZeroDivisionError, ValueError, and                              FileNotFoundError.
        -> Example: Dividing by zero or trying to access a file that doesn’t exist

84. How many except statements can a try-except block have? Name Some built-in exception classes: 
-> A try-except block in Python can have multiple except statements to handle different types of exceptions. Each except statement can specify a            different exception type to catch specific errors. There’s technically no limit to the number of except blocks you can have in a single try-except       block.

-> Some Built-in Exception Classes in Python:
-> Here are some common built-in exception classes:
    1. ValueError: Raised when an operation receives an argument of the right type but an inappropriate value.
    2. TypeError: Raised when an operation is applied to an object of inappropriate type.
    3.IndexError: Raised when trying to access an index that is out of the range of a list or tuple.
    4. KeyError: Raised when a dictionary key is not found.
    5. FileNotFoundError: Raised when trying to open a file that does not exist.
    6. ZeroDivisionError: Raised when trying to divide by zero.
    7. AttributeError: Raised when an invalid attribute is referenced.
    8. ImportError: Raised when an import statement fails to import a module.
    9. IOError: Raised when an input/output operation fails (e.g., reading or writing files).
    10. OverflowError: Raised when a calculation exceeds the limits for a numeric type.

85. When will the else part of try-except-else be executed? 
-> The else part of a try-except-else block in Python is executed only if the code in the try block does not raise any exceptions. It provides a way to     define a block of code that should run when the try block is successful.
-> Example
    -> Input: try:
                  result = 10 / 2  # This will succeed
              except ZeroDivisionError:
                  print("Cannot divide by zero!")
              else:
                  print("Division successful, result is:", result)  # This will run if no exception occurs
    -> Explanation:
        -> In the above example, since 10 / 2 does not raise any exceptions, the code in the else block executes, printing the result.                           -> If there had been an exception (for example, if we tried to divide by zero), the except block would have executed, and the else block would              be skipped.
-> Key Points:
    -> The else block is useful for code that should run only after the try block executes successfully without errors.
    -> It helps in separating the error handling (in except) from the successful execution code, improving code readability.

86. Can one block of except statements handle multiple exception? 
-> Yes, a single except block in Python can handle multiple exceptions by specifying the exception types as a tuple. This allows you to catch different     exceptions with the same handling code.
-> Example
    -> Input: try:
                  num = int(input("Enter a number: "))
                  result = 10 / num
              except (ValueError, ZeroDivisionError) as e:
                  print("An error occurred:", e)
    -> Explanation:
        -> In the example above, the except block is designed to catch both ValueError (if the input is not a number) and ZeroDivisionError                         (if the input is 0).
        -> If either of these exceptions occurs, the program will print the error message along with the specific exception message.
-> Key Points:
    -> Using a single except block for multiple exceptions can help reduce code duplication and make error handling more efficient.
    -> You can still access the caught exception using the as keyword, allowing you to print or log specific details about the error.

87. When is the finally block executed? 
-> The finally block in Python is executed always, regardless of whether an exception was raised or handled in the try block. Here are the key scenarios where the finally block will be executed:

    1. No Exception Raised: If the code in the try block executes successfully without any exceptions, the finally block will run after the try block.

    2. Exception Raised and Caught: If an exception occurs and is caught by an except block, the finally block will still execute afterward.

    3. Exception Raised but Not Caught: If an exception occurs that is not caught by an except block, the finally block will execute before the program                                          terminates.

    4. Program Exit: If the program exits via a sys.exit() call or due to an unhandled exception, the finally block will execute just before the program                      exits.

88. What happens when „1‟== 1 is executed?
-> When the expression “1” == 1 is executed in Python, it evaluates to False. Here’s why:
    1. Data Types: The left side of the expression is a string ("1"), and the right side is an integer (1). In Python, the equality operator (==) checks                    for both value and type equality.
    2. Type Mismatch: Since the two operands are of different types (string vs integer), Python determines that they cannot be equal.
    3. Result: The expression will return False.
-> Example
    -> Input: result = "1" == 1
              print(result)  # Output: False
-> Summary:
    -> Expression: “1” == 1
    -> Evaluation: False (due to type mismatch)
    -> Reason: Different data types (string vs integer) are not considered equal in Python.

89. How Do You Handle Exceptions with Try/Except/Finally in Python? Explain with coding snippets
-> In Python, you can handle exceptions using the try, except, and finally blocks. This structure allows you to manage errors gracefully while ensuring     that certain code always executes, regardless of whether an exception occurred. Here’s how each part works:
     1. try Block
         -> The try block contains code that might raise an exception. If an exception occurs, the control is passed to the corresponding except block.
     2. except Block
         -> The except block is used to handle specific exceptions that might be raised in the try block. You can have multiple except blocks to handle              different types of exceptions.
     3. finally Block
         -> The finally block contains code that will execute regardless of whether an exception occurred or was caught. This is useful for cleanup                  actions, such as closing files or releasing resources.

-> Explanation:
    -> try Block: The code attempts to divide num1 by num2.
    -> except ZeroDivisionError: If num2 is 0, this block will execute, printing an error message.
    -> except TypeError: If either num1 or num2 is not a number (like a string), this block will execute.
    -> else Block: If no exceptions occur, this block will print the successful division result.
    -> finally Block: This block executes no matter what, ensuring that any cleanup actions are performed. It always runs after the try and except                             blocks.

-> Summary:
    -> Use the try block to enclose code that might raise an exception.
    -> Handle specific exceptions in except blocks.
    -> Use the finally block for cleanup code that should always execute. 
-> Example: The example is write down above shell.

.. code:: ipython3

    # 89. How Do You Handle Exceptions with Try/Except/Finally in Python? Explain with coding snippets
    
    def divide_numbers(num1, num2):
        try:
            # Attempt to divide two numbers
            result = num1 / num2
        except ZeroDivisionError:
            # Handle the case where division by zero occurs
            print("Error: Cannot divide by zero.")
            return None
        except TypeError:
            # Handle the case where the inputs are not numbers
            print("Error: Both inputs must be numbers.")
            return None
        else:
            # This block runs if no exceptions were raised
            print("Division successful. Result:", result)
            return result
        finally:
            # This block always executes, regardless of exceptions
            print("Execution of finally block.")
    
    # Example usage
    print("Example 1:")
    divide_numbers(10, 2)  # Valid division
    
    print("\nExample 2:")
    divide_numbers(10, 0)  # Division by zero
    
    print("\nExample 3:")
    divide_numbers(10, "a")  # Invalid input type


.. parsed-literal::

    Example 1:
    Division successful. Result: 5.0
    Execution of finally block.
    
    Example 2:
    Error: Cannot divide by zero.
    Execution of finally block.
    
    Example 3:
    Error: Both inputs must be numbers.
    Execution of finally block.
    

.. code:: ipython3

    # 90. Write python program that user to enter only odd numbers, else will raise an exception. 
    
    def get_odd_number():
        while True:
            try:
                # Prompt the user for input
                number = int(input("Enter an odd number: "))
                # Check if the number is odd
                if number % 2 == 0:
                    raise ValueError("The number entered is even. Please enter an odd number.")
                else:
                    print(f"Thank you! You entered the odd number: {number}")
                    break  # Exit the loop if an odd number is entered
            except ValueError as e:
                print(e)  # Print the error message
    
    # Example usage
    get_odd_number()


.. parsed-literal::

    Enter an odd number:  2
    

.. parsed-literal::

    The number entered is even. Please enter an odd number.
    

.. parsed-literal::

    Enter an odd number:  1
    

.. parsed-literal::

    Thank you! You entered the odd number: 1
    

