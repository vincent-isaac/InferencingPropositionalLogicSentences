## EX NO:07
## DATE:
# <p align="center">Inferencing Propositional Logic Sentences
  
## AIM

To develop python code to inference propositional logic sentences to solve Wumpus World problem.

## THEORY
The Wumpus World's agent is an example of a knowledge-based agent that represents Knowledge representation, reasoning , and planning. A Knowledge-Based agent links general knowledge with current percepts to infer hidden characters of the current state before selecting actions.

## DESIGN STEPS
## STEP 1:
Importing required logical and utils files.

## STEP 2:
Defining a knowledge base class with functions on a python file.

## STEP 3:
creating a new knowledge base for agent, with a function called propKB().

## STEP 4:
Mentioning the labels in the wumpus game cell for location in the function of expressions.

## STEP 5:
Using wumpus_kb.tell() to define the environment of the wumpus game.

## STEP 6:
Using propositional Logic defines the possibility of agent's next move.

## STEP 7:
Using wumpus_kb.ask_if_true() to get the result based on TRUE value.

## PROGRAM
```python
from utils import *
from logic import *
char=['P','B','W','S']
abc=''
ind=[1,2,3,4]
for i in char:
    for x in ind:
        for y in ind:
            abc= abc+(str(i)+str(x)+str(y))+','
abc= abc[0:-1]
abc
wumpus_kb = PropKB()
P11,P12,P13,P14,P21,P22,P23,P24,P31,P32,P33,P34,P41,P42,P43,P44,B11,B12,B13,B14,B21,B22,B23,B24,B31,B32,B33,B34,B41,B42,B43,B44,W11,W12,W13,W14,W21,W22,W23,W24,W31,W32,W33,W34,W41,W42,W43,W44,S11,S12,S13,S14,S21,S22,S23,S24,S31,S32,S33,S34,S41,S42,S43,S44= expr('P11,P12,P13,P14,P21,P22,P23,P24,P31,P32,P33,P34,P41,P42,P43,P44,B11,B12,B13,B14,B21,B22,B23,B24,B31,B32,B33,B34,B41,B42,B43,B44,W11,W12,W13,W14,W21,W22,W23,W24,W31,W32,W33,W34,W41,W42,W43,W44,S11,S12,S13,S14,S21,S22,S23,S24,S31,S32,S33,S34,S41,S42,S43,S44')
wumpus_kb.tell(~P11)
wumpus_kb.tell(~S11)
wumpus_kb.tell(~W11)
wumpus_kb.tell(~B11)
wumpus_kb.tell(~S12)
wumpus_kb.tell(~B12)
wumpus_kb.tell(~P12)
wumpus_kb.tell(~W12)
wumpus_kb.tell(~P13)
wumpus_kb.tell(~S13) 
wumpus_kb.tell(~W13)
wumpus_kb.tell(~B13)
wumpus_kb.tell(~S14)
wumpus_kb.tell(~B14)
wumpus_kb.tell(~P14)
wumpus_kb.tell(~W14)
wumpus_kb.clauses
wumpus_kb.ask_if_true(P21)
wumpus_kb.tell(~S24)
wumpus_kb.tell(~B24)
wumpus_kb.tell(~P24)
wumpus_kb.tell(~W24)
wumpus_kb.clauses
wumpus_kb.ask_if_true(W23)
wumpus_kb.tell(~S21)
wumpus_kb.tell(~B21)
wumpus_kb.tell(~P21)
wumpus_kb.tell(~W21)
wumpus_kb.clauses
wumpus_kb.ask_if_true(B21)
wumpus_kb.tell(~S22)
wumpus_kb.tell(~B22)
wumpus_kb.tell(~P22)
wumpus_kb.tell(~W22)
wumpus_kb.clauses
wumpus_kb.ask_if_true(B22)
wumpus_kb.tell(B34)
wumpus_kb.tell(B23)
wumpus_kb.tell(B31)
wumpus_kb.tell(B32)
wumpus_kb.tell(B44)
wumpus_kb.tell(B42)
wumpus_kb.tell(S12 | '<=>' | ((W22 | W13)))
wumpus_kb.tell(~B12 | '<=>' | ((~P22 | ~P13)))
wumpus_kb.tell(B23 | '<=>' | ((P33 | P34)))

wumpus_kb.tell(B31 | '<=>' | ((P41| P23)))
wumpus_kb.tell(B32 | '<=>' | ((P33| P42)))
wumpus_kb.tell(B34 | '<=>' | ((P33| P44)))
wumpus_kb.clauses
wumpus_kb.ask_if_true(~P41)
```

## OUTPUT:
## Checking in algorithm:
![21](https://user-images.githubusercontent.com/75235090/175758834-b2efad2d-195c-4ca9-93c7-23117c4baf08.png)
![22](https://user-images.githubusercontent.com/75235090/175758841-854bdea3-ab4f-4730-881c-4a787ad4ffc5.png)
## Propositional logic:
![23](https://user-images.githubusercontent.com/75235090/175758880-3a98ba74-2657-4bc9-9918-d50cf79c2fd2.png)
## Starting of the game:
![24](https://user-images.githubusercontent.com/75235090/175758904-9e04ae05-4c41-45d6-9587-c16d28775b64.png)
## Mid of the game:
![25](https://user-images.githubusercontent.com/75235090/175758917-a1b07f7e-0864-4ed8-9514-b881778a5331.png)
## End of the game:
![26](https://user-images.githubusercontent.com/75235090/175758937-bd118486-7374-431a-8ec3-fb71ba5e1871.png)

  ## RESULT
Thus, the developed agent can predict the next move in the wumpus game using propositional logic sentences .
