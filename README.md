# ODD GENERATOR - Brutalist Verse Machine

A mobile-friendly, browser-based site that generates odd 1-3 sentence outputs from text input, images, or curated corpus. Think "bumper sticker" style idiom adjacent with brutalist styling.

## 🚀 Quick Start

### Local Testing
```bash
cd /workspace/odd-generator
python3 -m http.server 8000
```
Then open: `http://localhost:8000`

### Deploy to Netlify (Recommended for iPad/iPhone)
1. Go to https://app.netlify.com/drop
2. Drag the entire `/workspace/odd-generator` folder
3. Get instant HTTPS URL
4. Open in Safari on iOS → Share → "Add to Home Screen"

### Deploy to GitHub Pages
```bash
cd /workspace/odd-generator
git init
git add .
git commit -m "Initial commit"
git remote add origin YOUR_REPO_URL
git push -u origin main
```
Then enable GitHub Pages in repo settings.

## 📁 Files

- **index.html** - Complete single-file app (HTML/CSS/JS)
- **prompts.json** - Admin-configurable prompt ingredients
- **README.md** - This documentation

## 🎨 Features

### Creative Modes
- **Vague Monotone** - Flat, indifferent statements
- **Fever Dream Log** - Surreal, disjointed imagery
- **Lyrical Entropy** - Poetic decay and beautiful disorder
- **Diary of Random** - Intimate confessions from unreliable narrator
- **Bumper Sticker Wisdom** - Pseudo-profound advice

### Input Options
- Text textarea for custom input
- Image upload (extracts filename/metadata for inspiration)
- Leave blank for pure random generation

### Actions
- **Generate** - Create odd output based on current mode
- **Random Mode** - Cycle to random creative mode
- **Save** - Store output in localStorage memory
- **Share** - Native iOS share sheet integration
- **Copy** - Copy to clipboard

### Memory System
- Persistent localStorage storage
- View all saved generations
- Delete individual items
- Survives page refreshes

## 🔧 Customize prompts.json

Edit the JSON file to add new modes, prefixes, middles, suffixes, or corpus fragments:

```json
{
  "modes": {
    "your_new_mode": {
      "name": "Display Name",
      "description": "What it does",
      "prefixes": ["prefix one", "prefix two"],
      "middles": ["middle phrase", "another middle"],
      "suffixes": ["ending one", "ending two"]
    }
  },
  "corpus": {
    "free_verse_fragments": ["your fragments here"],
    "idiom_adjacent": ["your idioms here"]
  },
  "settings": {
    "default_mode": "vague_monotone",
    "max_sentences": 3,
    "min_sentences": 1
  }
}
```

## 📱 iOS Optimization

- Mobile-first responsive design
- Touch-optimized buttons
- `apple-mobile-web-app-capable` meta tag
- Full-screen mode when added to Home Screen
- Native share sheet support
- High-contrast brutalist UI readable in sunlight

## 🎯 Usage Tips

1. **Pure Random**: Leave text blank, hit Generate
2. **Seed Ideas**: Type a word or phrase, generate variations
3. **Image Inspiration**: Upload any image for metadata-based prompts
4. **Mode Mixing**: Use Random Mode button for surprise combinations
5. **Build Collections**: Save favorites to memory over time

## 🛠 Technical Details

- Zero dependencies - pure HTML/CSS/JS
- Works offline after initial load
- localStorage for persistence (no server required)
- Responsive breakpoints for all screen sizes
- Monospace typography for brutalist aesthetic
- High contrast black/white color scheme

## 📄 License

MIT License - Do whatever you want with it.