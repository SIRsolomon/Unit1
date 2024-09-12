#quiz 005


#paper solutions
![20240911_143700 1](https://github.com/user-attachments/assets/b25aa18c-466e-473f-9edd-3b198b8c428f)


#code
```.py
check_a = 'abcdefghijklmnopqrstuvwxyz'
check_b = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'

for text in ['Math','maTH','Hello world','Computer SCIENCE']:
    l = len(text)
    total = 0
    for i in range (0, l):
        if text[i] in check_a:
            for x in range (0, 26):
                if text[i] == check_a[x]:
                    total = total + x + 1
        elif text[i] in check_b:
            for x in range (0, 26):
                if text[i] == check_b[x]:
                    total = total + x + 1
        elif text[i] == ' ':
            total = total - 32
    print(total)
```

##Proof of work
<img width="1470" alt="Screenshot 2024-09-12 at 9 51 12 AM" src="https://github.com/user-attachments/assets/737d1142-ae1f-4ed0-ae2b-ed43c465d853">
