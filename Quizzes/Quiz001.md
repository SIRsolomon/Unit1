#quiz 001


#paper solutions
![20240821_151846](https://github.com/user-attachments/assets/57c11eaf-08a4-42b2-aabb-37274d857cda)

#code
'''.py
word = input("Enter input")
spl = word.split()
array_limit = int (len(spl))

print(spl, array_limit)

i = 0

while i < array_limit+1:
      char_count = len(spl[i]) - 2
      word = spl[i]
      index = len(spl[i]) - 1
      last_character = word[index]
      first_character = word[0]
      if char_count == 0:
             print(word)
      else:
             print(first_character, char_count, last_character)
      i = i + 1
'''

##Proof of work
