# QOSF-Mentorship-Program
Hi!
Once again, thank you for your interest in the QC Mentorship program!

We decided to select participants based on how they will manage to do some simple “screening 	tasks” 

These tasks have been designed to:
- find out if you have the skills necessary to succeed in our program.
- be doable with basic QC knowledge - nothing should be too hard for you to quickly learn.
- allow you to learn some interesting concepts of QC.
- give you some choices depending on your interests.

What we mean by skills is not knowledge and expertise in QC. It’s the ability to code, learn new concepts and to meet deadlines.

What are we looking for in these applications?
Coding skills – clear, readable, well-structured code	
Communication – well-described results, easy to understand, tidy.
Reliability – submitted on time, all the points from the task description are met
Research skills – asking good questions and answering them methodically

Also, feel free to be creative – once you finish the basic version of the task, you can expand it. Bonus questions provide just some ideas on how to expand a given topic.

Choose tasks based on your interests, don’t try to pick the easiest one. 

You need to do only 1 task. Feel free to do all of them, it might be a good learning opportunity, but it won’t affect admissions to the program :)

So here are the tasks:


Task 1 Add values

For this problem, you want to find a positive integer that can be composed of the summation of a subset of the input vector, for example:
[1,3,6,4,2],   and we need to find the number 6

the possible solutions are:
- [1,3,2],
- [4,2],
- [6]
For this challenge, consider as input a vector of positive integers and a positive integer, generate a quantum circuit that indicates with higher probability the subset(s) that manage to obtain the number with their sum.
Tip consider a QRAM to save the input vector and the encoding basis, using the before example that could be, we need n qubits for the length of the vector and m qubits for the length of the bits. Consider that we will use n = 5 qubits for the address, so the state |10000⟩ represents the index 1, the state |01000⟩  represents the index 2 and so on. And m = 3, because the number we need is 6 and in binary is 110, so we can use the bases encoding and  the state  result is |110⟩
In view of the above, the following should be carried out
|index of the vector⟩|value of the index⟩
Consider this format, we  need 5 qubits for the index and 3 qubits of the values, i.e:
1 = > |10000001>
3 = > |01000011>
6 = > |00100110>
4 = > |00010100>
2 = > |00001010>
And you want to find 6. The green part is the index state, and the red is the value.
For this example, you need to find an oracle where is the state six in the  red qubits is a correct answer.
The output could be 
- [1,3,2]  = > |11001> ,
- [4,2]  = > |00011>  ,
- [6]  = > |00100> 
Hint: For this task you can make use of the Adder by Draper, a general quantum circuit to make this proposal can be found  here, but instead of adding 2 numbers find a way to accommodate the request.

Based on the diagram, the QFT and QFT-1 are used and U1 =  .  Then  the values  to be the binary number  depends on the U1 gates. Examples of this you can see in the images, consider the green cat  as |0> and purple cat as |1>. 



The challenge
Design a quantum circuit that finds the subsets where the sum is equal to the value 16 in the following vector [5,7,8,9,1]
References 
Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton (2004). A new quantum ripple-carry addition circuit. (https://arxiv.org/abs/quant-ph/0410184)
Thomas G. Draper (2000). Addition on a Quantum Computer (https://arxiv.org/abs/quant-ph/0008033)

Task 2 Encoding and Classifier


Encoding the following files in a quantum circuit mock_train_set.csv and mock_test_set.csv in at least two different ways (these could be basis, angle,  amplitude, kernel or random encoding).
Design a variational quantum circuit for each of the encodings, uses the column 4  as the target,  this is a binary class 0 and 1.
You must  use the data  from column0 to column3 for your proposed classifier. 
Consider the ansatz you are going to design as a layer and find out how many layers are necessary to reach the best performance.

Analyze and discuss the results.

Feel free to use existing frameworks (e.g. PennyLane, Qiskit) for creating and training the circuits.
This PennyLane demo can be useful: Training a quantum circuit with Pytorch, 
This Quantum Tensorflow tutorial can be useful: Training a quantum circuit with Tensorflow.

For the variational circuit, you can try any circuit you want. You can start from one with a layer of RX, RZ and CNOTs.


Task 3 Find best results

For this problem you have the following situation: you are playing a game of tic-tac-toe, and you find the situation in the figure below, next is your turn, develop a quantum algorithm to be able to find the best decisions with higher probability.

 


The following considerations apply:
You are the X's.
The matrix as a qubit and the state of the X's is |1> and of the O's is |0>, of the empty cells an unknown state.
What are the valid combinations to win?
You have at most 2 turns

A hint for this exercise should consider all the possible ways to win that (there’s 8 of them), for this exercise must obtain with probability the state with the highest probability.


for the output only give the status of the empty boxes, you consider this example: 

If you think the solution is put the values 

X | O | O 
X | X  | X
O | O | O

The state output must be |1100>




Bonus : what if we start one step earlier and your opponent has not chosen yet, as shown in the following image, it shows with higher probability the chances of you winning. Please refer to the above considerations.




Task 4 – Decompose and reduction

From the qasm 3.0 code, make a decomposition in which only the gates of the Clifford+T group remain, and then identify if the number of gates can be reduced, e.g.

What can the following quantum circuits be reduced to?





The gates you need to consider changing are RX, RY, RZ,  CCX,  and reduce them if exist the case.






Deadline
2 weeks from when you’ve submitted your application in your timezone. 
This means that if you submitted your application on February 15th, you can send your solution by midnight of March 1st.

Once you have finished a screening task, please submit your GitHub repository containing the code to this google form: https://forms.gle/T9CrU4BNAu5EyRjV8 -- other forms of submission will not be accepted! 
 
If you have any questions - please add comments to this document, or ask it in the QOSF slack workspace (invitation link) in the #mentorship-applicants channel. We will be updating this document with more details and/FAQ to avoid confusion, so make sure to check it before asking :)


Have a nice day!
QOSF team 


FAQ

Q: Can we use any quantum libraries or are we restricted to a particular set of tools?

A: Feel free to use whatever you like, just make sure that the tool doesn’t solve the whole problem for you.
Regarding the language of choice, Python is definitely the preferred one, since this is the language that most of the mentors use.
You can do the task first in the language of your preference and then translate it to Python if that’s more convenient for you.


Q: I am applying as a member of a team. How many tasks do we submit?

A: Each member of a team must submit their own screening task. This will help us judge the skill level of each individual team member and help us pair folks up with the right mentor.

Q: How should I submit the solution?

A: All the materials for the submission should be inside a GitHub repository. Please do not send us any loose files as attachments or in any other format. Please submit your GitHub repository to this google form once you’ve finished: https://forms.gle/T9CrU4BNAu5EyRjV8 
Q: My team-mate wants to leave the team because he/she/they can’t manage these along with exams. So will this affect our team status or anything like that?

A: Well, just let us know and you can continue as an individual/smaller team.

Q:  Is it possible to make more than one task and send everything together?
A: Yes, you can. But you should specify which task you want to be evaluated. In other words, do it as an exercise but it does not affect your chances to enter the program.

Q: Can I please get the slack link? I think the link has expired ?

A: try this:  https://qosf.slack.com/archives/C019UEZRCM9
Another one to try: 
https://join.slack.com/t/qosf/shared_invite/zt-vb1ftjp1-D2gpVKEfl6Ifv9oXvk_xDw





