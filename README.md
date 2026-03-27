# CueTimer

A lightweight, mobile-friendly browser app for building timed sequences of alarms and silent intervals — no install required, works entirely offline as a single HTML file.

## 🌟 Features

- **🔔 Alarm blocks**: Add alarms that fire a soft chime after a set duration
- **⏸️ Interval blocks**: Add silent waiting periods — no sound, just a visual countdown
- **📋 Free sequencing**: Mix alarms and intervals in any order to build your practice routine
- **✎ Inline editing**: Edit the duration of any block directly in the list without losing your sequence
- **🗑️ Clear all**: Wipe the current sequence in one tap
- **💾 Saved configurations**: Name and save multiple sequences; they persist across sessions via localStorage
- **↓↑ Export / Import**: Share configurations as JSON files between devices
- **🌐 EN / ES language toggle**: Full interface available in English and Spanish, preference saved automatically
- **⚡ Client-Side Processing**: No server required — works entirely in your browser, including on mobile

## 🚀 Live Demo

**[Try it now!](https://andresromeroarcas.github.io/CueTimer/CueTimer.html)**

## 🎯 Use Cases

- **Meditation & breathwork practitioners**: Structure sessions with precise timed phases and silent resting intervals
- **Yoga & kriya practitioners**: Build reproducible sequences for daily practice routines
- **Athletes & coaches**: Time training intervals with distinct work and rest blocks
- **Facilitators & teachers**: Cue transitions during guided sessions or workshops

## 💻 Getting Started

### Option 1: Use Online (Recommended)
Simply visit the [live demo](https://andresromeroarcas.github.io/CueTimer/CueTimer.html) and start using it immediately — no sign-up, no install.

### Option 2: Download and Run Locally
1. Download the `CueTimer.html` file
2. Open it in any modern web browser (desktop or mobile)
3. Add your alarms and intervals and start your session

### Option 3: Clone Repository
```bash
git clone https://github.com/andresromeroarcas/CueTimer.git
cd CueTimer
# Open CueTimer.html in your browser
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
- [x] Each block stores its own duration — blocks chain sequentially
- [x] Both own duration and cumulative mark displayed per block
- [x] Completed blocks (alarms and intervals) visually faded with checkmark
- [x] Per-block inline editing without disrupting the sequence
- [x] Multiple named configurations with save, load, and delete
- [x] JSON export and import for cross-device sharing
- [x] Automatic session restore on reopen
- [x] EN / ES bilingual interface with persistent language preference
- [x] Works offline after first load

## 📖 Example: Building a Practice Session

Here is a step-by-step walkthrough of a typical session — a routine with two alarm cues separated by a silent interval.

**Goal**: alarm after 2 min → silent rest for 30 sec → alarm after 2 min 30 sec → run the timer.

> **How time works**: each block stores its own duration and blocks chain sequentially. An alarm set to `02:30` fires 2 minutes and 30 seconds after the previous block ends. The cumulative mark (e.g. `→ 05:00`) is shown alongside each block's own duration so you always know where in the timeline it sits.

### Step 1 — Add the first alarm
1. Tap **+ Alarm**
2. A modal slides up from the bottom. Set **2 min 0 sec**
3. Tap **+ Add alarm**
4. The block appears in the sequence showing `02:00 → 02:00`

### Step 2 — Add a silent interval
1. Tap **+ Interval**
2. Set **0 min 30 sec**
3. Tap **+ Add interval**
4. A blue interval block appears below the alarm, connected by a vertical line, showing `30s → at 02:30`

### Step 3 — Add a second alarm
1. Tap **+ Alarm**
2. Set **2 min 30 sec**
3. Tap **+ Add alarm**
4. The sequence reads: Alarm `02:00 → 02:00` → Interval `30s` → Alarm `02:30 → 05:00`
5. Total session duration: **5:00** (2:00 + 0:30 + 2:30)

### Step 4 — Edit a block (optional)
1. Tap the **✎** pencil icon on any block
2. An inline editor opens below that block
3. Change the minutes or seconds and tap **Save**
4. The block updates in place without affecting the others

### Step 5 — Run the session
1. Tap **Start** — the timer turns green and begins counting
2. After 2:00 the first alarm fires a soft three-note chime and the block fades out with a ✓
3. The interval block becomes active (blue) and counts down silently for 30 sec, then fades out with a ✓
4. After another 2:30 the second alarm fires
5. Tap **Reset** to go back to zero (the sequence is preserved)

### Step 6 — Save the configuration
1. Tap **Configurations** (top right)
2. Tap **+ Save current sequence**
3. Type a name, e.g. `Morning practice`, and tap **Save**
4. The configuration is stored on your device

### Step 7 — Reload it next time
1. Tap **Configurations**
2. Find `Morning practice` in the list — it shows the number of alarms and total duration
3. Tap **Load** — the sequence is restored instantly, ready to run

### Step 8 — Share it with another device
1. Tap **Configurations → ↓ Export**
2. A `stopwatch-configs.json` file downloads to your device
3. Send it to another phone via WhatsApp, AirDrop, or email
4. On the other device, open CueTimer, tap **Configurations → ↑ Import**, and select the file
5. All saved configurations merge in — no duplicates

## 📄 License

This project is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0). For comprehensive details, kindly refer to the LICENSE file included with this project.
