import random

dollar = 1.00
quarter = .25
dime = .10
nickel = .05
penny = .01


def main():

    calculating = True

    total_bill = round(random.uniform(11, 95), 2)

    print(f"Hello, your total is: ${total_bill:.2f}\n")

    while calculating:

        amount_given = input("How much cash will you be paying with today? Type Here: ")

        if amount_given.isdigit():

            change = round(float(amount_given) - float(total_bill), 2)

            print(f"Your change is {change:.2f}.\n")

            dollar_calculated = calculate_dollars(change)
            quarter_calculated = calculate_quarters(dollar_calculated[0])
            dime_calculated = calculate_dimes(quarter_calculated[0])
            nickel_calculated = calculate_nickels(dime_calculated[0])
            penny_calculated = calculate_pennies(nickel_calculated[0])

            print_change(dollar_calculated[1], quarter_calculated[1], dime_calculated[1], nickel_calculated[1], penny_calculated[1])

            if change < 0:
                print("\nYou still owe them money!")

            calculating = False

        else:
            print("Please type a number. \n")


def calculate_dollars(change):

    if change / dollar >= 1:
        amount_dollars = int(change / dollar)
        change = round(change % dollar, 2)

    else:
        amount_dollars = int(0)

    return change, amount_dollars


def calculate_quarters(change):

    if change / quarter >= 1:
        amount_quarters = int(change / quarter)
        change = round(change % quarter, 2)

    else:
        amount_quarters = int(0)

    return change, amount_quarters


def calculate_dimes(change):

    if change / dime >= 1:
        amount_dimes = int(change / dime)
        change = round(change % dime, 2)

    else:
        amount_dimes = int(0)

    return change, amount_dimes


def calculate_nickels(change):

    if change / nickel >= 1:
        amount_nickels = int(change / nickel)
        change = round(change % nickel, 2)

    else:
        amount_nickels = int(0)

    return change, amount_nickels


def calculate_pennies(change):

    if change / penny >= 1:
        amount_pennies = int(change / penny)
        change = round(change % penny, 2)

    else:
        amount_pennies = int(0)

    return change, amount_pennies


def print_change(dollars, quarters, dimes, nickels, pennies):

    print(f"{dollars} dollars.")
    print(f"{quarters} quarters.")
    print(f"{dimes} dimes.")
    print(f"{nickels} nickels.")
    print(f"{pennies} pennies.")


main()
