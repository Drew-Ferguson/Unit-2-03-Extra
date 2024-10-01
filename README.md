# Unit-2-03-Extra
def calculate_birth_year(age, had_birthday_this_year):
    current_year = 2024  # You can also use the datetime module to get the current year dynamically
    if had_birthday_this_year:
        birth_year = current_year - age
    else:
        birth_year = current_year - age - 1
    return birth_year

def main():
    # Asking for user input
    name = input("What is your name? ")
    age = int(input("What is your age? "))
    had_birthday = input("Have you had a birthday this year? (yes/no) ").strip().lower()

    # Checking if the input for birthday is valid
    if had_birthday not in ['yes', 'no']:
        print("Please answer with 'yes' or 'no'.")
        return

    had_birthday_this_year = had_birthday == 'yes'

    # Calculate the birth year
    birth_year = calculate_birth_year(age, had_birthday_this_year)

    # Output the result
    print(f"{name}, you were born in the year {birth_year}.")

if __name__ == "__main__":
    main()