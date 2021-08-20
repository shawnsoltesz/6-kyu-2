# \_6_kyu

Codewar: https://www.codewars.com/kata/59c5f4e9d751df43cf000035/train/csharp

The vowel substrings in the word codewarriors are o,e,a,io. The longest of these has a length of 2. Given a lowercase string that has alphabetic characters only (both vowels and consonants) and no spaces, return the length of the longest vowel substring. Vowels are any of the following letters - aeiou.

Documentation:
Kata.Solve Method (String)
Returns the length of the greatest continuous vowel substring in a string.

Syntax -

public static int Solve(
string str
)

Parameters -
str
Type: System.String
The string to be processed.

Return Value -
Type: System.Int32
The length of the greatest continuous vowel substring in str, or 0 if str contains no vowels.

Exceptions
Exception Condition
ArgumentNullException str is null.

---PEDA---

P

In a given string with lower case letters and no spaces, it may contain vowel (a, e, i, o, u) substrings. We need to transverse the string and 1. identify if there are any vowels, and if so 2. count the consecutive vowels and 3. determine the length of the longest grouping within the string. If the string contains zero vowels, return a 0.

E

1. vowels are any of - a, e, i, o, u
   the string 'codewarriors' contains o,e,a,io
   The longest of these has a length of 2 (io)

2. string 'fabulous' contains a, u, ou - the longest substring of these has a length of 2 (ou)
3. string 'envelope' contains e, e, o, e - the longest substring of these has a length of 1 (e)
4. string 'greasy' contains 'ea' - the longest substring length of these is 2 (ea)
5. string 'dry' contains no vowels - the longest substring length of these is Null
6. string 'epizootiologies' contains e, i, oo, io, o, ie - the longest substrings are length of this is 2 (oo, io, ie)
7. no string = mull

D

1. String
2. sub-string
3. Index of
4. Parse Int.32 (maybe?)

A

1. Review the string of characters for vowels. (for loop)
2. If no string, return Null exception
3. Otherwise based on the length on the number of characters using the index number (for loop)
4. Establish a list of vowels variable(s)(?)
5. In a loop, use (LINQ) to transverse through the string and find any vowels
6. If a vowel is located, record a (bool=True)
7. Loop through the string to tally the number of trues of consecutive True (Consecutive means number of 'trues' between 'falses') (maybe need Parse Int.32 here?)
8. Loop through tally in Ascending order - value in index 0 is the longest substring
9. Return a value of 0 if no vowels in string
