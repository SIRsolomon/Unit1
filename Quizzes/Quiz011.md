#quiz 011


#paper solutions


#code
```.py
def best_month():
    t = ''
    z = 6
    t = '    October2024    \nMo Tu We Th Fr Sa Su\n'
    for i in range (0, 32):
        if i == 0:
            t = t + '  '
        elif i > z:
            p = str(i)
            t = t + f'\n{p}'
            z = z + 7
        elif i > 10:
            p = str(i)
            t = t + f' {p}'
        else:
            p = str(i)
            t = t + f'  {p}'
    return t

end_code = "\033[00m"
red = "\033[0;31m"
out = best_month()
print(f'{red}{out}{end_code}')
```

##Proof of work

##Flow Chart
