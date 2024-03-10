---
toc: False
comments: True
layout: post
title: Individual Final CPT 
description: CSP Tri 2 Final 
courses: { compsci: {week: 18} }
type: tangibles
---

# Project Overview: 
## ByteJam: Cayden, Saaras, Eric, Sri, Austin 

Game website with multiple games of different genres. 

## My Feature: 

"Mathnopoly". A math question gets displayed each round. The User answers the math question by submitting the answer in the answer box. If the user answers the question correctly, two dice are rolled, and the user moves forward on a board based on that roll. The board has different boxes/steps with different values set to each box. The user plays against the AI, who always rolls after the users turn. Each step/box the user lands on gives or takes differing set amounts of money. The player who gets to 500$ first wins. 

[Collegeboard Requirements](https://apcentral.collegeboard.org/media/pdf/ap-csp-student-task-directions.pdf)

## Component A: Program Code 

| Requirements | Completed | 
| --------------- | -----------------| 
| Instructions for input from the user (including user actions that trigger events) | There is a math question displayed each round. The user can input the answer to the displayed math question into the interactive Answer Box. The code takes this user input, and compares it to a computer solved answer of the question displayed. If the answers are equal, the code generates a number between 2 and 12 to simulate rolling two dice. The player will move forward on the board however many steps generated.  |
| Use of at least one list (or other collection type) to represent a collection of data that is stored and used to manage program complexity and help fulfill the program’s purpose | This code assigns a specific price value to each position on the game board. Since the values on the visual board are just for show, we need to be able to access another set of values for calculations. For instance, the second item in the list (1:100) corresponds to the second box or "step" on the visual board, which is valued at 100 dollars. These values align with the visual representation of the board but are primarily used for calculations and algorithms rather than visual display purposes. When accessing to calculate how much money the player or ai earns when they land on a specific box, I call this list instead of the values used for the css display.  ![CodePic](https://media.discordapp.net/attachments/974516458300256316/1211222387861758002/list.png?ex=65ed69c0&is=65daf4c0&hm=eb9299bdf9bc6a28ebce7d5b0fe0091944633dabaff0ba6488ff250021b8f494&=&format=webp&quality=lossless&width=872&height=1306) | 
| One procedure that contributes to the program’s intended purpose, where you have defined: the procedure’s name, the return type (if necessary), one or more parameters | Procedure Name (move), parameters: token and steps.  ![CodePic](https://media.discordapp.net/attachments/974516458300256316/1211222388184973342/procedure.png?ex=65ed69c0&is=65daf4c0&hm=0a40071a28e12eae8483c4ddd97e80f6c8913b835752ff2f0427894085ddcb49&=&format=webp&quality=lossless&width=1664&height=1306) |
| An algorithm that includes sequencing, selection, and iteration that is in the body of the selected procedure | Selection: If/Else Statements. Iteration: The setTimeout function introduces a delay between actions, enabling the repetition of certain tasks over time, creating a form of iteration in the program. ![CodePic](https://media.discordapp.net/attachments/974516458300256316/1211222388474122350/calls.png?ex=65ed69c0&is=65daf4c0&hm=3f8dc064b318d2781ef69b730d51472ea75cb02080bb33863a898d5fecd0feaa&=&format=webp&quality=lossless&width=1916&height=1306) |
| Calls to your student-developed procedure | Calling move function: move() ![CodePic](https://media.discordapp.net/attachments/974516458300256316/1211222388474122350/calls.png?ex=65ed69c0&is=65daf4c0&hm=3f8dc064b318d2781ef69b730d51472ea75cb02080bb33863a898d5fecd0feaa&=&format=webp&quality=lossless&width=1916&height=1306) |
| Instructions for output (tactile, audible, visual, or ) based on input and program functionality | Textually inform user if they won/lost. Sends pop up notification to alert. ![CodePic](https://media.discordapp.net/attachments/974516458300256316/1211222388763791390/textual_output.png?ex=65ed69c0&is=65daf4c0&hm=82237624f81da02eae42c929bbbc16bad1849b7760d02e06fe660726fafac354&=&format=webp&quality=lossless&width=1544&height=752) |

## Component B: Video 

[Video Link](https://drive.google.com/file/d/1X746y5FGmSrgK0HV_eA1YVFWxJ3l1hmP/view?usp=sharing)

| Requirements | Completed | 
| --------------- | -----------------| 
| Input to your program | Y - Show Submit Answer into Answer Box |
| At least one aspect of the functionality of your program | Y - Show that Game Functions as Expected W/O Bugs |
| Output produced by your program | Y - Show Visual Movement, Display Steps Moved, Money Gained, Show Victory/Loss Notification |
| Your video may NOT contain: Any distinguishing information about yourself, Voice narration (though text captions are encouraged) | Y |
| Your video must be: Either .webm, .mp4, .wmv, .avi, or .mov format | Y - .mp4 File |
| No more than 1 minute in length | Y - 1 Minute Long |
| No more than 30MB in file size | Y - 28 MB|


