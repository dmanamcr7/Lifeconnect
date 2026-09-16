# Connected Life

Gym, Money and Shop in one app. One HTML file, no install, runs in the phone browser and on the computer.

- **Gym** — RepBank training log.
- **Money** — Finance Hub: pay cycle, bills, debts, savings, budgets.
- **Shop** — shopping trips priced from your store history, recorded into Money.
- **Connected** — insights across all three.

## Setup

1. GitHub Pages serves this repo. Open `https://<username>.github.io/<repo>/` on each device; on the phone add it to the Home Screen.
2. On the device that already has your data, tap the sync button in the top bar and enter:
   - a sync code (12+ characters, keep it private — anyone with it sees Money)
   - the database line: `{ "databaseURL": "https://<your-db>.firebasedatabase.app" }`
3. Do the same on the other device with the same code and line. Changes made on one show on the other; a banner offers Refresh if you're mid-use.

## Notes

- The sync code and database line are stored on each device, not in this file. Replacing `index.html` never touches your data.
- Data is stored in Firebase Realtime Database under `households/<code>/connected/` — one record each for Gym, Money and Shop.
- The app checks GitHub for a newer version each time it opens and reloads itself.
- Firebase rules should require codes of 12+ characters (see Rules tab in the Firebase console).
