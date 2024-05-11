# Command--line-arguments-to-count-word
## AIM:
To write a python program for getting the word count from the contents of a file using command line arguments.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1: Open Command Prompt or Terminal.

### Step 2: Navigate to the desktop directory using cd command.

### Step 3: Optionally, list files using dir (Windows) or Is (Unix-based).

### Step 4: Identify the target file.

### Step 5: Navigate to the directory containing the file using cd command.

### Step 6: Execute or perform operations on the file as needed.

## PROGRAM:
```
#DEVELOPED BY :MOHAMED HAMEEM SAJITH J
#REGISTER NUMBER : 212223240090

import sys

def count_words(filename):
    try:
        with open(filename, 'r') as file:
            text = file.read()
            words = text.split()
            return len(words)
    except FileNotFoundError:
        print("File not found.")
        return -1

def main():
    if len(sys.argv) != 2:
        print("Usage: python word_count.py <filename>")
        sys.exit(1)

    filename = sys.argv[1]
    word_count = count_words(filename)

    if word_count != -1:
        print("Word count:", word_count)

if __name__ == "__main__":
    main()

```

### OUTPUT:

![image](https://github.com/Sajith7862/Command--line-arguments-to-count-word/assets/145972360/9c7287fe-0138-467f-89c3-b491142488df)

## RESULT:
Thus the program is written to find the word count from the contents of a file using command line arguments.
