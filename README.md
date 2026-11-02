# Dice Duel

Build a dice game in JavaScript using the same CodeHS commands you used in Units 2–5. Write all your code in `program.js`.

## Getting started in Codespaces

1. On this repository's page, click **Code → Codespaces → Create codespace on main**.
2. Wait for the codespace to load. `program.js` and this README open on their own.
3. A browser tab called **Dice Duel** opens. If it doesn't, open the **Ports** tab at the bottom, find port **8080**, and click the globe icon.
4. Click **Run** to run your program, and **Reset** to clear it. After saving changes to `program.js`, click **Reset** and then **Run**.

Your program's output shows in the black box beside the canvas, like the CodeHS console. Questions from `readLine` and `readInt` pop up as boxes at the top of the page.

## What your program must do

### Part 1: Welcome (2 marks)
- Ask for the player's name with `readLine`.
- Greet them by name, for example `Welcome to Dice Duel, Sam!`

### Part 2: Number of rounds (3 marks)
- Ask how many rounds to play with `readInt`.
- Use a `while` loop to keep asking until the number is from 1 to 5.

### Part 3: Play the rounds (6 marks)
- Use a `for` loop to play each round.
- Each round, roll two dice with `Randomizer.nextInt(1, 6)`.
- Print the round number, both dice and their total, for example `Round 2: 4 + 6 = 10`.
- If both dice match, print `Doubles!` and add 1 to a doubles counter.
- Keep a running total of all the rolls.

### Part 4: Final score (3 marks)
- After the loop, print the total score and the number of doubles.
- If the total score is greater than 7 × the number of rounds, print `Lucky roller!`. Otherwise, print `Better luck next time.`

### Part 5: Draw the last roll (4 marks)
- Draw two dice for the last roll on the canvas. Use a `Rectangle` for each die and a `Text` for its number.
- Colour both dice green if the last roll was doubles, and blue if it wasn't.
- Use `getWidth()` and/or `getHeight()` so that the dice are placed relative to the canvas size.

### Style (2 marks)
- Use clear variable names and consistent indenting.
- Add comments that explain each part.

**Total: 20 marks**

## Useful CodeHS commands

```javascript
let name = readLine("What is your name? ");
let rounds = readInt("How many rounds? ");
let roll = Randomizer.nextInt(1, 6);

let box = new Rectangle(80, 80);       // width, height
box.setPosition(50, 100);              // top-left corner
box.setColor(Color.blue);
add(box);

let label = new Text("6", "30pt Arial");
label.setPosition(75, 155);            // bottom-left of the text
label.setColor(Color.white);
add(label);
```

## Submitting

Your work is submitted every time you push to GitHub.

1. Click the **Source Control** icon in the left sidebar.
2. Type a short message, like `Finished part 3`, and click **Commit**. If you're asked about staging changes, click **Yes**.
3. Click **Sync Changes** to push.

Push as often as you like. The last push before the due date counts, and the automatic checks run on every push.
