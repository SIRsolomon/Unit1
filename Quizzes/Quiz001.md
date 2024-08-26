#quiz 001


#paper solutions
![20240821_151846](https://github.com/user-attachments/assets/57c11eaf-08a4-42b2-aabb-37274d857cda)

#code
```.py
#split inputs and count characters within them
for test_case in ['internationalization', 'localization', 'Hello world !', '98 99 100 101 1062', '(codin) + (game) = (codingame)']:
      word = test_case
      spl = word.split()
      array_limit = int (len(spl))

      print(spl, array_limit)

      i = 0

      while i < array_limit:
            char_count = len(spl[i]) - 2
            word = spl[i]
            index = len(spl[i]) - 1
            last_character = word[index]
            first_character = word[0]
            if len(spl[i]) == 1:
                  print(word)
            else:
             if char_count == 0:
                   print(word)
             else:
                   print(first_character, char_count, last_character)
            i = i + 1
```

##Proof of work
<img width="1470" alt="Screenshot 2024-08-26 at 3 20 37 PM" src="https://github.com/user-attachments/assets/dc3677ee-8fbc-464b-b521-86224f045bdf">
