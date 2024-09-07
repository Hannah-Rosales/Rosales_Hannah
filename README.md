# Function to compute gross income
def compute_gross_income(hours_per_day, days_per_week, weeks_per_month):
    gross_income = hours_per_day * days_per_week * weeks_per_month
    return gross_income

# Function to compute deductions based on gross income
def compute_deductions(gross_income):
    pagibig_contribution = 100.00  # Pag-ibig is a fixed contribution
    
    # Determine SSS and PhilHealth contributions based on gross income ranges
    if gross_income <= 20000:
        sss_contribution = 100.00
        philhealth_contribution = 125.75
    elif 20001 <= gross_income <= 50000:
        sss_contribution = 1200.00
        philhealth_contribution = 2200.50
    elif 50001 <= gross_income <= 75000:
        sss_contribution = 6800.00
        philhealth_contribution = 4800.00
    else:  # Gross income > 75000
        sss_contribution = 8800.00
        philhealth_contribution = 5800.00
    
    # Calculate total deduction
    total_deduction = sss_contribution + pagibig_contribution + philhealth_contribution
    return total_deduction

# Main function to run the payroll computation
def main():
    # Input employee details
    employee_name = input("Enter employee's name: ")
    department = input("Enter employee's department: ")
    
    # Input working hours and rates
    hours_per_day = float(input("Enter number of working hours per day: "))
    days_per_week = int(input("Enter number of working days per week: "))
    weeks_per_month = int(input("Enter number of working weeks per month: "))
    
    # Compute gross income
    gross_income = compute_gross_income(hours_per_day, days_per_week, weeks_per_month)
    
    # Compute total deduction
    total_deduction = compute_deductions(gross_income)
    
    # Compute net income
    net_income = gross_income - total_deduction
    
    # Output the payroll details
    print("\n--- Employee Payroll Information ---")
    print(f"Employee Name: {employee_name}")
    print(f"Department: {department}")
    print(f"Gross Income: {gross_income:.2f}")
    print(f"Total Deduction: {total_deduction:.2f}")
    print(f"Net Income: {net_income:.2f}")

# Run the program
if __name__ == "__main__":
    main()
