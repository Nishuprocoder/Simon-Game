# Simon Game

A browser-based implementation of the classic **Simon** memory game using HTML, CSS and JavaScript (jQuery). The game lights up a sequence of colored pads and plays sounds — the player must repeat the sequence. With each successful round the sequence gets longer, testing short-term memory and concentration.

---

## Demo / Quick start

1. Make sure the project folder contains these files and folders:

   * `index.html` (your HTML file)
   * `style.css` (styling)
   * `game.js` (game logic)
   * `sounds/` (folder containing `red.mp3`, `blue.mp3`, `green.mp3`, `yellow.mp3`, `wrong.mp3`)

2. Open `index.html` in a modern browser (Chrome/Firefox/Edge). No build step required.

> Optional: If the game behaves differently when opened via `file://`, serve it with a local HTTP server (recommended):

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000
```

---

## How to play

* Press any key to start the game.
* Watch (and listen to) the sequence of coloured pads that light up.
* Repeat the sequence by clicking the pads in the same order.
* If you complete the sequence correctly the game advances to the next level and adds one more color to the sequence.
* If you make a mistake, a "wrong" sound plays and the screen briefly flashes — then press any key to restart.

---

## Project structure

```
/ (project root)
├─ index.html
├─ style.css
├─ game.js
└─ sounds/
   ├─ red.mp3
   ├─ blue.mp3
   ├─ green.mp3
   ├─ yellow.mp3
   └─ wrong.mp3
```

---

## Notes on code

* `game.js` contains the main logic:

  * `nextSequence()` builds the `gamePattern` and updates the level.
  * Player clicks are stored in `userClickedPattern` and validated by `checkAnswer()`.
  * Sounds are played with `new Audio(...)` and simple animations are applied using jQuery.
* The UI uses Google Font `Press Start 2P` via CDN and jQuery (CDN link) in `index.html`.

---

## Common issues & troubleshooting

* **No sound?** Ensure the `sounds/` folder exists and filenames match exactly (case sensitive on some OS).
* **Buttons not responding on click?** Confirm `game.js` is correctly referenced at the end of `index.html` and jQuery is loaded before it.
* **Game doesn’t start on key press:** Some browsers require the page to be focused before key events are detected — click on the page first and then press a key.

---

## Customization ideas

* Add difficulty modes (slow/fast sequence playback).
* Replace jQuery with vanilla JS for a lighter bundle.
* Add high-score persistence using `localStorage`.
* Make the layout responsive for mobile devices.

---

## Credits & assets

* Font: *Press Start 2P* — Google Fonts.
* jQuery CDN used for convenience (can be replaced by a local copy).
* Sound effects: Supply your own short `red/blue/green/yellow/wrong` sound files (or use free sound effect packs). Please ensure you have the rights to any sounds you include.

---

## License

This project is released under the **MIT License**. Feel free to fork, modify, and use it in personal projects.

---

