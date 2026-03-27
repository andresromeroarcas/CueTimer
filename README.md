# CueTimer

A lightweight, mobile-friendly browser app for building timed sequences of alarms and silent intervals — no install required, works entirely offline as a single HTML file.

## 🌟 Features

- **🔔 Alarm blocks**: Add alarms that fire a soft chime at a specific elapsed time
- **⏸️ Interval blocks**: Add silent waiting periods between alarms — no sound, just a visual countdown
- **📋 Free sequencing**: Mix alarms and intervals in any order to build your practice routine
- **✎ Inline editing**: Edit the duration of any block directly in the list without losing your sequence
- **💾 Saved configurations**: Name and save multiple sequences; they persist across sessions via localStorage
- **↓↑ Export / Import**: Share configurations as JSON files between devices
- **🌐 EN / ES language toggle**: Full interface available in English and Spanish, preference saved automatically
- **🗑️ Clear all**: Wipe the current sequence in one tap
- **⚡ Client-Side Processing**: No server required — works entirely in your browser, including on mobile

## 🚀 Live Demo

**[Try it now!](https://romeroarcasandres.github.io/CueTimer/)**

## 🎯 Use Cases

- **Meditation & breathwork practitioners**: Structure sessions with precise timed phases and silent resting intervals
- **Yoga & kriya practitioners**: Build reproducible sequences for daily practice routines
- **Athletes & coaches**: Time training intervals with distinct work and rest blocks
- **Facilitators & teachers**: Cue transitions during guided sessions or workshops

## 💻 Getting Started

### Option 1: Use Online (Recommended)
Simply visit the [live demo](https://romeroarcasandres.github.io/CueTimer/) and start using it immediately — no sign-up, no install.

### Option 2: Download and Run Locally
1. Download the `index.html` file
2. Open it in any modern web browser (desktop or mobile)
3. Add your alarms and intervals and start your session

### Option 3: Clone Repository
```bash
git clone https://github.com/romeroarcasandres/CueTimer.git
cd CueTimer
# Open index.html in your browser
```

## 📱 Browser Compatibility

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript** — No frameworks or external dependencies
- **Web Audio API** for soft, non-intrusive chime synthesis
- **requestAnimationFrame** for smooth millisecond-accurate timer display
- **localStorage** for persistent configurations and language preference
- **Mobile-first layout** with safe-area insets and touch-optimised controls
- **Your data never leaves your device** — everything runs client-side

## 📝 Supported Features

- [x] Unlimited alarm and interval blocks per sequence
- [x] Per-block inline editing without disrupting the sequence
- [x] Multiple named configurations with save, load, and delete
- [x] JSON export and import for cross-device sharing
- [x] Automatic session restore on reopen
- [x] EN / ES bilingual interface with persistent language preference
- [x] Works offline after first load

## 📄 License

This project is governed by the CC BY-NC 4.0 license. For comprehensive details, kindly refer to the LICENSE file included with this project.
