#quiz 009


#paper solutions


#code
```.py
def scramble(scramble_victim:str)->str:
    length = len(scramble_victim)
    library = 'abcdefghijklmnopqrstuvwxyz'
    library2 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
    out = ''
    for i in range (0, length):
        if scramble_victim[i].islower():
            for n in range (0, 13):
                if library[n] == scramble_victim[i]:
                    out = out + library[n+13]
            for n in range (13, 26):
                if library[n] == scramble_victim[i]:
                    out = out + library[n-13]
        elif scramble_victim[i].isupper():
            for n in range (0, 13):
                if library2[n] == scramble_victim[i]:
                    out = out + library[n+13]
            for n in range (13, 26):
                if library2[n] == scramble_victim[i]:
                    out = out + library[n-13]
        else:
            out = out + scramble_victim[i]

    return out

output = scramble('hello world')
print(output)
```

##Proof of work

##Flow Chart
