students = [
    {"name": "Laiba", "department": "Cyber Security", "grades": {"Networks": 89, "Python": 78}},
    {"name": "Maryam", "department": "Data Science", "grades": {"Python": 95, "Statistics": 90}},
    {"name": "Amina", "department": "AI", "grades": {"ML": 85, "Python": 88}}
]

print("---- Student Performance Records ----")
for student in students:
    print(f"Name: {student['name']}")
    print(f"Department: {student['department']}")
    print("Grades:")
    for course, grade in student['grades'].items():
        print(f"  {course}: {grade}")
    print("-" * 40)

print("\n---- Average Grades ----")
for student in students:
    grades = list(student['grades'].values())
    average_grade = sum(grades) / len(grades)
    print(f"{student['name']} ({student['department']}) → Average: {average_grade:.2f}")

top_student = None
highest_avg = 0

for student in students:
    avg = sum(student['grades'].values()) / len(student['grades'])
    if avg > highest_avg:
        highest_avg = avg
        top_student = student

print("\n---- Top Performer ----")
print(f" {top_student['name']} from {top_student['department']} "
      f"with an average grade of {highest_avg:.2f}")

department_toppers = {}
for student in students:
    dept = student["department"]
    avg = sum(student['grades'].values()) / len(student['grades'])
    if dept not in department_toppers or avg > department_toppers[dept]["avg"]:
        department_toppers[dept] = {"name": student["name"], "avg": avg}

print("\n---- Department-wise Toppers ----")
for dept, topper in department_toppers.items():
    print(f"{dept}: {topper['name']} (Average: {topper['avg']:.2f})")
