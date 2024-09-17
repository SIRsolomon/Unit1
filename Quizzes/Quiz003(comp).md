#quiz 003


#paper solutions
![20240902_194641](https://github.com/user-attachments/assets/54bead0b-5aa4-4caf-8e08-a97658d9467f)


#code
```.py
in_protein = input("Enter protein")
length = len(in_protein)
out_protein = ''
let_g = 'G'
let_a = 'A'
let_t = 'T'
let_c = 'C'
for i in range (0, length):
    if in_protein[i] == "A":
        out_protein = out_protein + let_t
    elif in_protein[i] == "G":
        out_protein = out_protein + let_c
    elif in_protein[i] == "T":
        out_protein = out_protein + let_a
    elif in_protein[i] == "C":
        out_protein = out_protein + let_g

print(out_protein)
```

##Proof of work
<img width="1470" alt="Screenshot 2024-09-02 at 7 51 06 PM" src="https://github.com/user-attachments/assets/d3954fe4-a15e-4a7d-baed-5a926687587b">

#Flowchart
![003](https://github.com/user-attachments/assets/dfde8156-8da9-48ff-8dcc-f857c235862e)
