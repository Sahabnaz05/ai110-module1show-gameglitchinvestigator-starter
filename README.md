# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [x] The purpose of the game is for the player to guess a randomly generated secret number within a limited number of attempts. The game gives higher or lower hints to help the player find the correct number.
- [x] I found several bugs while testing the game. The higher and lower hints were backwards, decimal guesses such as 35.9 were being accepted as whole numbers, and starting a new game did not completely reset the previous game state. I also found that the secret could be converted to a string, which caused an error when it was compared with an integer guess.
- [x] I fixed the higher and lower logic, changed the input validation so decimal guesses are rejected, and fixed the New Game button so the attempts, score, status, history, and secret number reset. I also kept the secret number as an integer and moved the game logic into `logic_utils.py` so it could be tested separately.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. Run the Streamlit app and choose a difficulty.
2. Open the Developer Debug Info section to see the secret number, attempts, score, and guess history.
3. Enter a whole number and click "Submit Guess."
4. If the guess is too high or too low, the game gives the correct "Go LOWER!" or "Go HIGHER!" hint.
5. Continue guessing until the secret number is found, or click "New Game" to reset the game and start again.
**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# =========================  3 passed in 0.02s =========================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
