# octordle-results

Display results of octordle game graphically or in character-based mode

## Background

Those of you who enjoy playing octordle (a variation of wordle that presents 8 wordle-like boards simultaneously with a maximum of 13 guesses permitted to solve all 8 boards) may be frustrated that the the "sharing" functions only displays the count of guesses for each board, but not the actual display of guesses as the other wordle variations display. Typically, the sharing functionality inserts something like the following into your clipboard:

<pre>
Daily Octordle #83
4️⃣🕛
🔟🕚
5️⃣6️⃣
8️⃣🕐
octordle.com
</pre>

However, what we might really want is something like the following (or perhaps some other layout like 1x8, 8x1, or 2x4):

<pre>
Board: 1    Board: 2
⬛🟨⬛⬛🟨 ⬛⬛⬛🟩⬛ 
⬛⬛⬛🟨⬛ 🟨⬛⬛⬛🟨 
🟨⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛🟨🟩⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛🟩🟩 
⬛⬛⬛⬛⬛ 🟨⬛🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛🟩 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 3    Board: 4
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
🟩⬛⬛⬛🟨 ⬛⬛⬛⬛🟨 
🟨⬛⬛⬛⬛ 🟨🟨⬛⬛⬛ 
🟨🟩⬛⬛⬛ ⬛🟨⬛⬛⬛ 
🟨⬛🟩⬛⬛ ⬛⬛🟨⬛⬛ 
🟨⬛🟩⬛⬛ ⬛🟨🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛🟨⬛⬛⬛ ⬛🟩⬛⬛🟩 
🟩🟩🟩🟩🟩 ⬛🟨🟨⬛⬛ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 5    Board: 6
⬛🟨⬛🟨🟨 ⬛⬛⬛🟩⬛ 
⬛⬛⬛⬛🟨 ⬛⬛🟨⬛🟨 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
🟩⬛⬛🟩🟩 🟩⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 🟩🟨🟩⬛⬛ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 7    Board: 8
🟨⬛⬛🟨⬛ 🟩⬛⬛⬛🟨 
⬛🟨⬛⬛⬛ ⬛🟨⬛⬛⬛ 
⬛⬛⬛⬛🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛🟩⬛ 
⬛🟩⬛⬛⬛ ⬛⬛⬛🟩⬛ 
⬛⬛⬛🟨⬛ ⬛⬛⬛⬛⬛ 
⬛🟩🟩🟩🟩 ⬛⬛🟩🟨⬛ 
🟩🟩🟩🟩🟩 ⬛⬛🟩🟨⬛ 
⬛⬛⬛⬛⬛ 🟨⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
</pre>

With a little bit of code, we can address that issue. In all cases we simply need to display the browser's debugger window using Ctrl Shift J (on Windows) or Ctrl Option J (on Mac).

## Graphical Approach

This is the easiest, but will probably require you to use some screen capture tool after performing this operation.

```js
document.querySelectorAll('div[class="letter-content"]').forEach(function (x) {
  x.innerText = "";
});
```

This has the effect of removing the text from each cell, but leaving the color behind so that you can take a screenshot and share the image without revealing your actual guesses. The resulting image after screen capture might look something like (I prefer to play octordle in widescreen mode so the screen capture reflects this layout):

![octordle results as a screen capture](/images/octordle-results.png)

## Character-based approaches

You may want or need to display your guesses in character form rather than in image form. There are several ways you can do this.

## Game boards arranged 2 columns x 4 rows

The following code, when executed in the debugger window you have opened already, will produce a a result consisting of two columns with boards 1, 2 displayed stacked above boards 3, 4 and those consequently above boards 5, 6, and finally boards 7, 8. Make sure you have refreshed the browser to restore the text, if you ran the code in the "Graphical Approach".

**Important** Any layout that has multiple columns may require adjustment to the code below to get the columns to display in an aligned manner. For example, Facebook converts tab characters to spaces, so the tab character `\t` does not align text, but instead just adds one space. Furthermore, converting a tab into multiple consecutive spaces does not work because browsers collapse consecutive spaces into one space when viewing HTML. Facebook does not allow you to use (or at least use well) the non-breaking space character so the least instrusive character that is printable is probably the period.

```js
nbsp = " ".repeat(5);
// For Facebook, use nbsp = (".".repeat(14))
nbsp = ".".repeat(14);
dictGuessToSymbol = {
  "no-match": "⬜",
  "word-match": "🟨",
  "exact-match": "🟩",
  "no-guess": "⬛",
};
results = "\n";
for (i = 1; i < 5; i++) {
  for (board = 1; board < 3; board++) {
    results += "Board: " + (board + 2 * (i - 1)) + (board < 2 ? nbsp : "");
  }
  correct_guess = [false, false];
  for (row = 1; row < 14; row++) {
    rowSymbols = "\n";
    for (board = 1; board < 3; board++) {
      if (correct_guess[board - 1]) {
        rowSymbols += dictGuessToSymbol["no-guess"].repeat(5) + " ";
      } else if (
        document
          .getElementById("board-" + (2 * (i - 1) + (board < 2 ? 1 : 2)))
          .getElementsByClassName("board-row")
          [row - 1].getElementsByClassName("letter exact-match").length > 4
      ) {
        correct_guess[board - 1] = true;
        rowSymbols += dictGuessToSymbol["exact-match"].repeat(5) + " ";
      } else {
        for (col = 1; col < 6; col++) {
          if (
            document
              .getElementById("board-" + (2 * (i - 1) + (board < 2 ? 1 : 2)))
              .getElementsByClassName("board-row")
              [row - 1].getElementsByClassName("letter")
              [col - 1].classList.contains("exact-match")
          )
            rowSymbols += dictGuessToSymbol["exact-match"];
          else if (
            document
              .getElementById("board-" + (2 * (i - 1) + (board < 2 ? 1 : 2)))
              .getElementsByClassName("board-row")
              [row - 1].getElementsByClassName("letter")
              [col - 1].classList.contains("word-match")
          )
            rowSymbols += dictGuessToSymbol["word-match"];
          else rowSymbols += dictGuessToSymbol["no-match"];
        }
        rowSymbols += " ";
      }
    }
    results += rowSymbols;
  }
  results += "\n";
}
console.log(results);
```

This produces a result similar to this:

<pre>
Board: 1.....Board: 2
🟩⬜🟨🟩🟨 ⬜🟨⬜⬜🟨 
🟨⬜⬜⬜⬜ 🟩⬜⬜🟩⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
⬜🟨⬜⬜🟩 🟨⬜⬜⬜⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜⬜🟨⬜ 🟨⬜⬜⬜🟨 
🟩⬜🟩⬜⬜ ⬜🟨🟨⬜⬜ 
🟩🟩🟩🟩🟩 ⬜🟩🟨⬜⬜ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 3.....Board: 4
⬜⬜⬜🟩⬜ 🟩🟩⬜⬜⬜ 
🟩⬜🟨⬜⬜ 🟨⬜⬜⬜⬜ 
⬜⬜⬜⬜⬜ 🟨⬜⬜⬜⬜ 
⬜🟨⬜⬜⬜ 🟨⬜⬜⬜⬜ 
⬜⬜⬜⬜⬜ 🟨⬜⬜⬜⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜🟨 
⬜⬜🟩⬜⬜ 🟩🟩🟩🟩🟩 
⬜⬜🟩🟩⬜ ⬛⬛⬛⬛⬛ 
🟩⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 5.....Board: 6
⬜🟨⬜⬜⬜ ⬜🟨🟨⬜⬜ 
🟨⬜⬜⬜⬜ ⬜⬜⬜⬜🟨 
⬜🟨⬜⬜⬜ ⬜⬜🟩⬜⬜ 
🟨⬜⬜⬜⬜ 🟨⬜🟨⬜🟨 
⬜⬜⬜⬜🟩 ⬜🟩⬜⬜⬜ 
⬜⬜⬜⬜🟨 🟩🟩🟩🟩🟩 
⬜🟨🟨⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜🟨⬜⬜ ⬛⬛⬛⬛⬛ 
🟨⬜🟩⬜⬜ ⬛⬛⬛⬛⬛ 
🟨⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 7.....Board: 8
⬜⬜⬜⬜⬜ ⬜🟨🟨🟨⬜ 
⬜⬜⬜⬜🟨 ⬜⬜⬜⬜🟨 
🟩🟨⬜🟩⬜ ⬜⬜⬜🟩⬜ 
⬜⬜🟩🟩⬜ 🟩🟩🟩🟩🟩 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
</pre>

# sedecordle-results

Similar to the solution for the octordle game above, we can extend something similar to the [sedecordle game](https://sedecordlegame.org/)

The results are normally displayed in a simple grid, something like:

<pre>
I solved this Sedecordle in 21/21 tries. Can you guess these 16 words? 

🟩🟩🟩🟩
🟩🟩🟩🟩
🟩🟩🟩🟩
🟩🟩🟩🟩

https://sedecordlegame.org?challenge=cGVhY2gsdHJhaXQscXVpZXQsZ2lhbnQsZGVuc2UsZmF1bmEsc2VwaWEsZmVtbWUsd2hlbHAsY3J1bWIsZm9saW8sc3RlaW4sZHJhcGUscGFkZHksc2lnbWEscmVidXM6ZW4
</pre>

But this obviously only show which of the 16 boards you managed to complete within the 21 tries allowed.

## Character-based solution

```js
nbsp = " ".repeat(5);
// For Facebook, use nbsp = (".".repeat(14))
nbsp = ".".repeat(14);
dictGuessToSymbol = {
  "no-match": "⬜",
  "word-match": "🟨",
  "exact-match": "🟩",
  "no-guess": "⬛",
};
results = "";
for (i = 0; i < 8; i++) {
	for (board = 0; board < 2; board++) {
		results += "Board: " + (board + 1 + (2 * (i))) + (board < 1 ? nbsp : "")
	}
	for (row = 0; row < 21; row++) {
		rowSymbols = "\n"
		for (board = 0; board < 2; board++) {
			if (document.getElementsByClassName("game_rows")[board + (2 * (i))].getElementsByClassName("Row")[row].classList.contains("Row-not-using")) {
				rowSymbols += (dictGuessToSymbol["no-guess"]).repeat(5) + " "
			} else {
				for (col = 0; col < 5; col++) {
					letr = document.getElementsByClassName("game_rows")[board + (2 * (i))].getElementsByClassName("Row")[row].getElementsByClassName("Row-letter")[col]
					if (letr.classList.contains("letter-absent")) {
						rowSymbols += dictGuessToSymbol["no-match"]
					} else if (letr.classList.contains("letter-elsewhere")) {
						rowSymbols += dictGuessToSymbol["word-match"]
					} else {
						rowSymbols += dictGuessToSymbol["exact-match"]
					}
				}
				rowSymbols += " "
			}
		}
		results += rowSymbols
	}
	results += "\n"
}
console.log(results)
```

For the above game, this produces the following output in the console:

<pre>
Board: 1......Board: 2
⬜⬜🟨⬜⬜ ⬜🟨⬜🟨⬜ 
🟨⬜⬜⬜⬜ 🟨⬜⬜🟩⬜ 
⬜⬜⬜🟨🟩 ⬜⬜⬜⬜⬜ 
⬜⬜⬜⬜🟨 ⬜⬜🟨🟨⬜ 
⬜⬜🟨⬜⬜ ⬜🟨⬜🟩⬜ 
⬜⬜🟩⬜⬜ ⬜⬜🟩⬜🟨 
⬜⬜⬜⬜🟨 ⬜🟨⬜⬜🟨 
🟩🟩🟩🟩🟩 ⬜⬜🟩⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟨🟩⬜🟩 
⬛⬛⬛⬛⬛ ⬜🟩🟩⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜🟨⬜🟩 
⬛⬛⬛⬛⬛ ⬜⬜⬜🟩🟨 
⬛⬛⬛⬛⬛ ⬜🟨⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟩⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜🟩⬜ 
⬛⬛⬛⬛⬛ ⬜🟨⬜⬜⬜ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 3......Board: 4
⬜🟨🟨⬜⬜ ⬜🟨⬜⬜🟨 
⬜🟩⬜🟨⬜ 🟨⬜⬜🟨⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
🟩🟩🟩🟨🟨 ⬜⬜🟨🟨⬜ 
⬜🟨🟨🟨⬜ ⬜🟨⬜🟨🟨 
⬜⬜⬜⬜🟨 ⬜⬜🟩⬜🟨 
⬜🟨⬜⬜⬜ ⬜🟩🟨⬜🟨 
⬜🟨⬜⬜⬜ ⬜⬜🟩⬜⬜ 
⬜🟨⬜⬜🟩 🟩🟩🟩🟩🟩 
⬜⬜⬜⬜🟨 ⬛⬛⬛⬛⬛ 
⬜🟨⬜⬜⬜ ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 5......Board: 6
🟨⬜🟨⬜🟨 ⬜⬜⬜⬜🟨 
⬜⬜🟨⬜⬜ 🟨🟨⬜⬜⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜⬜⬜🟩 ⬜🟨⬜⬜⬜ 
🟨⬜🟨⬜🟨 ⬜⬜⬜⬜🟨 
🟨⬜⬜⬜⬜ ⬜⬜🟨⬜⬜ 
🟨⬜⬜⬜⬜ ⬜⬜⬜⬜🟩 
⬜🟩⬜⬜⬜ ⬜⬜🟨⬜⬜ 
⬜⬜⬜🟨⬜ ⬜⬜🟨🟩⬜ 
🟩⬜⬜⬜🟩 ⬜⬜🟨⬜⬜ 
⬜🟩⬜⬜🟩 🟩⬜⬜⬜⬜ 
⬜⬜⬜🟨⬜ ⬜🟨⬜⬜⬜ 
🟨🟩⬜⬜⬜ ⬜⬜⬜⬜🟩 
⬜⬜⬜🟨⬜ 🟩🟩🟩🟩🟩 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 7......Board: 8
🟩⬜🟨⬜⬜ ⬜⬜🟨⬜⬜ 
🟨⬜⬜🟩⬜ ⬜⬜⬜⬜⬜ 
⬜⬜⬜🟨⬜ ⬜⬜🟩⬜⬜ 
⬜⬜🟨⬜🟨 ⬜⬜⬜⬜🟩 
🟩⬜🟨🟩⬜ ⬜⬜🟨⬜⬜ 
🟩⬜🟨⬜🟨 ⬜⬜⬜🟩⬜ 
🟩🟨⬜⬜🟩 ⬜⬜⬜🟩⬜ 
🟨🟩🟨⬜⬜ ⬜🟩⬜⬜⬜ 
⬜🟨🟨⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜🟨🟨🟨 ⬜⬜⬜⬜🟩 
⬜🟩⬜⬜⬜ 🟩🟩🟩🟩🟩 
⬜⬜🟨🟨⬜ ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 9......Board: 10
⬜⬜🟩⬜⬜ ⬜⬜⬜🟨⬜ 
⬜⬜⬜⬜⬜ ⬜🟨⬜⬜⬜ 
🟨⬜⬜🟨🟨 ⬜⬜🟨⬜⬜ 
⬜⬜⬜⬜🟨 ⬜🟨⬜⬜⬜ 
⬜⬜🟩⬜⬜ ⬜⬜⬜⬜⬜ 
⬜🟨⬜⬜⬜ ⬜⬜⬜🟩⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜🟩⬜ 
🟨🟨⬜⬜🟨 ⬜⬜⬜🟨⬜ 
⬜⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜⬜🟨🟨 ⬜🟩⬜⬜⬜ 
⬜🟨⬜⬜⬜ ⬜⬜⬜🟩⬜ 
⬜⬜⬜🟨⬜ ⬜🟨⬜⬜⬜ 
⬜🟨🟨⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜⬜⬜⬜ ⬜⬜🟩⬜⬜ 
⬜🟨⬜⬜⬜ ⬜⬜⬜⬜⬜ 
🟩🟩🟩🟩🟩 ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 11.....Board: 12
⬜⬜⬜⬜⬜ 🟩🟩🟩⬜🟩 
⬜⬜⬜🟩🟩 ⬜⬜⬜🟩⬜ 
🟨⬜⬜⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜🟨⬜⬜ ⬜⬜🟨🟨🟨 
⬜⬜⬜🟩⬜ 🟩🟩🟩🟩🟩 
⬜⬜⬜⬜🟨 ⬛⬛⬛⬛⬛ 
⬜🟨⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜🟨⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
🟩⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜🟨⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜🟩⬜ ⬛⬛⬛⬛⬛ 
🟩⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜🟨⬜ ⬛⬛⬛⬛⬛ 
⬜⬜⬜⬜⬜ ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 13.....Board: 14
⬜⬜🟨🟨⬜ ⬜⬜⬜⬜⬜ 
🟨⬜🟨⬜⬜ 🟨⬜🟩⬜⬜ 
⬜⬜⬜🟩⬜ ⬜🟨⬜🟨⬜ 
⬜⬜⬜⬜🟩 ⬜⬜⬜⬜⬜ 
⬜⬜🟨⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜🟩⬜⬜ ⬜⬜🟨⬜⬜ 
⬜⬜⬜⬜🟨 ⬜⬜⬜⬜🟨 
🟨🟨🟩⬜⬜ 🟩⬜🟨⬜⬜ 
⬜⬜🟩⬜⬜ ⬜⬜🟨⬜⬜ 
🟩🟩🟩🟩🟩 🟨⬜🟨🟨⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜🟨⬜🟨 
⬛⬛⬛⬛⬛ ⬜🟩⬜⬜⬜ 
⬛⬛⬛⬛⬛ 🟨⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜🟨 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 15.....Board: 16
🟩⬜⬜⬜⬜ 🟨⬜🟨🟨⬜ 
🟨⬜⬜🟨⬜ ⬜🟨⬜⬜⬜ 
⬜⬜🟨⬜⬜ ⬜⬜⬜⬜⬜ 
⬜⬜🟨⬜⬜ ⬜🟨⬜⬜🟨 
🟩⬜⬜🟨⬜ 🟨⬜🟨⬜⬜ 
🟩⬜🟨🟩🟨 🟨⬜⬜⬜⬜ 
🟩🟩🟩🟩🟩 🟨⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟩⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟨⬜⬜🟨 
⬛⬛⬛⬛⬛ ⬜🟩⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟨⬜🟨⬜ 
⬛⬛⬛⬛⬛ 🟨🟩⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜🟨⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟩⬜🟨⬜ 
⬛⬛⬛⬛⬛ ⬜⬜🟨⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟨🟨⬜🟨 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜⬜⬜⬜⬜ 
⬛⬛⬛⬛⬛ ⬜🟨⬜⬜⬜ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
</pre>