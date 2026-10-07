   What is an Escape Sequence?
   
   An escape sequence is a special combination of characters that starts with a backslash \.
   print("Hello\nWorld")  # hello
                            word
    here \n means new line  mainly In Python, the backslash is commonly used to create escape sequences.
    when we have to create 1 backslash then we have to use to the double blackslash
    print("C:\\Users\\Sriram")    #C:\Users\Sriram

           \b — Backspace

    Move the cursor one position backward.
     \b is the bring to the cursor 1 character position is backward 
     print("ABC\bD") python prints then cursor is here ABC|  so the cursor can move one position is back now AB|C
     so python prints D then . D is write in the cursor position 
     then u may see "ABD"
     > The exact visual result of \b can depend on the terminal you're using.
     The important concept is that \b sends a backspace control character; it isn't simply "delete the previous character" in every output environment.
          \u — Unicode

     Unicode is a standard for representing characters from different languages and symbols.
     A
   ఆ
   中
   ₹
   ❤
   Computers need numerical codes to represent these characters.
      What does \u do?

   Python allows us to write a Unicode character using:
  print("\u0041"))   result:A

  when we want to unicode and symbol we have to write the unicode then automatically symbol is there 
  you can representt the indian ruppes unicode is print("\u20B9") 

  What are hexadecimal digits?
    Hexadecimal means base 16.
        insted of only 0 1 2 3 4 5 6 7 8 9 we also have A B C D E F   so hexadecimal digits are 16 is there 

    \u → 4 digits
    \U → 8 digits

    \r cursor
   print("12345\rABC")
     ABC45                     #Because ABC overwrites the first three characters.
So \r doesn't erase the entire string.
It moves the cursor to the beginning, and the next characters can overwrite what was already there.
