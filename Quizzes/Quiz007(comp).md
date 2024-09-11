#quiz 007


#paper solutions
![20240911_143624 1](https://github.com/user-attachments/assets/c7725cee-59f7-4b70-abf7-94e3934b4ada)


#code
```.py
  import random

length = int(input("Enter length of password"))
symbol_bool = (input("True - include symbols, False - exclude symbols"))
output = ''
chest = 'qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM1234567890'
chest2 = 'qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM1234567890!@#$%^&*()_-+={}[]:;"<>?/.'
chest_length = int(len(chest))
chest2_length = int(len(chest2))

if symbol_bool == 'True':
    for i in range (0, length):
        n = random.randint(0, chest2_length-1)
        output = output + chest2[n]
elif symbol_bool == 'False':
    for i in range (0, length):
        n = random.randint(0, chest_length-1)
        output = output + chest[n]
else:
    output = "invalid"

print(f"your password is {output}")
```

##Proof of work
<img width="1470" alt="Screenshot 2024-09-10 at 3 11 15 PM" src="https://github.com/user-attachments/assets/e9370cd4-6b9c-4ae8-a64b-987a4d24a022">
