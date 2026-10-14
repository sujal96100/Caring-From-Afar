# Caring-From-Afar
How can slow-paced, routine-based care mechanics in a game prototype simulate emotional presence and foster player attachment when physical presence is impossible?

A slow-paced 2D care game built in Unity, made as the practical prototype for my MSc Computer Games Technology dissertation at Abertay University.

You play an international student living abroad while your father recovers from surgery back home. You can't be there. All you can do is show up every day, make careful choices, and hope it's enough.

## Research Question

> How can slow-paced, routine-based care mechanics in a game prototype simulate emotional presence and foster player attachment when physical presence is impossible?

Every design decision in the game (real-time schedule, budget, medicine routine, Papa's changing responses) exists to test this question.

## The Game

The game runs across **5 real days**, mirroring a recovery period. Each day you must return at specific real-world times to look after Papa:

- **Daily check-in** – greet Papa, ask how he feels, offer reassurance
- **Medicine management** – read the schedule on your virtual phone and confirm each dose on time
- **Meal choices** – pick meals that balance cost against nutrition, on a fixed budget that has to last all 5 days
- **Goodnight** – Papa sends a closing message based on how the day went

There are no reminders. If you miss a window, the family at home doesn't know what to give Papa, and he goes without. The outcome is also never guaranteed: you can do everything right and Papa may still not fully recover.

### Rule-Based Response System

Papa isn't following a fixed script. A rule-based system tracks four variables across the 5 days:

| Variable | Affected by |
|---|---|
| Health score | Medicine compliance, meal nutrition |
| Mood score | Check-in quality and consistency |
| Budget remaining | Meal choices, which limits later options |
| Medicine compliance | Doses given on time vs missed |

At the end of each day these produce one of three states, **Healing**, **Stable** or **Declining**, which decides which of Papa's dialogue lines you see.

At the end of Day 5 the game shows a results screen with your tracked stats.

## Tech

| | |
|---|---|
| Engine | Unity 2D (Unity 6.3) |
| Language | C# |
| Platform | PC (Windows `.exe`) |
| Style | Pixel art, warm tones, visual-novel-style dialogue |

Key systems: real-time clock windows, rule-based Papa state system, budget tracker, save/load between days, 5-day stats report.

## Getting Started

### Play the build

1. Download `CaringFromAfar.exe` from the `Build/` folder in this repo.
2. Run the `.exe` (Windows only).
3. Play once per scheduled window across 5 real days. The game uses your device clock, so changing the system time will break the experience.

### Run from source

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
2. Open the project folder in **Unity Hub** using **Unity 6.3**.
3. Open the main scene from `Assets/Scenes` and press Play.

## Project Structure

```
Assets/
├── Scripts/      # GameManager, clock windows, rule-based state system, budget
├── Scenes/
├── Prefabs/
├── Dialogues/    # Papa's dialogue, organised by day and state
└── Assets/       # Third-party art and audio
```

*(Adjust to match your actual folders.)*

## Design Influences

Detroit: Become Human · Papers, Please · Tamagotchi · Telling Lies · The Cat and the Coup · Ghost of Tsushima (Kurosawa Mode) · This War of Mine

## Credits and Attribution

- Pixel art assets: itch.io packs. Add each pack name, creator and link here.
- Audio: add sources here.

## Author

**Sujal**, MSc Computer Games Technology, Abertay University
LinkedIn: www.linkedin.com/in/sujal-anjara-4b3961256.
