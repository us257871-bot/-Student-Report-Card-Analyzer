import pandas as pd
import matplotlib.pyplot as plt

# === DATA ===
# Sirf 1 Teacher
teacher_data = {
    "teacher_name": ["Sir Umer"],
    "class": ["9th"],
    "subject": ["Math"]
}

# 38 Students
student_data = {
    "student_id": list(range(1, 39)), # 1 se 38 tak
    "student_name": [f"Student {i}" for i in range(1, 39)],
    "class": ["9th"] * 38,
    "marks": [75, 82, 90, 65, 88, 70, 95, 60, 77, 83, 91, 68, 85, 72, 89, 66, 
              78, 84, 92, 69, 80, 73, 87, 67, 79, 81, 93, 71, 76, 86, 94, 64, 
              74, 90, 63, 88, 70, 96]
}

teachers_df = pd.DataFrame(teacher_data)
students_df = pd.DataFrame(student_data)

# === MERGE ===
report_df = pd.merge(teachers_df, students_df, on="class")

# === ANALYSIS ===
print("=== Class Report Card ===")
print(report_df)
print(f"\nAverage Marks: {report_df['marks'].mean():.2f}")
print(f"Highest Marks: {report_df['marks'].max()}")

# === CHART ===
plt.figure(figsize=(12, 6)) # chart bada kar diya taake 38 naam fit hon
plt.bar(report_df["student_name"], report_df["marks"], color="skyblue")
plt.xticks(rotation=90)
plt.xlabel("Student Names")
plt.ylabel("Marks")
plt.title(f"{report_df['class'][0]} Class - {report_df['teacher_name'][0]} - {report_df['subject'][0]} Report")
plt.tight_layout() # ye line zaroori hai warna title cut ho jayega
plt.show()

# === SAVE CSV ===
report_df.to_csv("Class_9th_Math_Report.csv", index=False)
print("\nCSV file ban gai: Class_9th_Math_Report.csv")