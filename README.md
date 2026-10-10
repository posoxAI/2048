# 2048

[Русская версия](README.ru.md)

The sliding-tile puzzle for the browser. Slide the tiles, merge equal numbers and build a 2048 tile. Tiles run cold to hot like a heat map as they double.

**[Play in the browser](https://posoxai.github.io/2048/)**

<p>
  <img src="screenshots/day.png" width="300" alt="2048 in the light theme with the Russian interface: a game in progress with tiles from 2 to 1024, pale blue for small numbers, orange for 1024">
  <img src="screenshots/night.png" width="300" alt="The same game in the dark theme with the English interface: a red 2048 tile in the corner">
</p>

Left: the light theme with the Russian interface. Right: the dark theme with the English one.

## Rules

- Every move slides all tiles as far as they go in one direction.
- Two equal tiles that meet merge into one with their sum. A tile merges only once per move, so 2 2 2 2 becomes 4 4, not 8.
- The sum of every merge is added to the score.
- After every move a new tile appears on a free cell: a 2 nine times out of ten, otherwise a 4.
- Making a 2048 tile wins. You can keep going after it.
- The game ends when the board is full and no two neighbouring tiles are equal.

## The tiles

The colour of a tile follows its value on a heat-map scale: pale and cold blue for 2 and 4, then deeper blue, teal, green, yellow, orange, red for 2048, and magenta and violet beyond it. The small number in a tile's corner shows it as a power of two: 1024 is 2¹⁰, 2048 is 2¹¹.

## Undo

The last move can be undone, also after the game has ended. Only one move back is kept.

## Controls

- Keyboard: arrow keys or W, A, S, D. U undoes the last move.
- Phone and mouse: swipe on the board the way to go.

The board, the score, the best score and the move that can be undone are kept in the player's browser, so a reload continues the same game.

## Language

The interface is in English and Russian. It opens in Russian when Russian is among the browser's languages and in English otherwise. The RU/EN switch remembers your choice.

## How to run

The whole game is one file, `index.html`. There is no build step and there are no dependencies.

- Locally: open `index.html` in a browser.
- Online: the game is published with GitHub Pages at https://posoxai.github.io/2048/. Every commit to `main` updates it automatically.

Fonts load from Google Fonts. Without a network the game falls back to system fonts.

## Visit counter

The published page counts visits with [GoatCounter](https://www.goatcounter.com/). According to the service, it sets no cookies and stores no personal data. The counter does not run when `index.html` is opened from disk.

## Credits

The game was written by Claude, the AI assistant made by Anthropic: the logic, the tile animation, the sound and the page design.

The rules are those of 2048 by Gabriele Cirulli (2014). The colours, the power-of-two marks and the design of this version are its own.

The idea of making a browser version came from posoxAI.

## License

MIT. The full text is in [LICENSE](LICENSE).
