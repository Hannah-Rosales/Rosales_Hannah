# Function to compute final grade
def compute_final_grade(midterm, minor_b, final_exam):
    # Calculate final grade
    final_grade = (0.30 * midterm) + (0.10 * minor_b) + (0.60 * final_exam)
    return final_grade

# Function to determine equivalent grade
def determine_equivalent_grade(final_grade):
    if 98 <= final_grade <= 100:
        return 4.00
    elif 95 <= final_grade <= 97:
        return 3.75
    elif 92 <= final_grade <= 94:
        return 3.50
    elif 89 <= final_grade <= 91:
        return 3.25
    elif 86 <= final_grade <= 88:
        return 3.00
    elif 83 <= final_grade <= 85:
        return 2.75
    elif 80 <= final_grade <= 82:
        return 2.50
    elif 77 <= final_grade <= 79:
        return 2.25
    elif 74 <= final_grade <= 76:
        return 2.00
    elif 71 <= final_grade <= 73:
        return 1.75
    elif 68 <= final_grade <= 70:
        return 1.50
    elif 64 <= final_grade <= 67:
        return 1.25
    elif 60 <= final_grade <= 63:
        return 1.00
    else:
        return 0.00

# Main program
def main():
    # Input student's name and grades
    student_name = input("Enter student's name: ")
    midterm_grade = float(input("Enter midterm grade: "))
    minor_b_grade = float(input("Enter minor B grade: "))
    final_exam_grade = float(input("Enter final exam grade: "))

    # Compute final grade
    final_grade = compute_final_grade(midterm_grade, minor_b_grade, final_exam_grade)

    # Determine equivalent grade
    equivalent_grade = determine_equivalent_grade(final_grade)

    # Output the results
    print("\n--- Student Grade Report ---")
    print(f"Student Name: {student_name}")
    print(f"Midterm Grade: {midterm_grade}")
    print(f"Minor B Grade: {minor_b_grade}")
    print(f"Final Exam Grade: {final_exam_grade}")
    print(f"Final Grade: {final_grade:.2f}")
    print(f"Equivalent Grade: {equivalent_grade:.2f}")

# Run the main program
if __name__ == "__main__":
    main()
