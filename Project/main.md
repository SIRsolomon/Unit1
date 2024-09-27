# Project Unit 1

## Criterion A: Planning

### Problem Definition

#### The local advisor, the manager of a stop and clean team, has requested help with developing some software. His faithful emplyees have been struck with the strife of having to cope with inadquate software. In they passed they have used pen and paper to store their password for sensitive documents and private content but, this presents multipile limtiations such as being vulnerable to loss, destruction, theft, fire, ligtning, water, termites, a child, and most importantly rival local espionage operations. Unfortunately, a rival team has discovered their methods and began stealing their passwords in covert local espionage operations in order to gain access to their sensitive documents and private content, which included, recipies, cleaning techniques, images, more passwords, videos, text messages, reciepts, safe codes, medical documents, academic transcripts, maps, financial records, family locations, employee bathroom time records, CCTV footage.

### Proposed Solution

The proposed solution is to make a program which has a primary purpose as a front end and a secondary purpose hidden behind it in order to keep the passwords hidden and secure while the file wiht passwords will be stored separately and securely using encryption.

### Success Criteria

####
1. A basic calculator will act as the front end of the program with simple functions such as finding amount of cleaning products needed for different scenaios, for example amount of soap for plates or a load of laundry etc.
2. If the user enters the secred ("Open Sesame Please >:)"), the program will change modes and act as a password manager.
3. In password manager mode, the user should be able to perform CRUD operations (Create, Replace, Update, Delete):
   - Add password (for example, for a website).
   - Vew the stored passwords (only if they re-enter the secret code)
4. Save passwords permanantly and securely using external files and encription tools.
5. Use the terminal to interact with the user.

## Criterion B: Design

### System Diagram
![Comp sci project 1 systems diagram (1)](https://github.com/user-attachments/assets/0a51abe4-0786-47e2-aad8-7c1ee820f7d0)

### Flow Diagrams for Algorithm
![image](https://github.com/user-attachments/assets/6132600f-2bd0-43ec-80de-722c38c662ad)

### Data storage

Global Variables:
1. end_code: str
2. red: str
3. cyan: str
4. Bold_red: str

In scramble(scramble_victim: str) -> str function:
1. scramble_victim: str
2. length: int
3. library: str
4. library2: str
5. library3: str
6. library4: str
7. out: str
8. i: int
9. n: int

In un_scramble(victim: str) -> str function:
1. victim: str
2. length: int
3. library: str
4. library2: str
5. library3: str
6. library4: str
7. out: str
8. i: int
9. n: int

In the while loop (calculator section):
1. bleach: float
2. soap: float
3. dish_soap: int
4. time: int
5. wash_time: int
6. wash_and_dry: int
7. selection_for_calc: str
8. color: str
9. amt: int or str (depending on if it's converted or not)
10. bleach_amt: float
11. soap_amt: float
12. dish_soap_amt: int
13. l: int or str (depending on if it's converted or not)
14. w: int or str (depending on if it's converted or not)
15. area: int
16. tot_time: int
17. minutes: int
18. seconds: int
19. terminate: bool
20. entrance: str

In the password manager section:
1. data: list[str]
2. catalog: dict[str, str]
3. selection: str
4. un_scrambled_data: str
5. data_cleaned: str
6. data_separated: list[str]
7. name: str
8. password: str
9. check2: str
10. check: str
11. new_name: str
12. new_password: str
13. compilation: str
14. scrambled: str
15. list_of_passwords: str
16. un_scrambled_list: str
17. i: int
18. number: int
19. new_data: list[str]
20. check3: str
21. check4: str

### Test Plan
| Test NO |      Type of test     |              Area tested              |                                                        Outcome of test                                                        | Time estimate | Target completion date | Criterion |
|:-------:|:---------------------:|:-------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|:-------------:|:----------------------:|:---------:|
| 1       | Functionality Testing | Cleaning Calculator                   | Ensuring the calculator works as intended even in extreme cases.                                                              | 10 minutes    | Sept 15th              | B         |
| 2       | Functionality Testing | Password Manager                      | Testing ability to read and write to the storage file.                                                                        | 10 minutes    | Sept 16th              | B         |
| 3       | Functionality Testing | Password Manager                      | Testing encryption and decryption functions.                                                                                  | 10 minutes    | Sept 17th              | B         |
| 4       | Functionality Testing | Password Manager                      | Finding the ideal method to iterate the program and open the password manager function.                                       | 1 hour        | Sept 19th              | B         |
| 5       | Functionality Testing | Password Manager                      | Successfully having the print all function that works.                                                                        | 30 minutes    | Sept 20th              | B         |
| 6       | Functionality Testing | Password Manager                      | Having the ability to delete individual passwords as well as all to provide the user with options.                            | 20 minutes    | Sept 21st              | B         |
| 7       | Functionality Testing | Password Manager/ Cleaning Calculator | Having an about page and terminate functions in both the password manager and calculator so the user can exit when they want. | 10 minutes    | Sept 22nd              | B         |
| 8       | Functionality Testing | Password Manager/ Cleaning Calculator | Allowing the ability to return to the calculator from the password manager.                                                   | 5 minutes     | Sept 23rd              | B         |
| 9       | Functionality Testing | Entire program                        | Ensuring that all functions within the program work together and debugging any issues which appear.                           | 20 minutes    | Sept 25th              | B         |

## Record of Tasks 
| TasK Number | Planned Action           | Planned Outcome                                               | Time Estimated | Target Completion Date | Criterion |
|-------------|--------------------------|---------------------------------------------------------------|----------------|------------------------|-----------|
| 1           | Meet client              | Get a problem definition and discuss initial proposal         | 1 hour         | Sept 11th              | A         |
| 2           | Brainstorm               | Brainstorm and come up with solution and success criteria     | 1 hour 10 mins | Sept 12th              | A         |
| 3           | Meet client              | Show solution and succes criteria and get approval for design | 20 minutes     | Sept 12th              | A         |
| 4           | Systems diagram          | Design of systems diagram                                     | 30 minutes     | Sept 13th              | B         |
| 5           | Flowchart design         | Creating the flowchart for the program                        | 3 hours        | Sept 15th              | B         |
| 6           | Code design              | Writing code                                                  | 1 week         | Sept 25th              | B         |
| 7           | Prototype presentation   | Presenting Prototype                                          | 20 minutes     | Sept 25th              | B         |
| 8           | Finalization of Project  | Completion and Presentation of Project to client              | 10 minutes     | September 27th         | B         |

###Sources
- Reddit
