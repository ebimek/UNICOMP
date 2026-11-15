# Junior Astronaut Trainer: Outpost Commander

A browser game for the NASA Space Apps Challenge, "Build a Junior Astronaut Mission Trainer".
Kids ages 7 to 12 run a Moon or Mars outpost for 12 weeks and learn the real trade-offs behind survival in deep space.
Plain HTML, CSS and JavaScript. No install, no account, no build step.

## How it teaches trade-offs
- **Pack cargo:** the rocket carries a limited amount, so more shielding means less food or power.
- **Balance power, air and water, food and radiation:** every week the crew chooses a focus, and no choice is free.
- **Real solar flares:** storms come from NASA DONKI flare data, so playthroughs change. Going to the storm shelter protects the crew but costs power and science time.
- **Radio delay:** on the Moon, Mission Control answers in about a second. On Mars, messages take 3 to 22 minutes each way, so the crew cannot wait for help.
- **Learn from failure:** each ending explains what went wrong, and each week shows a short "Real science" fact.

Extra training stations (Mars landing, orbit builder, quiz) and live NASA photos are on the home screen.

## Run it
Open `index.html` in a browser. Live NASA data needs an internet connection; otherwise the game clearly labels the archived examples it uses instead.

## Publish on GitHub Pages
1. Create a public repository and upload `index.html`, `README.md` and `DATASETS.md`.
2. Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`, Save.
3. Your game is live after about a minute at `https://<your-username>.github.io/<repository-name>/`.
4. Optional: request a Web Filter Classification (FortiGuard form linked in the Space Apps submission guide) so judges can open the site.

## NASA data
See `DATASETS.md` for the datasets used, how, and why.
Get your own free NASA API key at https://api.nasa.gov and replace `NASA_API_KEY` in `index.html`.
