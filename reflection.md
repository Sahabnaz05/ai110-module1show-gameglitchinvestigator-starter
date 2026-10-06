# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
  The first time I ran the game, it looked like a normal number guessing game. It asked me to guess a number between 1 and 100 and showed how many attempts I had left.
- List at least two concrete bugs you noticed at the start  
  One bug I noticed was that the hints were backwards. When the secret number was 32 and I guessed 50, the game told me to “Go HIGHER!” instead of telling me to go lower. I also noticed that the New Game button did not fully reset the previous game. Another bug was that the game accepted a decimal like 35.9 and treated it as 35 instead of rejecting it.
**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|


| Secret = 32, Guess = 50 | The game should tell me to go lower | The game said "Go HIGHER!" | No console error |
| Click New Game after winning | The game should reset the previous game information | Some of the previous game state did not reset | No console error |
| Secret = 35, Guess = 35.9 | The game should reject the decimal guess | The game treated 35.9 as 35 and said "Correct!" | No console error |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
