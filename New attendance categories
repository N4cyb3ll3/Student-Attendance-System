# Student_Attendance_System-By-Mateo-Rosario-Burlat-

attendance = {}

def add_student():
    name = input("Enter student name: ").title()

    if name in attendance:
        print("Student already exists.\n")
    else:
        attendance[name] = {"Present": 0, "Absent": 0, "Late": 0, "Late Filing": 0, "Excused": 0, "Special Order": 0, "Cutting Classes": 0}
        print("Student added successfully.\n")


def mark_attendance():
    name = input("Enter student name: ").title()

    if name not in attendance:
        print("Student not found.\n")
        return

    print("P - Present")
    print("A - Absent")
    print("L - Late")
    print("LF - Late Filing")
    print("E - Excused")
    print("SO - Special Order")
    print("CC - Cutting Classes")

    status = input("Enter status: ").upper()

    if status == "P":
        attendance[name]["Present"] += 1
    elif status == "A":
        attendance[name]["Absent"] += 1
    elif status == "L":
        attendance[name]["Late"] += 1
    elif status == "LF":
        attendance[name]["Late Filing"] += 1
    elif status == "E":
        attendance[name]["Excused"] += 1
    elif status == "SO":
        attendance[name]["Special Order"] += 1
    elif status == "CC":
        attendance[name]["Cutting Classes"] += 1
    else:
        print("Invalid input.\n")
        return

    print("Attendance recorded.\n")


def view_record():
    name = input("Enter student name: ").title()

    if name not in attendance:
        print("Student not found.\n")
        return

    print("Attendance Record for", name)
    print("Present:", attendance[name]["Present"])
    print("Absent:", attendance[name]["Absent"])
    print("Late:", attendance[name]["Late"])
    print("Late Filing:", attendance[name]["Late Filing"])
    print("Excused:", attendance[name]["Excused"])
    print("Special Order:", attendance[name]["Special Order"])
    print("Cutting Classes:", attendance[name]["Cutting Classes"])

    total_infractions = (
    attendance[name]["Absent"] +
    attendance[name]["Late"] +
    attendance[name]["Late Filing"] +
    attendance[name]["Cutting Classes"]
    )
    
    if total_infractions >= 3:
        print("Status: Probation")
    else:
        print("Status: Good Standing")

    print()


def view_all():
    if len(attendance) == 0:
        print("No students yet.\n")
        return

    for name in attendance:
        print(name)
        print("Present:", attendance[name]["Present"])
        print("Absent:", attendance[name]["Absent"])
        print("Late:", attendance[name]["Late"])
        print("Late Filing:", attendance[name]["Late Filing"])
        print("Excused:", attendance[name]["Excused"])
        print("Special Order:", attendance[name]["Special Order"])
        print("Cutting Classes:", attendance[name]["Cutting Classes"])


        if attendance[name]["Absent"]["Late"]["Late Filing"]["Cutting Classes"] >= 3:
            print("Status: Probation")
        else:
            print("Status: Good Standing")

        print()


def count_students():
    print("Total Students:", len(attendance))
    print()


def check_probation():
    name = input("Enter student name: ").title()

    if name not in attendance:
        print("Student not found.\n")
        return

    if attendance[name]["Absent"] >= 3:
        print(name, "is on Probation.\n")
    else:
        print(name, "is in Good Standing.\n")


def exit_program():
    print("Exiting Attendance System. Goodbye!")
    exit() # stops the program


while True:
    print("===== Attendance System =====")
    print("1 - Add Student")
    print("2 - Mark Attendance")
    print("3 - View Student Record")
    print("4 - View All Students")
    print("5 - Total Students")
    print("6 - Check Probation")
    print("7 - Exit")

    choice = input("Choose: ")

    if choice == "1":
        add_student()
    elif choice == "2":
        mark_attendance()
    elif choice == "3":
        view_record()
    elif choice == "4":
        view_all()
    elif choice == "5":
        count_students()
    elif choice == "6":
        check_probation()
    elif choice == "7":
        exit_program()
    else:
        print("Invalid choice.\n")
