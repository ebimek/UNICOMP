# NASA data and resources used

This note explains which NASA datasets the game uses, how, and why. It is also summarized inside the game (Outpost Commander > "Which numbers are real?").

## NASA datasets

### DONKI: Space Weather Database Of Notifications, Knowledge, Information
- Source: https://ccmc.gsfc.nasa.gov/tools/DONKI/ (API: https://api.nasa.gov/DONKI/FLR)
- What we use: the solar flare list (`FLR`), requested for the last 84 days (12 weeks) when the game loads.
- How it affects gameplay: the 12 weeks of the mission replay the real flares from those 12 weeks. A week with an M5 or larger flare becomes a solar storm event. A bigger flare class gives a bigger radiation event (game scaling: M5 to M9 = small, X1 to X4.9 = large, X5 and above = extreme). Players decide whether to go to the storm shelter, which costs power and crew time.
- Why: it ties the shielding trade-off to real, current space weather, so every playthrough is different.
- Live or archived: when the page can reach NASA, the game says "live data from NASA DONKI" and shows the dates it replays. If NASA cannot be reached, or the Sun was quiet, the game says so and uses archived examples of well-known flares (7 Mar 2012 X5.4, 6 Sep 2017 X9.3, 11 May 2024 X5.8). Archived data is never presented as live.
- API key: the page uses the shared `DEMO_KEY`. Replace `NASA_API_KEY` near the top of the outpost script with a free key from https://api.nasa.gov for higher rate limits.

### RadLab (OSDR Radiation Dosimetry Database)
- Source: https://visualization.osdr.nasa.gov/radlab/gui/data-api/
- What we use: one documented sample query for the International Space Station (DosTel instrument, 1 April 2022). The game shows the number of readings and their average absorbed dose rate as a real instrument reading.
- How it affects gameplay: it does not change game rules. It gives players a real measurement next to the game's radiation numbers. If the data cannot be loaded, the note is hidden.

### NASA Image and Video Library
- Source: https://images.nasa.gov (API: https://images-api.nasa.gov/search)
- What we use: real photos for Mars rovers, the Moon surface, and the Sun, shown on the home screen with a link to each photo's page.

## Published measurements and facts (not NASA datasets)
- Daily radiation baseline on the Moon, about 1.4 mSv per day: measured by the Chang'e-4 lander (Zhang et al., Science Advances, 2020).
- Daily radiation baseline on Mars, about 0.65 mSv per day: measured by NASA's Curiosity rover RAD instrument (Hassler et al., Science, 2014).
- Space station radiation, about 0.5 mSv per day: NASA public information.
- NASA's career radiation limit of 600 mSv is mentioned for context. The game's 120 mSv mission limit is a game number.
- Crew needs (about 0.84 kg of oxygen and 0.6 kg of food per person per day) are rounded from NASA human spaceflight reference values.
- "Real science" tips shown after each week are short, plain-language facts about NASA missions (Opportunity rover and the 2018 dust storm, space station exercise, lettuce grown on the station, Moon day and night length).

## Game-scaled numbers
To fit a mission into 12 short turns, these are invented for gameplay and are not NASA data: power units (PU), cargo units, battery and equipment sizes, the 120 mSv mission limit, and the size of each storm.

## Other resources
- Fonts: Inter and Space Grotesk, from Google Fonts (SIL Open Font License).
- No code libraries or frameworks. The game is plain HTML, CSS and JavaScript.
- No NASA logos or branding are used. This project is not endorsed by NASA.
