## EX NO:07
## DATE:23.06.2022
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
```
Developed by: Vincent Isaac Jeyaraj J
Register  No:  212220230060
```
```python
from utils import *
from logic import *
wumpus_kb = PropKB()
P11,P12,P21,P22,B11,B12,B21,B22,W11,W12,W21,W22,S11,S12,S21,S22,OK11,OK12,OK21,OK22=expr('P11,P12,P21,P22,B11,B12,B21,B22,W11,W12,W21,W22,S11,S12,S21,S22,OK11,OK12,OK21,OK22')

wumpus_kb.tell(B11 | '<=>' | ((P12 | P21)))
wumpus_kb.tell(B12 | '<=>' | ((P11 | P22)))
wumpus_kb.tell(B21 | '<=>' | ((P11 | P22)))
wumpus_kb.tell(B22 | '<=>' | ((P21 | P12)))

wumpus_kb.tell(S11 | '<=>' | ((W12 | W21)))
wumpus_kb.tell(S12 | '<=>' | ((W11 | W22)))
wumpus_kb.tell(S21 | '<=>' | ((W11 | W22)))
wumpus_kb.tell(S22 | '<=>' | ((W21 | W12)))

wumpus_kb.tell(~OK11| '<=>' | ((W11 | P11)))
wumpus_kb.tell(~OK12| '<=>' | ((W12 | P12)))
wumpus_kb.tell(~OK21| '<=>' | ((W21 | P21)))
wumpus_kb.tell(~OK22| '<=>' | ((W22 | P22)))

wumpus_kb.clauses

# 1,1
wumpus_kb.tell(~P11)
wumpus_kb.tell(~W11)
wumpus_kb.tell(~S11)
wumpus_kb.tell(~B11)

# 2,1
wumpus_kb.tell(~P21)
wumpus_kb.tell(~W21)
wumpus_kb.tell(S21)
wumpus_kb.tell(~B21)

# 1,2
wumpus_kb.tell(~P12)
wumpus_kb.tell(~W12)
wumpus_kb.tell(~S12)
wumpus_kb.tell(~B12)

# 2,2
wumpus_kb.tell(~P22)
wumpus_kb.tell(~W22)
wumpus_kb.tell(~S22)
wumpus_kb.tell(~B22)

wumpus_kb.ask_if_true(OK22)

```

## OUTPUT:
### check
![image](https://user-images.githubusercontent.com/65499285/175802972-4159eb7d-8d72-44d9-9ead-6a9828558ad0.png)

## RESULT
Thus, the developed agent can predict the next move in the wumpus game using propositional logic sentences .
