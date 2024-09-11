#quiz 002


#paper solutions
![20240822_141013](https://github.com/user-attachments/assets/3f53a1fc-6cd4-4b02-b2c0-7e4d6c40d39b)


#code
```.py
for test_case in ['30, 10', '30, 5', '30, -10', '200, -180', '[10, 30, 10, 20] [20, 15, 5, -6]']:

    num = test_case.replace(",","")
    num2 = num.replace("[","")
    
    spl = num2.split()

    num_of_digits = int(len(spl))
    x = int(num_of_digits)
    y = int(x / 2)

    #turning string into string of numbers (didnt work)
    #numbers_list1 = [char for char in spl[0] if char.isdigit()]
    #numbers_list2 = [char for char in spl[y] if char.isdigit()]
    #numbers1 = ''.join(numbers_list1)
    #numbers2 = ''.join(numbers_list2)

    #test
    numbers1 = int(spl[0])
    numbers2 = int(spl[y])

    #turning string to int
    Numbers1 = int(numbers1)
    Numbers2 = int(numbers2)

    #final check
    total1 = Numbers1 + Numbers2

    if Numbers1 == 20:
        print("true")
    elif Numbers2 == 20:
        print("true")
    elif total1 == 20:
        print("true")
    else:
        print("false")
```

##Proof of work
<img width="1470" alt="Screenshot 2024-08-27 at 9 23 17 AM" src="https://github.com/user-attachments/assets/ecd0e7c4-d797-461a-8513-8463e7b74262">
