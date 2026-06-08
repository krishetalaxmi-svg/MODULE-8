# # 🔢 Hackerrank:# 🏆 Student Topper Finder

This Python program helps determine the **top-performing student** based on the total marks across five subjects. It uses a dictionary to store each student’s marks and identifies the topper using simple calculations and built-in functions.

---

## 🎯 Aim

To maintain a dictionary of students with their marks in five subjects, calculate their **total marks**, store them in a new dictionary, and identify the **student with the highest total (topper)**.

---

## 🧠 Algorithm

1. **Start** the program.
2. Create a dictionary `student_marks`:
   - Keys → Student names.
   - Values → List of marks in five subjects.
3. Initialize an empty dictionary `total_marks`.
4. Loop through `student_marks`:
   - Calculate the total marks using `sum()`.
   - Store the result in `total_marks`.
5. Use `max()` on `total_marks` to find the student with the highest total.
6. Print:
   - The `total_marks` dictionary.
   - The **topper's name and score**.

---

## 💻 PROGRAM:
      student_marks = {
          'Alice': [85, 90, 88, 92, 80],
          'Bob': [78, 82, 85, 88, 90],
          'Charlie': [90, 91, 92, 93, 94]
      }
      
      total_marks = {}
      
      for student in student_marks:
          total_marks[student] = sum(student_marks[student])
      
      topper = max(total_marks, key=total_marks.get)
      
      print(total_marks)
      print(topper, total_marks[topper])

## OUTPUT
<img width="587" height="299" alt="image" src="https://github.com/user-attachments/assets/26bd58d9-abc0-4000-b9ed-2137783b01a2" />

## RESULT
Thus, the program is verified successfully


# 🔄 Hackerrank : # 📦 Python Word Wrap Function

This Python program defines a function that **wraps a long string into multiple lines**, ensuring each line does not exceed a specified width.

---

## 🎯 Aim

To write a Python function that takes a long string and a specified width, and returns the string formatted with line breaks such that each line has **at most the given width**.

---

## 🧠 Algorithm

1. **Start** the program.
2. Define a function `wrap(string, max_width)`:
   - Create an empty list `wrapped_lines` to store parts of the string.
   - Loop through the string using steps of `max_width`.
   - In each iteration, extract a substring of length `max_width`.
   - Append this substring to the list.
3. Join the list with `\n` to create the final string.
4. Return the result.
5. **End** the program.

---


## 🧪 Program
      def wrap(string, max_width):
          wrapped_lines = []
          for i in range(0, len(string), max_width):
              wrapped_lines.append(string[i:i+max_width])
          return '\n'.join(wrapped_lines)
      
      string = input()
      max_width = int(input())
      print(wrap(string, max_width))


## Sample Output
<img width="805" height="309" alt="image" src="https://github.com/user-attachments/assets/9c196460-d9e3-4122-b66a-72dd6f3d93ae" />

## Result
Thus, the program is verified successfully.


# 🎓 Hackerrank:Python Program to Find Students with the Second Lowest Grade

This program reads student names and their corresponding grades, identifies the **second lowest grade**, and prints the names of all students who have that grade in **alphabetical order**.

---

## 🎯 Aim

To write a Python program to:
- Read a list of students and their grades.
- Identify the second lowest grade.
- Print the names of students who have that grade, sorted alphabetically.

---

## 🧠 Algorithm

1. **Read** an integer `n` representing the number of students.
2. **Read** each student’s name and grade, and store them as a sublist inside a list.
3. **Extract** all the grades and sort them.
4. **Identify** the second lowest grade from the sorted grade list.
5. **Collect** names of all students whose grade matches the second lowest grade.
6. **Sort** the names alphabetically.
7. **Print** each name on a new line.

---

## 💻  Program

    n = int(input())
    records = []
    
    for i in range(n):
        name = input()
        grade = float(input())
        records.append([name, grade])
    
    grades = sorted({grade for name, grade in records})
    second_lowest = grades[1]
    
    names = [name for name, grade in records if grade == second_lowest]
    names.sort()
    
    for name in names:
        print(name)

## Output
<img width="619" height="627" alt="image" src="https://github.com/user-attachments/assets/443d8970-e38b-4aee-beb3-53dfc99e67d3" />

## Result
Thus, the program is verified successfully


# 🏆 Hackerrank:Runner-Up Score Finder in Python

## 🎯 AIM:
To write a Python program that takes a list of scores from participants and finds the **runner-up score** (i.e., the second-highest score), eliminating any duplicates.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create a variable `n` and get its value from the user (number of participants)
3. Read the list of `n` scores from the user using `input().split()` and convert them to integers
4. Store the scores in a list
5. Use `set()` to remove any duplicate scores
6. Convert the set back to a list and sort it in ascending order
7. Print the second-last element of the sorted list (i.e., the runner-up score)
8. **Stop**

---

## 💻 PROGRAM:

    n = int(input())
    scores = list(map(int, input().split()))
    unique_scores = list(set(scores))
    unique_scores.sort()
    print(unique_scores[-2])

## OUTPUT
<img width="515" height="459" alt="image" src="https://github.com/user-attachments/assets/c03d9b3d-b871-4358-9a00-7761aa91cb36" />

## RESULT
Thus, the program is verified successfully.
