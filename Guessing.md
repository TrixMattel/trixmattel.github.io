flowchart TD
    A([Start]) --> L[/"What range do you want to guess today (edges included)? Low:__  High:__"/]
    L --"low == high"-->
    L --switch low and high if necessary--> K[Generate and store random number within correct range] --> B[/"What is your guess?"/]
    B -->I{make sure input is valid; no string in integer, float, etc.}
    I --invalid--> B
    I --valid--> J[store as different value]--> C[Check against randomly generated value]
    C --> D{Give feedback}
    D --too high--> E[/"Too high. Guess again. "/]
    D --too low--> F[/"Too low. Guess again. "/]
    D --values match--> G[/"Congrats, Tiger's proud of you!" *insert ascii image of Tiger Woods smiling*/]
    E & F --> B
    G --> H([End])



## Explanation
### Start
To start, the program will ask the user for a custom range to generate a number in. It will make sure low and high are not the same, and if so, it will prompt the same input again. If not, it will make sure low is lower than high, switching them when necessary. After that, it will generate and store a random number in the correct range (**A**). 
### User Guess
Then, it will ask the user for their guess. Once that has been input, the users input needs to be checked for the right format, and if not, the user will again be prompted for their guess. If the input is correct, it will be stored as well (**B**). **A** and **B** will be checked to see if they match. 
### Verifying Guess
If **B** is greater than **A**, the user will be told so, and the user will be told to guess again. If **B** is less than **A**, the user will be told so, and the user will be told to guess again. If they are the same, the user will be congratulated on their success and the program will end.
