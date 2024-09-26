```.py
#miscelaneous
end_code = "\033[00m"
red = "\033[0;31m"
cyan = "\033[0;36m"
Bold_red = "\33[1;31m"

#encryption function
def scramble(scramble_victim: str) -> str:
    length = len(scramble_victim)
    library = 'abcdefghijklmnopqrstuvwxyz'
    library2 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
    library3 = '!@#$%^&*()_<>?:"{}|+=-,./;[]|`'
    library4 = '1234567890'
    out = ''
    for i in range(0, length):
        if scramble_victim[i].isalpha():
            if scramble_victim[i].islower():
                for n in range(0, 13):
                    if library[n] == scramble_victim[i]:
                        out = out + library[n + 13]
                for n in range(13, 26):
                    if library[n] == scramble_victim[i]:
                        out = out + library[n - 13]
            elif scramble_victim[i].isupper():
                for n in range(0, 13):
                    if library2[n] == scramble_victim[i]:
                        out = out + library2[n + 13]
                for n in range(13, 26):
                    if library2[n] == scramble_victim[i]:
                        out = out + library2[n - 13]

        elif scramble_victim[i].isdigit():
            for n in range(0, 5):
                if library4[n] == scramble_victim[i]:
                    out = out + library4[n + 5]
            for n in range(5, 10):
                if library4[n] == scramble_victim[i]:
                    out = out + library4[n - 5]

        elif scramble_victim[i].isspace():
                out = out + '~'

        else:
            for n in range(0, 15):
                if library3[n] == scramble_victim[i]:
                    out = out + library3[n + 15]
            for n in range(15, 30):
                if library3[n] == scramble_victim[i]:
                    out = out + library3[n - 15]
    return out

def un_scramble(victim: str) -> str:
    length = len(victim)
    library = 'abcdefghijklmnopqrstuvwxyz'
    library2 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
    library3 = '!@#$%^&*()_<>?:"{}|+=-,./;[]|`'
    library4 = '1234567890'
    out = ''
    for i in range(0, length):
        if victim[i].isalpha():
            if victim[i].islower():
                for n in range(0, 13):
                    if library[n] == victim[i]:
                        out = out + library[n + 13]
                for n in range(13, 26):
                    if library[n] == victim[i]:
                        out = out + library[n - 13]
            elif victim[i].isupper():
                for n in range(0, 13):
                    if library2[n] == victim[i]:
                        out = out + library2[n + 13]
                for n in range(13, 26):
                    if library2[n] == victim[i]:
                        out = out + library2[n - 13]

        elif victim[i].isdigit():
            for n in range(0, 5):
                if library4[n] == victim[i]:
                    out = out + library4[n + 5]
            for n in range(5, 10):
                if library4[n] == victim[i]:
                    out = out + library4[n - 5]

        elif victim[i] == '~':
            out = out + ' '

        else:
            for n in range(0, 15):
                if library3[n] == victim[i]:
                    out = out + library3[n + 15]
            for n in range(15, 30):
                if library3[n] == victim[i]:
                    out = out + library3[n - 15]
    return out

with open('project_store.csv', mode='r') as f:
    data = f.readlines()
    catalog = {}

entrance = ''

terminate = False
while terminate == False:

    while entrance != 'Open Sesame Please >:)' and terminate == False:

        bleach = 0.01  # litres per kg
        soap = 0.05  # litres per kg
        dish_soap = 2  # ml per dish
        time = 30  # seconds per sq. meter
        wash_time = 80  # mins
        wash_and_dry = 180  # mins

        print("WELCOME To CLEANING CALCULATOR\n")
        print("Enter 1 for washing clothes\n")
        print("Enter 2 for washing dishes\n")
        print("Enter 3 for space cleaning\n")
        print("Enter 4 to leave\n")
        selection_for_calc = input("What would you like to do? :")

        # Clothes
        if selection_for_calc == '1':
            color = input("Are they white? [Enter 'y' for YES and 'n' for NO.] :")
            color = color.lower()
            if color == 'y':
                amt = input("Enter amount of clothes in KG:")
                if amt.isdigit():
                    amt = int(amt)
                    bleach_amt = amt * bleach
                    soap_amt = amt * soap
                    print(f"You need {cyan}{bleach_amt}{end_code} litres of bleach and {cyan}{soap_amt}{end_code} litres of soap\n")
                else:
                    print(f"{Bold_red}Invalid entry{end_code}\n")
            if color == 'n':
                amt = input("Enter amount of clothes in KG:")
                if amt.isdigit():
                    amt = int(amt)
                    soap_amt = amt * soap
                    print(f"You need {cyan}{soap_amt}{end_code} litres of soap\n")
                else:
                    print(f"{Bold_red}Invalid entry{end_code}\n")

        # Dishes
        elif selection_for_calc == '2':
            amt = input("How many dishes are there:")
            if amt.isdigit():
                amt = int(amt)
                dish_soap_amt = amt * dish_soap
                print(f"You need {cyan}{dish_soap_amt}{end_code} millilitres of dish soap\n")
            else:
                print(f"{Bold_red}Invalid entry{end_code}\n")

        # Area
        elif selection_for_calc == '3':
            l = input("Enter length of room in meters: ")
            w = input("Enter width of room in meters: ")
            if l.isdigit() and w.isdigit():
                l = int(l)
                w = int(w)
                area = l * w
                tot_time = area * time
                minutes = tot_time // 60
                seconds = tot_time % 60
                print(
                    f"It will take {cyan}{minutes}{end_code} minutes and {cyan}{seconds}{end_code} seconds to clean a room with an area of {area} square meters.\n")
            else:
                print(f"{Bold_red}Invalid entry{end_code}\n")

        elif selection_for_calc == '4':
            terminate = True

        elif selection_for_calc == 'Open Sesame Please >:)':
            entrance = selection_for_calc


        else:
            print(f"{Bold_red}OUT OF RANGE{end_code}\n")

#End of calculator

    else:
        if terminate == False:
            print("\n\nWelcome to password manager\n")
            print("Enter 1 to add password\n")
            print("Enter 2 to see list of passwords\n")
            print("Enter 3 to delete password\n")
            print(f"{red}Enter 4 to delete all{end_code}\n")
            print("Enter 5 to terminate\n")
            print("Enter 6 for about page\n")
            print("Enter 7 to return to calculator\n")

            selection = input("Select Menu Option--->")

            un_scrambled_data = un_scramble(str(data))

            if len(data) > 0:
                for item in un_scrambled_data:

                    data_cleaned = item.strip()
                    data_separated = un_scrambled_data.split(',')

                    name = data_separated[0]
                    password = data_separated[1]

                    catalog[name] = password

        #Selcection 1..........................................
            if selection == "1":
                check2 = input("re-enter verification password")
                if check2 == "Open Sesame Please >:)":
                    check = input(f'{cyan}Enter new name [Press X to exit, Y to add new password]{end_code}:')
                    check = check.lower()
                    if check == 'x':
                        terminate = True
                    elif check == 'y':
                        new_name = input("Enter new name :")
                        if new_name not in catalog:
                            new_password = input("enter password :")
                            compilation = f"{new_name}, {new_password}"
                            scrambled = scramble(compilation)
                            if len(data) != 0:
                                with open('project_store.csv', mode='a') as f:
                                    f.writelines(f"\n{scrambled}")
                            else:
                                with open('project_store.csv', mode='a') as f:
                                    f.writelines(f"{scrambled}")
                            print("Password saved")
                        else:
                            print(f"{Bold_red}Invalid{end_code}")
                else:
                    print(f"{Bold_red}INVALID{end_code}")

        #Selcection 2..........................................
            elif selection == "2":
                print("\nStored passwords:")
                with open('project_store.csv', mode='r') as f:
                    data = f.readlines()
                for list_of_passwords in data:
                    un_scrambled_list = un_scramble(list_of_passwords)
                    print(un_scrambled_list)

        #Selcection 3..........................................
            elif selection == "3":
                check2 = input("re-enter verification password")
                if check2 == "Open Sesame Please >:)":
                    i = 1
                    print(f"\n{cyan}Stored passwords:{end_code}")
                    with open('project_store.csv', mode='r') as f:
                        data = f.readlines()
                    for list_of_passwords in data:
                        un_scrambled_list = un_scramble(list_of_passwords)

                        print(f"{i}--{un_scrambled_list}")
                        i += 1

                    number = int(input(f"{cyan}Please enter a number to delete: {end_code}"))
                    # we will delete the item at number
                    new_data = []
                    for line_no, line in enumerate(data):
                        if number != (line_no + 1):
                            new_data.append(line)

                    with open('project_store.csv', mode='w') as file:
                        file.writelines(new_data)
                    print("Completed")
                else:
                    print("out of range")

        #Selcection 4..........................................
            elif selection == "4":
                check3 = input(f"{Bold_red}ARE YOU SURE? [yes - yes, n - no]{end_code}:")
                check3 = check3.lower()
                if check3 == "yes":
                    check4 = input("Enter verification password")
                    if check4 == "Open Sesame Please >:)":
                        new_data = []
                        with open('project_store.csv', mode='w') as file:
                            file.writelines(new_data)
                        print(f"{Bold_red}DELETED{end_code}")
                    else:
                        print("Invalid")
                else:
                    print("Why waste my time?")

        #Selcection 5..........................................
            elif selection == "5":
                print("See ya next time")
                terminate = True

        #Selection 6...........................................
            elif selection == "6":
                print("\nCode Created by: Sir. Shorn-Michael Solomon"
                      "Pycharm 2024.2.2")

        #Selcection 5..........................................
            elif selection == "7":
                entrance = ''

        #End Condition.........................................
            else:
                print ("invalid")
```
