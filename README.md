# A Matter of Some Urgency

**An Interactive Comedy of Bureaucratic Adventure in One Act, Several Rooms, and Considerable Inconvenience**

A fully self-contained text-adventure RPG in a single HTML file. No dependencies, no server, no build step. Open it in a browser and play.

---

## Deploying to GitHub Pages

1. **Create a new repository** on GitHub (e.g. `a-matter-of-some-urgency` or any name you like)

2. **Upload `index.html`** — either drag it into the GitHub web interface or push via git:
   ```bash
   git init
   git add index.html
   git commit -m "Initial delivery"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repo → **Settings** → **Pages**
   - Under *Source*, select **Deploy from a branch**
   - Choose **main** branch, **/ (root)** folder
   - Click **Save**

4. Your game will be live at:
   `https://YOUR_USERNAME.github.io/YOUR_REPO/`
   (GitHub Pages usually takes 1–2 minutes to deploy)

---

## Playing the Game

Type commands into the input bar at the bottom. The game understands natural verb + noun constructions.

### Key Commands

| Command | Effect |
|---|---|
| `LOOK` | Describe your current location |
| `EXAMINE [thing]` or `X [thing]` | Look more closely at something |
| `GO NORTH` / `N` | Move (N, S, E, W also work) |
| `TAKE [item]` | Pick something up |
| `INVENTORY` or `I` | See what you're carrying |
| `TALK TO [person]` | Speak to a character |
| `GIVE [item] TO [person]` | Hand something over |
| `SHOW [item] TO [person]` | Show without giving |
| `USE [item]` | Use something from inventory |
| `EAT [item]` / `DRINK [item]` | Consume things |
| `KNOCK` | Knock on a door |
| `DELIVER LETTER` | Attempt final delivery |
| `RIDDLE` | Accept a riddle challenge |
| `ANSWER [word]` | Answer a riddle |
| `STAMP` | Use official rubber stamp |
| `SAVE` | Save your game |
| `LOAD` | Load saved game |
| `SCORE` | Check current score |
| `HELP` | Show command reference |

Arrow keys ↑↓ scroll through command history.

---

## The Story

You are **Crabwick Pell**, Licensed Deliverer (Third Class, Provisional), employed by the Omnipotent Postal Consortium. You have one letter. It must reach Mr. Horace Dunt of Mudwick-Under-Sorrow. Between you and delivery: a bridge warden who hasn't left her post in forty years, a philosophically confused mushroom, a dragon with an expired contract, a monk who only answers questions with questions, and a raven that won something it probably shouldn't have.

**Approximately 12–15 rooms. Around 45–90 minutes first playthrough.**

---

## The Rules System

Combat and skill challenges use **2d10 + stat vs. target number**:

- **CUNNING (4)** — Used for clever solutions, persuasion, trickery
- **NERVE (3)** — Used for confrontations, holding ground, final deliveries

When a skill check triggers, an animated dice roller appears. Roll the dice, add your stat, beat the target. Fail and you lose Stamina; drop to 0 and... well. The Consortium will send someone else.

**Stamina** can be restored by eating food found in the world, or drinking the Restorative Tincture from the village shop.

---

## Saving

The game auto-saves after every command to `localStorage`. You can also type `SAVE` explicitly. On the title screen, **Resume Duty** appears if a save exists.

Saves are stored in the browser — they persist between sessions on the same device/browser but won't transfer to another device.

---

## Technical Notes

- Single `index.html`, no external dependencies (one Google Fonts import for typography)
- ES5-compatible JavaScript
- Works on desktop and mobile browsers
- LocalStorage used for save data only

---

*"The letter always arrives eventually. For certain values of eventually."*  
*— Omnipotent Postal Consortium, Field Manual, p. 1*
