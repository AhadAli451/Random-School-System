# It is a random school system

that's program work is that user or anyone or school staff want to  get a student details of any student so user or school staff pour a student roll number then it program will print complete detail of student  for this it will make 

__One thing noted__

firstly install pandas environment before use this program or like you making similar program even if you work in pandas there also install pandas environment 

+ How to install pandas environment simple 

```pip install pandas```

+ Second import 

```import pandas as pd```

**Some statement which use in program**

Like:

+ pandas 
+ if statement
+ input function
+  print
+ dictionary 
+ try Except
+ while  loop

Here are solution 

``` python
import pandas as pd

# Sample student data
student_data = {
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily', 'Frank', 'Grace'],
    'Class': [10, 9, 11, 10, 12, 9, 11],
    'roll_no': [566, 771, 312, 805, 710, 907, 999]
}

df = pd.DataFrame(student_data)

print("""Wellcome To The Random School System
===============================""")

while True:
    try:
        # Get roll number input from user
        roll_number = int(input("Enter Your Student Roll Number: "))

        # Check if roll number exists in the DataFrame
        if roll_number in df["roll_no"].values:
            # Filter the row corresponding to the roll number
            student_info = df.loc[df['roll_no'] == roll_number]
            # Print the student's details
            print("Your Data Is Here!")
            print(student_info[['name', 'Class', 'roll_no']])
            break
        else:
            print(f"Student with roll number {roll_number} is not found. Please try again.")
    except ValueError:
        print("Invalid input! Please enter a valid roll number.")
```

