# octordle-results
Display results of octordle game graphically or in character-based mode

## Background
Those of you who enjoy playing octordle (a variation of wordle that presents 8 wordle-like boards simultaneously with a maximum of 13 guesses permitted to solve all 8 boards) may be frustrated that the the "sharing" functions only displays the count of guesses for each board, but not the actual display of guesses as the other wordle variations display. Typically, the sharing functionality /inserts something like the following into your clipboard:

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
document.querySelectorAll('td[id^="box"][class="box button"]').forEach(function (x) {x.innerText = ''})
```

This has the effect of removing the text from each cell, but leaving the color behind so that you can take a screenshot and share the image without revealing your actual guesses. The resulting image after screen capture might look something like (I prefer to play octordle in widescreen mode so the screen capture reflects this layout):

![octordle results as a screen capture](/images/octordle-results.png)

## Character-based approaches

You may want or need to display your guesses in character form raterh than in image form. There are several ways you can do this.

## Game boards arranged 1 column x 8 rows

The following code, when executed in the debugger window you have opened already, will produce a single column results with each of the 8 boards displayed stacked one on top of the other. Make sure you have refreshed the browser to restore the text, if you ran the code in the "Graphical Approach".

```js
results = ""
dictGuessToSymbol = {"rgb(24, 26, 27)":"⬛", "rgb(255, 204, 0)":"🟨", "rgb(0, 204, 136)":"🟩"}
for (board = 1; board < 9; board++) {
	results += "\nBoard: " + board;
	for (row = 1; row < 14; row++) {
		rowSymbols = "\n"
		for (col = 1; col < 6; col++) {
			rowSymbols += dictGuessToSymbol[document.getElementById("box"+board+","+row+","+col+",").style["background-color"]]
		}
		results += rowSymbols
	}
}
console.log(results)
```

This produces a result similar to this:

<pre>
Board: 1
⬛🟨⬛⬛🟨
⬛⬛⬛🟨⬛
🟨⬛⬛⬛⬛
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 2
⬛⬛⬛🟩⬛
🟨⬛⬛⬛🟨
⬛🟨⬛⬛⬛
⬛⬛⬛⬛⬛
⬛🟨🟨⬛⬛
⬛⬛🟨🟩⬛
⬛🟨⬛⬛⬛
⬛🟨⬛⬛⬛
⬛🟨⬛🟩🟩
🟨⬛🟨⬛⬛
⬛🟨⬛⬛🟩
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
Board: 3
⬛⬛⬛⬛⬛
🟩⬛⬛⬛🟨
🟨⬛⬛⬛⬛
🟨🟩⬛⬛⬛
🟨⬛🟩⬛⬛
🟨⬛🟩⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛🟨⬛⬛⬛
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 4
⬛⬛⬛⬛⬛
⬛⬛⬛⬛🟨
🟨🟨⬛⬛⬛
⬛🟨⬛⬛⬛
⬛⬛🟨⬛⬛
⬛🟨🟨⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛🟩⬛⬛🟩
⬛🟨🟨⬛⬛
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 5
⬛🟨⬛🟨🟨
⬛⬛⬛⬛🟨
⬛⬛⬛⬛⬛
🟩⬛⬛🟩🟩
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 6
⬛⬛⬛🟩⬛
⬛⬛🟨⬛🟨
⬛⬛⬛⬛⬛
🟩⬛⬛⬛⬛
🟩🟨🟩⬛⬛
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 7
🟨⬛⬛🟨⬛
⬛🟨⬛⬛⬛
⬛⬛⬛⬛🟩
⬛⬛⬛⬛⬛
⬛🟩⬛⬛⬛
⬛⬛⬛🟨⬛
⬛🟩🟩🟩🟩
🟩🟩🟩🟩🟩
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
Board: 8
🟩⬛⬛⬛🟨
⬛🟨⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛🟩⬛
⬛⬛⬛🟩⬛
⬛⬛⬛⬛⬛
⬛⬛🟩🟨⬛
⬛⬛🟩🟨⬛
🟨⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
⬛⬛⬛⬛⬛
🟩🟩🟩🟩🟩
</pre>

## Game boards arranged 2 columns x 4 rows

The following code, when executed in the debugger window you have opened already, will produce a a result consisting of two columns with boards 1 through 4 displayed stacked above boards 5 through 8. Make sure you have refreshed the browser to restore the text, if you ran the code in the "Graphical Approach".

**Important** Any layout that has multiple columns may require adjustment to the code below to get the columns to display in an aligned manner. For example, Facebook converts tab characters to spaces, so the tab character ```\t``` does not align text, but instead just adds one space. Furthermore, converting a tab into multiple consecutive spaces does not work because browsers collapse consecutive spaces into one space when viewing HTML. Facebook does not allow you to use (or at least use well) the non-breaking space character so the least instrusive character that is printable is probably the period.

```js
nbsp = (" ".repeat(5))
// For Facebook, use nbsp = (".".repeat(14))
dictGuessToSymbol = {"rgb(24, 26, 27)":"⬛", "rgb(255, 204, 0)":"🟨", "rgb(0, 204, 136)":"🟩"}
results = "\n"
for (i = 1; i < 5; i++) {
	for (board = 1; board < 3; board++) {
		results += "Board: " + (board + (2 * (i-1))) + (board < 2 ? nbsp : "")
	}
	for (row = 1; row < 14; row++) {
		rowSymbols = "\n"
		for (board = 1; board < 3; board++) {
			for (col = 1; col < 6; col++) {
				rowSymbols += dictGuessToSymbol[document.getElementById("box"+(board + (2 * (i-1)))+","+row+","+col+",").style["background-color"]]
			}
			rowSymbols += " "
		}
		results += rowSymbols
	}
	results += "\n"
}
console.log(results)
```

This produces a result similar to this:

<pre>
Board: 1     Board: 2
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
Board: 3     Board: 4
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
Board: 5     Board: 6
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
Board: 7     Board: 8
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

## Game boards arranged 4 columns x 2 rows

```js
nbsp = (" ".repeat(5))
// For Facebook, use nbsp = (".".repeat(14))
dictGuessToSymbol = {"rgb(24, 26, 27)":"⬛", "rgb(255, 204, 0)":"🟨", "rgb(0, 204, 136)":"🟩"}
results = "\n"
for (i = 1; i < 3; i++) {
	for (board = 1; board < 5; board++) {
		results += "Board: " + (board + (2 * (i-1))) + (board < 4 ? nbsp : "")
	}
	for (row = 1; row < 14; row++) {
		rowSymbols = "\n"
		for (board = 1; board < 5; board++) {
			for (col = 1; col < 6; col++) {
				rowSymbols += dictGuessToSymbol[document.getElementById("box"+(board + (2 * (i-1)))+","+row+","+col+",").style["background-color"]]
			}
			rowSymbols += " "
		}
		results += rowSymbols
	}
	results += "\n"
}
console.log(results)
```

This produces a result similar to this:

<pre>
Board: 1     Board: 2     Board: 3     Board: 4
⬛🟨⬛⬛🟨 ⬛⬛⬛🟩⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛🟨⬛ 🟨⬛⬛⬛🟨 🟩⬛⬛⬛🟨 ⬛⬛⬛⬛🟨 
🟨⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ 🟨⬛⬛⬛⬛ 🟨🟨⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ 🟨🟩⬛⬛⬛ ⬛🟨⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨🟨⬛⬛ 🟨⬛🟩⬛⬛ ⬛⬛🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛🟨🟩⬛ 🟨⬛🟩⬛⬛ ⬛🟨🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛🟩🟩 ⬛🟨⬛⬛⬛ ⬛🟩⬛⬛🟩 
⬛⬛⬛⬛⬛ 🟨⬛🟨⬛⬛ 🟩🟩🟩🟩🟩 ⬛🟨🟨⬛⬛ 
⬛⬛⬛⬛⬛ ⬛🟨⬛⬛🟩 ⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
Board: 3     Board: 4     Board: 5     Board: 6
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛🟨⬛🟨🟨 ⬛⬛⬛🟩⬛ 
🟩⬛⬛⬛🟨 ⬛⬛⬛⬛🟨 ⬛⬛⬛⬛🟨 ⬛⬛🟨⬛🟨 
🟨⬛⬛⬛⬛ 🟨🟨⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
🟨🟩⬛⬛⬛ ⬛🟨⬛⬛⬛ 🟩⬛⬛🟩🟩 🟩⬛⬛⬛⬛ 
🟨⬛🟩⬛⬛ ⬛⬛🟨⬛⬛ 🟩🟩🟩🟩🟩 🟩🟨🟩⬛⬛ 
🟨⬛🟩⬛⬛ ⬛🟨🟨⬛⬛ ⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛🟨⬛⬛⬛ ⬛🟩⬛⬛🟩 ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
🟩🟩🟩🟩🟩 ⬛🟨🟨⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ 🟩🟩🟩🟩🟩 ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ ⬛⬛⬛⬛⬛ 
</pre>

## Game boards arranged 8 columns x 1 row

The following code, when executed in the debugger window you have opened already, will produce a result consisting of single row with each of the 8 boards displayed stacked side by side for 8 columns. In reality, this has little practical approach since the output produced is typically too wide to be used on social media sites.

```js
tabchar = "\t"
// For Facebook, use tabchar = (".".repeat(14))
dictGuessToSymbol = {"rgb(24, 26, 27)":"⬛", "rgb(255, 204, 0)":"🟨", "rgb(0, 204, 136)":"🟩"}
results = "Board: 1\tBoard: 2\tBoard: 3\tBoard: 4\tBoard: 5\tBoard: 6\tBoard: 7\tBoard: 8"
for (row = 1; row < 14; row++) {
	rowSymbols = "\n"
	for (board = 1; board < 9; board++) {
		for (col = 1; col < 6; col++) {
			rowSymbols += dictGuessToSymbol[document.getElementById("box"+board+","+row+","+col+",").style["background-color"]]
		}
		rowSymbols += " "
	}
	results += rowSymbols
}
console.log(results)
```

This produces a result similar to this:

<pre>
Board: 1	Board: 2	Board: 3	Board: 4	Board: 5	Board: 6	Board: 7	Board: 8
⬛🟨⬛⬛🟨	⬛⬛⬛🟩⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛🟨⬛🟨🟨	⬛⬛⬛🟩⬛	🟨⬛⬛🟨⬛	🟩⬛⬛⬛🟨	
⬛⬛⬛🟨⬛	🟨⬛⬛⬛🟨	🟩⬛⬛⬛🟨	⬛⬛⬛⬛🟨	⬛⬛⬛⬛🟨	⬛⬛🟨⬛🟨	⬛🟨⬛⬛⬛	⬛🟨⬛⬛⬛	
🟨⬛⬛⬛⬛	⬛🟨⬛⬛⬛	🟨⬛⬛⬛⬛	🟨🟨⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛🟩	⬛⬛⬛⬛⬛	
🟩🟩🟩🟩🟩	⬛⬛⬛⬛⬛	🟨🟩⬛⬛⬛	⬛🟨⬛⬛⬛	🟩⬛⬛🟩🟩	🟩⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛🟩⬛	
⬛⬛⬛⬛⬛	⬛🟨🟨⬛⬛	🟨⬛🟩⬛⬛	⬛⬛🟨⬛⬛	🟩🟩🟩🟩🟩	🟩🟨🟩⬛⬛	⬛🟩⬛⬛⬛	⬛⬛⬛🟩⬛	
⬛⬛⬛⬛⬛	⬛⬛🟨🟩⬛	🟨⬛🟩⬛⬛	⬛🟨🟨⬛⬛	⬛⬛⬛⬛⬛	🟩🟩🟩🟩🟩	⬛⬛⬛🟨⬛	⬛⬛⬛⬛⬛	
⬛⬛⬛⬛⬛	⬛🟨⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛🟩🟩🟩🟩	⬛⬛🟩🟨⬛	
⬛⬛⬛⬛⬛	⬛🟨⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	🟩🟩🟩🟩🟩	⬛⬛🟩🟨⬛	
⬛⬛⬛⬛⬛	⬛🟨⬛🟩🟩	⬛🟨⬛⬛⬛	⬛🟩⬛⬛🟩	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	🟨⬛⬛⬛⬛	
⬛⬛⬛⬛⬛	🟨⬛🟨⬛⬛	🟩🟩🟩🟩🟩	⬛🟨🟨⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	
⬛⬛⬛⬛⬛	⬛🟨⬛⬛🟩	⬛⬛⬛⬛⬛	🟩🟩🟩🟩🟩	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	
⬛⬛⬛⬛⬛	🟩🟩🟩🟩🟩	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	
⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	⬛⬛⬛⬛⬛	🟩🟩🟩🟩🟩
</pre>
