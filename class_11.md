  slicing?
Slicing means extracting a portion of a string, list, or tuple.
 Positive indexes start at 0 from the left.
  Negative indexes start at -1 from the right.


  single slicing..
Single slicing uses one colon :.
syntax:
string[start:stop]

start = where to begin.
stop = where to stop, but the stop index is not included.
ex:
text = "PYTHON"
print(text[0:3]) #pyt
and in this slicing 3 is not executed only 0,1,2 slicings are included
text = "PYTHON"
print(text[2:5]) #THO
It starts at index 2 (T) and stops before index 5 (N).
and mainly we can understand the
text = "PYTHON"
print(text[:3])
print(text[2:])
print(text[:])
output:
PYT
THON
PYTHON
text[:3]  From the beginning up to index 3
text[2:]  From index 2 to the end
text[:]   The entire string
    double slicing
 In beginner Python lessons, double slicing sometimes means taking a slice using both a start index and a stop index, like text[1:4].
 Technically, that is just ordinary slicing.   
 text = "PYTHON"
print(text[1:5]) #YTHO
Here, 1 is the start and 5 is the stop. The character at index 5 is excluded.
However, if you mean two separate slicing operations, you can slice the result of another slice:
text = "PYTHON"
print(text[1:5][1:3]) #th
explanation:
text[1:5] gives "YTHO".
"YTHO"[1:3] gives "TH".

index of slicing:
string[start:stop:step]
ex:
text = "PYTHON"
print(text[0:6:2]) # PTO
Explanation:
Start at index 0 (p)
Move 2 positions  (T)
Move 2 positions (O)
   reverse a string using of slicing?
  text = "PYTHON"
print(text[::-1]) # NOHTYP
Here, -1 as the step means move backwards through the string.
ex:
text = "PYTHON"
print(text[5:1:-1])
#NOHT
It starts at index 5 (N) and moves backwards, stopping before index 1 (Y).
and this is the slicing.
