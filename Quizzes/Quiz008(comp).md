#quiz 008


#paper solutions
![20240911_151800 1](https://github.com/user-attachments/assets/e790f251-c137-4cfe-a522-cd7c01450294)
![20240911_151805 1](https://github.com/user-attachments/assets/6e77351f-7585-47ee-94c4-b0071839b4df)


#code
```.py
def print_all():
    t = ''
    for i in range (1,101):
        if i == 100:
            t = t + '100-Room 10F10'
        else:
            floor = i//10
            room = i - (floor*10)
            t = t + f'{i}-Room {floor+1}F{room:02d}\n'
    return t

x = input("Enter room number")
if x.isdigit():
    x = int(x)
    if x == 100:
        out = '100-Room 10F10'
    else:
        floor = x // 10
        room = x - (floor * 10)
        out = f'{x}-Room {floor + 1}F{room:02d}\n'
print(out)
print('############################\n')

out = print_all()
print(out)
```

##Proof of work
<img width="1470" alt="Screenshot 2024-09-11 at 11 25 19 PM" src="https://github.com/user-attachments/assets/05133677-f6d5-4073-8f64-51d99c9e5776">
