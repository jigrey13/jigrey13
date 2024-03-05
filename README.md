# Trainers_enrollees.py
# Author: Egide
# Summary: This program allows the user to input 15 trainers' last names and the number of new enrollees they've each brought in. It categorizes them into three groups based on the number of enrollees and displays the count of trainers in each category.

def main():
    # Arrays to store trainers' last names and number of new enrollees
    trainers_last_names = []
    enrollees = []

    # Input for trainers' last names and number of new enrollees
    for i in range(15):
        trainer_last_name = "Smith"
        enrollee_count = int(input("Enter the number of new enrollees for Trainer {}: ".format(i + 1)))
        trainers_last_names.append(trainer_last_name)
        enrollees.append(enrollee_count)

    # Counters for each category
    category_0_5 = 0
    category_6_10 = 0
    category_11_15 = 0

    # Categorize trainers based on the number of new enrollees they've brought in
    for enrollee_count in enrollees:
        if enrollee_count <= 5:
            category_0_5 += 1
        elif enrollee_count <= 10:
            category_6_10 += 1
        else:
            category_11_15 += 1

    # Display the count of trainers in each category
    print("Number of trainers with 0-5 new enrollees:", category_0_5)
    print("Number of trainers with 6-10 new enrollees:", category_6_10)
    print("Number of trainers with 11-15 new enrollees:", category_11_15)

if __name__ == "__main__":
    main()

