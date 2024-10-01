#quiz 0


#paper solutions


#code
```.py
def averageLength(x:list)->int:

    totalLength = len(x)
    tot = 0
    for a in x:
        b = ''
        for i in range (0, len(a)):
            if a[i] != ' ':
                b = b + a[i]
            else:
                totalLength = totalLength + 1
        tot = len(b) + tot
    avg = tot/totalLength
    return avg

test_case = [["hello", "main"], ["Peru", "France", "Nepal"], ["Computer Science", "Art"], ["one", "two"]]
for random in test_case:
    out = averageLength(random)
    print(out)
```

##Proof of work

##Flow Chart
