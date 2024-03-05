# Trainers_enrollees.py
# Author: Egide
# Summary: This program takes input for 15 trainers' names and the number of new enrollees they've each brought in. It categorizes them into three groups based on the number of enrollees and displays the count of trainers in each category.

def main():
    # Arrays to store trainers' names and number of enrollees
    trainers = []
    enrollees = []

    # Input for trainers' names and number of enrollees
    for i in range(15):
        trainer_name = input("Enter Trainer {}'s last name: ".format(i + 1))
        enrollee_count = int(input("Enter the number of new enrollees for Trainer {}: ".format(i + 1)))
        trainers.append(trainer_name)
        enrollees.append(enrollee_count)

    # Counters for each category
    category_0_5 = 0
    category_6_10 = 0
    category_11_15 = 0

    # Categorize trainers based on the number of enrollees they've brought in
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

