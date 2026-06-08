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
