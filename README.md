# GRADE-SYSTEAM-USING-PYTHON


# Student Result Generator by Shreyash Dusane

# Input Section
student_name = input("Enter student name: ")

Math = int(input("Enter your marks in Math (out of 100): "))
PPS = int(input("Enter your marks in PPS (out of 100): "))
BEEE = int(input("Enter your marks in BEEE (out of 100): "))
CS = int(input("Enter your marks in CS (out of 100): "))
EG = int(input("Enter your marks in EG (out of 100): "))

# Total and Percentage
total_marks = Math + PPS + BEEE + CS + EG
percentage = (total_marks / 500) * 100

# Check for subject failure
failed_subjects = set()

if Math < 35:
    failed_subjects.add("Math")
if PPS < 35:
    failed_subjects.add("PPS")
if BEEE < 35:
    failed_subjects.add("BEEE")
if CS < 35:
    failed_subjects.add("CS")
if EG < 35:
    failed_subjects.add("EG")

# Output Section
print("\n--- RESULT ---")
print(f"Student Name: {student_name}")
print(f"Total Marks: {total_marks} / 500")
print(f"Percentage: {percentage:.2f}%")

# Grade and Result
if failed_subjects:
    print("Result: ❌ FAIL")
    print("Subjects Failed:", ", ".join(failed_subjects))
else:
    if percentage >= 90:
        grade = "A+"
    elif percentage >= 80:
        grade = "A"
    elif percentage >= 70:
        grade = "B"
    elif percentage >= 60:
        grade = "C"
    elif percentage >= 40:
        grade = "D"
    else:
        grade = "F"

    
    
