# ODD GENERATOR

A brutalist, mobile-friendly browser-based site that generates odd and unusual 1-3 sentence outputs (bumper sticker style idiom adjacent) from text input, images, or curated free-verse corpus.

## Features

- **5 Creative Modes:**
  - Vague Monotone - Flat, indifferent statements
  - Fever Dream Log - Surreal, disjointed imagery
  - Lyrical Entropy - Poetic decay and beautiful disorder
  - Diary of Random - Intimate confessions from unreliable narrator
  - Bumper Sticker Wisdom - Pseudo-profound advice

- **Input Options:**
  - Text input field
  - Image upload (extracts metadata for creative inspiration)
  - Leave blank for pure random generation

- **Actions:**
  - ⚡ Generate oddness
  - 🎲 Random mode selector
  - 💾 Save to local memory
  - 📤 Share (native share on iOS/Android)
  - 📋 Copy to clipboard

- **Mobile Optimized:**
  - Responsive design
  - Touch-friendly buttons
  - iOS web app capable (add to home screen)
  - Works offline after first load

- **Persistent Memory:**
  - Saves generations to localStorage
  - View and delete saved memories
  - Data persists across sessions

## Quick Start

### Local Testing
```bash
cd /workspace/odd-generator
python3 -m http.server 8080
# Open http://localhost:8080 in your browser
```

### Deploy to Web

#### Option 1: GitHub Pages (Free)
1. Push files to a GitHub repository
2. Enable GitHub Pages in repo settings
3. Access via `https://yourusername.github.io/repo-name`

#### Option 2: Netlify (Free)
1. Drag and drop the `odd-generator` folder to [Netlify Drop](https://app.netlify.com/drop)
2. Get instant HTTPS URL
3. Optionally connect custom domain

#### Option 3: Vercel (Free)
```bash
npm i -g vercel
cd /workspace/odd-generator
vercel --prod
```

#### Option 4: Any Static Host
Upload both files (`index.html` and `prompts.json`) to any static hosting service.

## Customization

### Edit prompts.json

The `prompts.json` file is admin-friendly and fully customizable:

```json
{
  "modes": {
    "your_mode_id": {
      "name": "Display Name",
      "description": "What this mode does",
      "prefixes": ["array", "of", "starting", "phrases"],
      "middles": ["array", "of", "middle", "content"],
      "suffixes": ["array", "of", "ending", "phrases"]
    }
  },
  "corpus": {
    "free_verse_fragments": ["poetic", "fragments", "here"],
    "idiom_adjacent": ["twisted", "idioms", "here"]
  },
  "settings": {
    "default_mode": "your_mode_id",
    "max_sentences": 3,
    "min_sentences": 1,
    "allow_image_input": true,
    "allow_text_input": true,
    "enable_memory": true
  }
}
```

### Add New Modes
Simply add a new entry to the `modes` object in `prompts.json`:

```json
"new_mode": {
  "name": "Your Mode Name",
  "description": "Description here",
  "prefixes": ["prefix 1", "prefix 2"],
  "middles": ["middle 1", "middle 2"],
  "suffixes": ["suffix 1", "suffix 2"]
}
```

### Customize Corpus
Add your own free-verse fragments or twisted idioms to the `corpus` arrays.

## iOS/iPhone Usage

1. Deploy to a web host (see options above)
2. Open the URL in Safari on your iPhone/iPad
3. Tap the Share button
4. Select "Add to Home Screen"
5. The app will install like a native app
6. Works offline after initial load!

## File Structure

```
odd-generator/
├── index.html          # Main application (all-in-one HTML/CSS/JS)
├── prompts.json        # Configurable prompt ingredients
└── README.md           # This file
```

## Technical Details

- **No dependencies** - Pure HTML, CSS, and vanilla JavaScript
- **LocalStorage** - All memories saved locally in browser
- **Fetch API** - Loads prompts.json dynamically
- **Web Share API** - Native sharing on supported devices
- **Responsive CSS** - Mobile-first brutalist design
- **PWA-ready** - Can be added to home screen on iOS/Android

## Browser Support

- ✅ Safari (iOS/macOS)
- ✅ Chrome (Android/Desktop)
- ✅ Firefox
- ✅ Edge
- ✅ Any modern browser with ES6 support

## License

MIT - Do whatever you want with it.

---

**Made with brute force and minimal elegance.**
