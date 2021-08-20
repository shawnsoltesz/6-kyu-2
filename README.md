# \_6_kyu

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

P

In a given string with lower case letters and no spaces, it may contain vowel (a, e, i, o, u) substrings. We need to transverse the string and 1. identify if there are any vowels, and if so 2. count the consecutive vowels and 3. determine the length of the longest grouping within the string. If the string contains zero vowels, return a 0.

E

vowels are any of - a, e, i, o, u
the string 'codewarriors' contains o,e,a,io
The longest of these has a length of 2 (io)

string 'fabulous' contains a, u, ou - the longest substring of these has a length of 2 (ou)
string 'envelope' contains e, e, o, e - the longest substring of these has a length of 1 (e)
string 'greasy' contains 'ea' - the longest substring length of these is 2 (ea)
string 'dry' contains no vowels - the longest substring length of these is Null
string 'epizootiologies' contains e, i, oo, io, o, ie - the longest substrings are length of this is 2 (oo, io, ie)

D

String
sub-string
Index of
Parse Int.32

A

1. Review the string of characters for vowels. for loop
2. Based on the length on the number of characters using the index number (for loop)
3. Establish a list of vowels variable(s)?
4. In a loop, use LINQ to transverse through the string and find any vowels
5. If a vowel is located, record a bool=True
6. Loop through the string to tally the number of trues of consecutive True
7. Loop through in Ascending order - value in index 0 is the longest substring
8. Return a value of 0 if no vowels in string
