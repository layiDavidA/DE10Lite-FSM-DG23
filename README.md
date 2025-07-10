# FSM-DG23

Top Level Quartus Schematic [split into sections]
Inputs:
<img width="629" alt="Screenshot 2025-07-09 at 10 11 43 PM" src="https://github.com/user-attachments/assets/cd04117a-8d64-4336-9c01-39c7ec31311d" />


State Equations:
<img width="709" alt="Screenshot 2025-07-09 at 10 12 04 PM" src="https://github.com/user-attachments/assets/dd93efac-2c0c-448a-8289-cbd9c21789b7" />

Dice Rolling:
<img width="620" alt="Screenshot 2025-07-09 at 10 12 19 PM" src="https://github.com/user-attachments/assets/e0fadd6d-7bf4-4eff-97c8-69d3a8d7df04" />

Counter:
<img width="628" alt="Screenshot 2025-07-09 at 10 12 34 PM" src="https://github.com/user-attachments/assets/017c5990-50bd-4584-b30b-03789271232b" />

Adder and Score Combo Logic:
<img width="621" alt="Screenshot 2025-07-09 at 10 12 51 PM" src="https://github.com/user-attachments/assets/7113d91b-a595-4657-951c-838adcaab530" />

Reg5:
<img width="626" alt="Screenshot 2025-07-09 at 10 13 03 PM" src="https://github.com/user-attachments/assets/313e1347-c873-42bc-95f3-a26070bff1f9" />

Reg4:
<img width="625" alt="Screenshot 2025-07-09 at 10 13 19 PM" src="https://github.com/user-attachments/assets/cb6b8d31-6f66-4388-9486-c2587b959a6d" />




how and why you chose the state assignment encoding that you did?
For this lab, I chose to use the recommended state assignments of one-hot encoding. One-hot encoding allows a single active bit per state, simplifies combinational logic, improves speed, and makes debugging easier. One-hot encoding also allowed us to look at the flow diagram provided in lab 6 and obtain our state equations directly from there.

what happens if the Add and Pass switches are both activated simultaneously after a roll? Explain how this is implemented in your design?
Based on my design, if the add and pass switches are both activated simultaneously after a roll, the game will automatically reject the score, but if you roll a six, the game will add the six. This is implemented in our design through our state equations. We roll the dice, and then from there, the game checks if a six is rolled. If both switches are up and a six is rolled, we automatically go into State E, which is the state where we add the score. If both switches are up and a six is not rolled, then we automatically enter State C, which passes the dice value, and then the game enters a state to reroll for another dice value.

What is one new feature you would add if you had more time?
If I had time to implement a new feature, I would add a 3-second timer that the player would have to reject or add their score. If the timer went off, then it would automatically add their dice value rolled to their score no matter what.

Conclusion
I learned how to design an FSM for a dice game using digital logic components and one-hot encoding for simplified control logic. In this lab, I used combo logic for score calculation and also handled different inputs (debounced vs. bouncing switches). I also debugged using LEDs and simulations. This lab was very challenging, but I learned a lot about FSM and state transitions.
