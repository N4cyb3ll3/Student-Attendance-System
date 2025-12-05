# Student-Attendance-System (By: Burlat, Rosario, Mateo)

	attendance = {}

	def studentname():
		name = input("Enter student name: ").title()

    if name not in attendance:
        attendance[name] = {"Present": 0, "Absent": 0, "Late": 0}
        print(f"{name} has been added to the system.\n")
    else:
        print(f"{name} is already in the system.\n")


	def attendancerecord():
    name = input("Enter student name: ").title()

    if name not in attendance:
        print("Student not found. Please add them first.\n")
        return

    print("\nAttendance Status:")
    print("P - Present")
    print("A - Absent")
    print("L - Late")

    att_stat = input("Enter attendance status (P/A/L): ").upper()

    if att_stat == "P":
        attendance[name]["Present"] += 1
    elif att_stat == "A":
        attendance[name]["Absent"] += 1
    elif att_stat == "L":
        attendance[name]["Late"] += 1
    else:
        print("Invalid input.\n")
        return

    print(f"Attendance for {name} has been recorded.\n")


	def disp_att():
   	 name = input("Enter the student's name to view their record: ").title()

    if name not in attendance:
        print("Student not found.\n")
        return

    print(f"\n--- {name}'s Attendance Record ---")
    print(f"Present: {attendance[name]['Present']}")
    print(f"Absent: {attendance[name]['Absent']}")
    print(f"Late: {attendance[name]['Late']}\n")


	def exitprogram():
    	print("Exiting Student Attendance System. Goodbye!")
    exit()


	def main():
    while True:
        print("========== Attendance Menu ==========")
        print("1 - Add Student")
        print("2 - Mark Attendance")
        print("3 - View Attendance Record")
        print("4 - Exit System")
        print("=====================================")

        choice = input("Enter your choice: ")

        if choice == "1":
            studentname()
        elif choice == "2":
            attendancerecord()
        elif choice == "3":
            disp_att()
        elif choice == "4":
            exitprogram()
        else:
            print("Invalid Input. Please try again.\n")


	main()
