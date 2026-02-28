# A-movie-dialogue-capture-tool-that-you-can-run-directly-in-notepad

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?logo=react)](https://reactjs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

A sleek, interactive React application that simulates capturing dialogue from movies and writing it directly to a virtual notepad. Perfect for filmmakers, screenwriters, students, or anyone who wants to collect memorable quotes with cinematic flair.

<img width="1864" height="1080" alt="image" src="https://github.com/user-attachments/assets/3ee9cb43-55c2-4e73-b4b6-a7340fceabf3" />

##  Features

- ** Real-time Dialogue Capture** – Insert timestamped movie quotes with a single click or keyboard shortcut
- ** AI Isolation Simulation** – Toggle between "mixed audio" and "isolated voice" modes for cleaner dialogue examples
- ** Live Notepad** – Fully editable contenteditable area that behaves just like a text editor
- ** Keyboard Shortcuts** – `Ctrl+Shift+D` to capture dialogue from anywhere in the app
- ** Audio Visualizer** – Dynamic animated bars that respond to recording state
- ** Capture History** – Keep track of your last 10 captured lines for quick reference
- ** Movie Metadata** – Each quote includes movie title and timestamp
- ** Dark Theme** – Easy on the eyes for those late-night writing sessions

##  Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/movie-dialogue-capturer.git
   cd movie-dialogue-capturer
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Build for production**
   ```bash
   npm run build
   ```

##  Usage

### Basic Workflow

1. **Launch the app** – The interface splits into two main panels: Audio Capturer (left) and Notepad (right)
2. **Toggle Isolation** – Use the switch in the Isolation Panel to simulate "clean voice" extraction
3. **Capture Dialogue** – Click the red **Capture** button or press `Ctrl+Shift+D`
4. **Watch it appear** – The dialogue inserts directly at your cursor position in the notepad
5. **Play with audio** – Use **Play** to start the visualizer animation, **Stop** to pause

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Shift+D` | Capture dialogue at cursor |
| `Ctrl+A` | Select all in notepad |
| `Ctrl+Z` | Undo (browser default) |

### Example Dialogue Lines

The app includes famous quotes from movies like:
- Interstellar
- Inception
- The Notebook
- Star Wars
- The Dark Knight
- And many more!

##  Component Structure

```
src/
├── App.js              # Main application component
├── App.css             # All styles (single file for simplicity)
├── index.js            # Entry point
└── index.css           # Global styles
```

##  Customization

### Adding Your Own Dialogue

Edit the `DIALOGUE_LINES` and `ISOLATED_LINES` arrays in `App.js`:

```javascript
const DIALOGUE_LINES = [
  { 
    id: 16, 
    text: 'Your custom quote here', 
    movie: 'Movie Name' 
  },
  // Add more...
];
```

### Modifying the Visualizer

Adjust the bar count or animation speed in the `useEffect` hook:

```javascript
// Change number of bars
const [audioLevel, setAudioLevel] = useState(Array(20).fill(15)); // 20 bars

// Change animation interval (ms)
setInterval(() => {
  // your logic
}, 500); // Slower animation
```

##  Design Philosophy

- **Cinematic Dark Theme** – Inspired by movie theater aesthetics
- **Skeuomorphic Elements** – Buttons with physical press effects, visualizer bars that mimic audio software
- **Content First** – Notepad takes center stage, controls are intuitive but unobtrusive
- **Responsive** – Works on desktop and tablet (mobile coming soon)

##  Dependencies

- React 18.2.0
- No external UI libraries – pure CSS for lightweight performance

##  Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-idea`)
3. Commit your changes (`git commit -m 'Add some amazing idea'`)
4. Push to the branch (`git push origin feature/amazing-idea`)
5. Open a Pull Request

### Ideas for Contributions
- Add more movie quotes
- Implement actual Web Audio API for real audio input
- Add export functionality (TXT, PDF, etc.)
- Create a backend API for saving sessions
- Add user authentication for personal quote libraries
- Implement search/filter for quotes

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by tools like EchoWrite, WhisperNotes, and Acon Digital's Extract:Dialogue
- Movie quotes belong to their respective copyright holders – used here for demonstration purposes only
- Built with React and lots of ☕

