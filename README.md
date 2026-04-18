# CueTimer

A browser-based session timer that cues you through structured practices — configure alarm and interval sequences for yoga, meditation, Tabata, Pomodoro, or any time-segmented routine. No install, runs offline as a single HTML file.

## 🌟 Features

- **🔔 Alarm blocks**: Add alarms that fire a soft chime after a set duration
- **⏸️ Interval blocks**: Add silent waiting periods — no sound, just a visual countdown
- **📋 Free sequencing**: Mix alarms and intervals in any order to build your practice routine
- **🔁 Repeat**: Run the full sequence N times in a row — ideal for Tabata rounds or Pomodoro cycles
- **🎛️ Mode selector**: Switch between Tabata / Pomodoro (chime at start AND end of each alarm) and Yoga (chime at end only)
- **✎ Inline editing**: Edit the duration of any block directly in the list without losing your sequence
- **🗑️ Clear all**: Wipe the current sequence in one tap
- **💾 Saved configurations**: Name and save multiple sequences; they persist across sessions via localStorage
- **↓↑ Export / Import**: Share configurations as JSON files between devices
- **🌐 EN / ES language toggle**: Full interface available in English and Spanish, preference saved automatically
- **📱 Screen always on**: Uses the Wake Lock API to prevent the screen from dimming while the timer runs
- **🔕 Background ticking**: Alarms fire even when the browser window is minimised or the tab is in the background
- **⚡ Client-side only**: No server required — works entirely in your browser, including on mobile

## 🚀 Live Demo

**[Try it now!](https://andresromeroarcas.github.io/CueTimer/CueTimer.html)**

## 🎯 Use Cases

- **Tabata & HIIT athletes**: Set work and rest alarm blocks, pick the number of rounds, and get a chime at every transition
- **Pomodoro practitioners**: Build a work + rest cycle, repeat it N times, and hear a chime only when each phase ends
- **Meditation & breathwork practitioners**: Structure sessions with precise timed phases and silent resting intervals
- **Yoga practitioners**: Hold each posture for a set duration — the chime signals when to release and transition, while the silent interval gives you time to move and settle before the next hold begins
- **Facilitators & teachers**: Cue transitions during guided sessions or workshops

## 🎛️ Modes

|  | Chime at alarm start | Chime at alarm end | Repeat control |
|--|--|--|--|
| **Tabata / Pomodoro** | ✅ | ✅ | ✅ |
| **Yoga** | — | ✅ | ✅ |

**Tabata / Pomodoro** fires a chime at both the beginning and end of every alarm block — the opening chime signals *"go"*, the closing chime signals *"stop"*. Use this for any protocol where each interval boundary matters.

**Yoga** fires a chime only when an alarm block ends. The chime means *"release and transition"* — not *"start"*. The following silent interval gives you time to move into the next posture and settle before the next hold begins quietly. Use this for yoga stretching sequences, meditation, breathwork, or any practice where you want a soft release cue rather than a start signal.

In both modes, interval blocks (blue) are always silent.

## 🔁 Repeat

The repeat control (− ×N +) lets you loop the entire sequence N times without manually duplicating blocks.

- **Tabata example**: Alarm 20 s (work) + Alarm 10 s (rest) → ×8 → 8 full rounds, chime at every transition
- **Pomodoro example**: Alarm 25 min (work) + Interval 5 min (rest) → ×4 → 4 cycles, chime only at end of each work block
- **Yoga example**: any sequence → ×1 (default, no repetition)

The current round is shown in the status bar while running (e.g. round 2 / 8). The repeat count and mode are both saved with each named configuration.

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

| Browser | Supported |
|---------|-----------|
| Chrome 60+ | ✅ |
| Firefox 55+ | ✅ |
| Safari 12+ | ✅ |
| Edge 79+ | ✅ |
| Mobile browsers (iOS Safari, Chrome Mobile) | ✅ |

Wake Lock (screen stays on while timer runs) requires Chrome/Edge on Android or Safari 16.4+ on iOS. On unsupported browsers the timer still works normally — the screen may dim as usual.

## 🛠️ Technical Details

- Pure HTML/CSS/JavaScript — no frameworks or external dependencies
- Web Audio API for soft, non-intrusive chime synthesis
- `setInterval` (100 ms) for timer ticking that continues when the window is minimised
- Screen Wake Lock API to keep the display on while the timer is running
- `localStorage` for persistent configurations, language preference, and mode
- Mobile-first layout with safe-area insets and touch-optimised controls
- Your data never leaves your device — everything runs client-side

## 📝 Supported Features

- Unlimited alarm and interval blocks per sequence
- Each block stores its own duration — blocks chain sequentially
- Both own duration and cumulative mark displayed per block
- Completed blocks visually faded with checkmark
- Per-block inline editing without disrupting the sequence
- Repeat control to loop the full sequence N times (up to 20)
- Mode selector: Tabata / Pomodoro (start + end chime) vs Yoga (end chime only)
- Round indicator in status bar during multi-round sessions
- Multiple named configurations with save, load, and delete
- Mode and repeat count saved with each configuration
- JSON export and import for cross-device sharing
- Automatic session restore on reopen
- EN / ES bilingual interface with persistent language preference
- Works offline after first load

## 📖 Example: Building a Tabata Session

**Goal**: 20 s work + 10 s rest, repeated 8 times — chime at every transition.

1. Select **Tabata / Pomodoro** mode
2. Tap **+ Alarm**, set 0 min 20 sec, tap **+ Add alarm** → work block
3. Tap **+ Alarm**, set 0 min 10 sec, tap **+ Add alarm** → rest block
4. Tap **+** on the repeat control until it shows **×8**
5. Tap **Start** — the timer chimes at the start and end of every block, for all 8 rounds

The status bar shows *round 1 / 8*, *round 2 / 8*, etc.

## 📖 Example: Building a Pomodoro Session

**Goal**: 25 min work + 5 min silent rest, repeated 4 times — chime only when work ends.

1. Select **Tabata / Pomodoro** mode
2. Tap **+ Alarm**, set 25 min 0 sec → work block (chimes at start and end)
3. Tap **+ Interval**, set 5 min 0 sec → silent rest block
4. Tap **+** on the repeat control until it shows **×4**
5. Tap **Start** — chimes at the start and end of each 25 min block; rest is silent

> If you prefer no chime at the start of each work block (only at the end), use **Yoga** mode instead.

## 📖 Example: Building a Yoga Stretching Session

**Goal**: hold each posture for 2 min → silent transition for 30 sec → hold next posture for 2 min 30 sec.

Each alarm marks the end of a hold; each interval gives you time to transition before the next one begins.

1. Select **Yoga** mode
2. Tap **+ Alarm**, set 2 min 0 sec → first hold
3. Tap **+ Interval**, set 0 min 30 sec → silent transition
4. Tap **+ Alarm**, set 2 min 30 sec → second hold
5. Tap **Start** — chimes only when each alarm block ends; the interval is silent
6. Tap **Reset** to go back to zero (the sequence is preserved)

**Saving and sharing**

- Tap **Configurations → + Save current sequence**, name it (e.g. *Morning practice*), tap **Save**
- To share: tap **Configurations → ↓ Export**, send the JSON file, and import it on another device via **↑ Import**

## 📄 License

This project is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0). For comprehensive details, kindly refer to the LICENSE file included with this project.
