## Overview

This section will focus on coding the mechanics of rock paper scissor in Python.

**Note:** Variable names in code are caps sensitive, should you wish to deviate from using our provided variable names, ensure that they are exactly the same throughout the entire file. Common mistakes in programming often include variable names that do not match exactly.

## Prepare Game Variables

This section will focus on setting up the variables needed for the game.

1. Import the random module

```py
import random
```

    a. This line of code imports the random module, which includes a function we will be using for the computer to randomly select rock, paper, or scissor.

2. Initialize all options

```py
options = ("rock", "paper", "scissor")
```

    a. This line of code writes all available choices in rock, paper, scissor in a tuple, where the random module will use as the pool to randomly select its choice.

3. Get player choice

```py
user_input = input("Rock, paper, or scissor? ").lower()
```

    a. This line of code pauses the program to wait for a player to type something into the terminal, while displaying the prompt "Rock, paper or scissor?".

    b. This line of code makes all letters received from the input turn to lowercase, allowing standardization of comparisons in the logic chain.

4. Get computer choice

```py
computer_choice = random.choice(options)
```

    a. This line of code randomly selects an option from the tuple initialized back in step 2.

5. Print out computer's choice

```py
print(f"Computer chooses {computer_choice}")
```

    a. This line of code lets the player know what the computer has chosen as its option.

    b. This line of code utilizes a concept known as f-strings, which is a shortcut to display program variables onto the terminal.

## Implement Logic Chain

This section will focus on implementing the logic flow that determines who wins the rock, paper, scissor game.

**WARNING:** Ensure the following steps are followed exactly as layed out. Deviation in the ordering may result in the program not working.

6. Handle invalid choices

```py
if user_input not in options:
    print("Funny error message here.")
```

    a. This line of code checks if the user input is valid choice using the tuple initialized in the previous section as the reference point.

7. Handle ties

```py
elif user_input == computer_choice:
    print("Tie!")
```

!!! note

    The "==" operator compares the value or equality between two objects. In this case, this line of code checks if the user input is the same as the computer's choice. If it is the same, then the program will print "Tie!".

1. Handle user choice of rock

```py
elif user_input == options[0] and computer_choice == options[2]:
    print("You Win!")
```

    a. This line of code checks if the computer has chosen scissor when the player input is rock, which will result in a win.

9. Handle user choice of paper

```py
elif user_input == options[1] and computer_choice == options[0]:
    print("You Win!")
```

    a. This line of code checks if the computer has chosen rock when the player input is paper, which will result in a win.

10. Handle user choice of scissor

```py
elif user_input == options[2] and computer_choice == options[1]:
    print("You Win!")
```

    a. This line of code checks if the computer has chosen paper when the player input is scissor, which will result in a win.

11. Handle lose scenario

```py
else:
    print("You Lose!")
```

    a. This line of code runs when none of the above requirements are met, which by default only happens when the player loses.

## The Final Code Snippet

If you have followed the instructions correctly, then your file should look like what is shown below

```py
import random

options = ("rock", "paper", "scissor")
user_input = input("Rock, paper, scissor? ").lower()
computer_choice = random.choice(options)
print(f"Computer chooses {computer_choice}")

if user_input not in options:
    print("Funny error message here.")
elif user_input == computer_choice:
    print("Tie!")
elif user_input == options[0] and computer_choice == options[2]:
    print("You Win!")
elif user_input == options[1] and computer_choice == options[0]:
    print("You Win!")
elif user_input == options[2] and computer_choice == options[1]:
    print("You Win!")
else:
    print("You Lose!")
```

## Running The Game

12. Save the code using CTRL + S or by clicking the File tab, then clicking on Save as shown below.
    ![notepad save](./assets/codeS11.PNG)
13. Go back to the terminal

14. Run the program
    > python rock_paper_scissor.py

**WARNING:** Ensure that you are in the directory. If you did not close the terminal from the previous section, you should still be in the proper directory. If you closed the terminal, refer back to "Setting Up Your Project" under the "Navigating Directories" section, and repeat steps 1 and 2 again until you have reached the projects folder.

15. Enjoy your game!

    a. If everything is correct, the terminal should look like the image below.

    ![terminal for game](./assets/codeS15a.png)

**Note:** If your code does not run, double check it matches exactly as shown, with extra emphasis on the indentation. Python uses indentation as its reference to know when blocks of code end and where they begin. Misaligning the indentations will result in the program working.

## Conclusion

By the end of this section, you will have successfully implemented the following concepts in Python:

-   [x] Import Python modules
-   [x] Get user input
-   [x] Generate random values
-   [x] Create logic flow

The next section will focus on uploading your project onto GitHub, click the link below.

[Uploading to GitHub](Upload%20to%20GitHub.md)
