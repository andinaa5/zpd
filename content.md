### Izveidot number guessing spēli ar Pyton programmēšanas valodu

### Dokumenta saturs

### 1.Spēles apraksts
Jautra, interesanta spēle, kas attīsta loģiku.
### 2.Spēles loģika

Dators uzmin vienu skaitli no 1 līdz 100. Talāk piedāvā spēlētāja uzminēt to skaitli utt

Spēles loģika ir labi aprakstīta šajā kodā:

```py
import random

repeat = True

while repeat:
    number = random.randint(1, 100)
    guess = 0
    tries = 0

    while guess != number:
        if guess < number:
            print("Pamēģini lielāku skaitli.")
        else:
            print("Pamēģini mazāku skaitli.")

        guess = int(input("Uzmini skaitli: "))
        tries += 1
    else:
        if tries < 3:
           print(f"WOW! Tu uzminēji pēc {tries} reizēm!")
        elif tries < 6:
            print(f"Nav slikti, tu uzminēji pēc {tries} reizēm!")
        else:
           print(f"Hmm... vajadzētu patrenēties, uzminēji pēc {tries} reizēm!")

    response = input("Vai gribi turpināt? y/n: ")

    if response== "y":
        repeat = True
    elif response == "n":
        repeat = False
        print("Paldies par spēli! Bye, bye! ")
    else:
        repeat = False
        print("Paldies par spēli! Bye, bye! ")
```

