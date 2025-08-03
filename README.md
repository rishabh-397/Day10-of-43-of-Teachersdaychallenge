# Day10-of-43-of-Teachersdaychallenge

Okay, you've provided the problem descriptions for "A. Helpful Maths" and "A. Nearly Lucky Number" from Codeforces.

Here's the README.md information for these two problems, structured for your GitHub repository.

Additions to your existing README.md
You would append these sections to your README.md file, likely under the "💡 Codeforces Problems" heading.

7. A. Helpful Maths
Problem Description: Given a sum of numbers (1, 2, and 3) separated by '+', rearrange the summands in non-decreasing order and print the new sum. The input string contains no spaces and is at most 100 characters long.

Key Idea/Logic:

The problem is essentially asking to sort the numbers (1s, 2s, and 3s) while preserving the '+' signs.

Method 1: Parse, Sort, Reconstruct:

Extract all the numbers from the input string. A simple way is to iterate through the string and collect characters that are not '+'.

Store these numbers in a list or array.

Sort the list of numbers in non-decreasing order.

Reconstruct the string by joining the sorted numbers with '+' signs.

Method 2: Counting Sort (more efficient for fixed small range):

Count the occurrences of '1', '2', and '3'.

Build the result string by appending '1's, then '2's, then '3's, each followed by a '+' (except the last number).

Time Complexity:

O(LlogN) if using a general sort, where L is string length and N is count of numbers (N≈L/2).


Example:
Input: 3+2+1
Output: 1+2+3

Input: 1+1+3+1+3
Output: 1+1+1+3+3


A. Nearly Lucky Number
Problem Description: A "lucky number" contains only digits '4' and '7'. A number n is "nearly lucky" if the count of lucky digits within n is itself a lucky number. Given an integer n (up to 10^18), determine if it's nearly lucky.

Key Idea/Logic:

Count Lucky Digits: Iterate through the digits of the input number n. Count how many times '4' or '7' appear.

Since n can be up to 10^18, it's best to read it as a string or use a loop with modulo and division for large integers.

Check if Count is Lucky: Take the calculated count of lucky digits. Check if this count is a lucky number itself (i.e., it consists only of '4's and '7's).

To do this, convert the count to a string and iterate through its characters, verifying each is '4' or '7'.

Time Complexity: O(log 
10
​
 N) for counting lucky digits in N, plus O(log 
10
​
 (count of lucky digits)) for checking if the count is lucky. Overall, roughly O(number of digits in N).

Space Complexity: O(1) (or O(log 
10
​
 N) if N is read as a string).


 Example:
Input: 40047
Output: NO
Explanation: Lucky digits are 4, 4, 7. Count = 3. Is 3 a lucky number? No (contains digit '3').

Input: 7747774
Output: YES
Explanation: Lucky digits are 7, 7, 4, 7, 7, 7, 4. Count = 7. Is 7 a lucky number? Yes (contains only '7').

O(L) if using counting sort (which is optimal here due to the small, fixed range of numbers 1, 2, 3).

Space Complexity: O(L) for storing numbers or counts.
