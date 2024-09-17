#quiz 004


#paper solutions
![20240902_194630](https://github.com/user-attachments/assets/1d385404-3d3d-438c-ad97-755b14b6d493)


#code
```.py
input_number = input("Input number")
storage_string = ''
space = " "
total = 0
y = 0

if input_number.isdigit():
    num = int(input_number)
#factorize
    for i in range (1, num):
        if num%i ==0:
            i_str = str(i)
            storage_string = storage_string + space + i_str
    print(f"The factors are {storage_string}")

    cut_str = storage_string.split()
    x = len(cut_str)

    while y < x:
        z = cut_str[y]
        print(z)
        total += int(z)
        y = y+1

    if total == num:
        print("True")

else:
    print("Invalid")
```

##Proof of work
<img width="1470" alt="Screenshot 2024-09-02 at 7 51 24 PM" src="https://github.com/user-attachments/assets/bf94e219-c42e-461a-8b61-038a2bdaea77">

#Flowchart
![004](https://github.com/user-attachments/assets/e84c4601-509b-41fa-85d6-09c53cafeba1)
