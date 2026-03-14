# Word Stacks

An Android word puzzle game where two words are scrambled together into a single stack of letter tiles. Drag and drop tiles into the correct slots to unscramble both words.

## How It Works

1. Press **Start** to begin a new round
2. Two random 5-letter words are interleaved into a single shuffled sequence
3. Letter tiles appear one at a time on a stack — drag each tile into the **Word 1** or **Word 2** row
4. Once all tiles are placed, the original words are revealed
5. Use **Undo** to move the last placed tile back onto the stack

The scrambling algorithm randomly interleaves characters from both words while preserving their relative order, then reverses the result so the stack pops letters in the correct sequence.

## Screenshots

<p align="center">
  <img src="screenshots/Screenshot_1563710502.png" width="250" />
  <img src="screenshots/Screenshot_1563710511.png" width="250" />
  <img src="screenshots/Screenshot_1563710528.png" width="250" />
</p>

## 🛠 Tech Stack

| Component | Technology |
|-----------|-----------|
| 📱 Platform | Android (minSdk 24, targetSdk 34) |
| ☕ Language | Java |
| 🏗️ UI | XML Layouts with Drag & Drop API |
| 📦 Dependencies | AndroidX AppCompat, Material Components |
| 🔧 Build | Gradle 7.5 / AGP 7.4.2 |

## Getting Started

```bash
git clone https://github.com/stabgan/Word-Stacks.git
```

Open the project in Android Studio (Flamingo or later recommended), sync Gradle, and run on a device or emulator with API 24+.

## Project Structure

```
app/src/main/
├── java/com/google/engedu/wordstack/
│   ├── MainActivity.java      # Game logic, drag listeners, scramble algorithm
│   ├── LetterTile.java        # Draggable tile view
│   └── StackedLayout.java     # Custom stack-based layout
├── res/layout/
│   └── activity_main.xml      # Main game UI
└── assets/
    └── words.txt              # Dictionary of 5-letter words
```

## ⚠️ Known Issues

- No score tracking or win/loss detection — the game reveals the answer after all tiles are placed but doesn't validate correctness
- Dictionary is bundled as a flat text file with no difficulty scaling
- No landscape layout or tablet-optimized UI

## License

Apache 2.0 — see [LICENSE](https://www.apache.org/licenses/LICENSE-2.0) for details.
