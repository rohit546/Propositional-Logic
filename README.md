# Propositional-Logic


Task 1:
Propositional logic, also known as sentential logic or propositional calculus, is a branch of formal
logic that deals with propositions, which are statements that can either be true or false but not
both. Propositional logic studies how these propositions can be combined using logical operators
to form more complex statements.
The logical connectives rules, which hold for any subsentences P and Q (atomic or complex) in
any model m (here “iff” means “if and only if”):


• ¬, not: ¬P is true if and only if (iff) P is false in m. The atomic sentences P and ¬P are
referred to as literals.
• ∧, and: P ∧ B is true iff both P is true and Q is true in m. An ’and’ sentence is known as a
conjunction and its component propositions the conjuncts.
• ∨, or: P ∨ Q is true iff either P is true or Q is true in m. An ’or’ sentence is known as a
disjunction and its component propositions the disjuncts.
• ⇒, implication: P ⇒ Q is true unless P is true and Q is false in m.
• ⇔, biconditional: P ⇔ Q is true iff either both P and Q are true or both are false in m.
You can implement the following truth table by employing the capabilities of logic.py library
provide by AIMA repository
Note: For further information, check the “propositional logic” tutorial provided by Georgia
Gwinnett College
https://ggc-discrete-math.github.io/logic.html

![image](https://github.com/rohit546/Propositional-Logic/assets/100420859/a9c96bb0-5186-4bac-b167-0c47d7a4372f)

Task 2:
Inference rules are the templates for generating valid arguments. Inference rules are applied to
derive proofs in artificial intelligence, and the proof is a sequence of the conclusion that leads to
the desired goal.
Implement the inference rule to get a Conclusion from the truth table given in Task 1.
a) Example 1:
Statement 1: “The grass was wet this morning, and it didn’t rain last night” ➔ q ∧¬p
Statement 2: “it didn’t rain last night”➔ ¬p
Which infers that “The grass was not wet this morning”
b) Example 2:
Statement 1: "If I am sleepy then I go to bed" ➔ P→ Q
Statement 2: "I do not go to the bed."➔ ~Q
Conclusion: Which infers that "I am not sleepy" ➔ ?
c) Example 3:
Statement 1: I have a vanilla ice-cream. ➔ P
Statement 2: I have Chocolate ice-cream. ➔ Q.
Conclusion: Which infers that “I have vanilla or chocolate ice-cream” ➔ ?

Task 3:
Expression of Relations and Knowledge Representation
a) Implement the expression of relations and the search for values which satisfy them,
i.e. asks for a number x such that ‘x == z’ and ‘z == 10’
i). If ‘a’ is equal to ‘b’ and ‘b’ is equal to 100
What is the value of ‘a’?
b) Implement a knowledge representation that stores data as facts that state relationships
between terms. For example, the parent relationship and uses it to state facts about who is a
parent of whom within the specific family.
• Fakhir is father of Usman
• Fakhir is father of Rehan
• Noman is father of Fakhir
• Suleman is father of Noman
Find the following:
a. Who is father of Usman?
b. Children of Fakhir?
c. Who is grandfather of Usman?


d. Who is grandfather of Fakhir?

Note: You can use ‘kanren’ library for logic programming in python.
Sample Example 1:
from kanren import var, eq, run
var1 = var()
var2 = var()
# It asks for `1` number, `x`, such that `x == 5`
print("The final value of var1 is: ", run(1, var1, eq(var1, var2), eq(var2, 5)))
Sample Example 2:
from kanren import Relation, facts, run, var
var1 = var()
var2 = var()
parent = Relation()
facts(parent, ("Fakhir", "Usman"), ("Fakhir", "Rehan"), ("Noman", "Fakhir"), ("Suleman",
"Noman"))
print("The father of Usman is: ", run(1, var1, parent(var1, "Usman")))

Task 4:
Wumpus World (Proof by Resolution)
Implement, a knowledge base and an inference engine for the Wumpus world. Firstly, create
a knowledge base that stores the rules of the Wumpus world, i.e., pits, monsters, breeze, and
stench. Secondly, create an inference engine, that given a knowledge base and a statement
determines if, based on the knowledge base, the statement is definitely true, definitely false,
or of unknown truth value.
You have already studied the Wumpus World game problem. Your task is to represent the WUMPUS
WORLD by using logic.py library. You may get the aid for implementation from following notebook.
https://notebook.community/SnShine/aima-python/logic

![image](https://github.com/rohit546/Propositional-Logic/assets/100420859/4e8c25a4-8349-49d2-a7f9-454c52b1ce99)

Apply the resolution rules to find the solution to this problem.
NOTE:- Consider Section 7.4 of your book for understanding. And for Simulation purpose you may
use the following link. https://thiagodnf.github.io/wumpus-world-simulator/
