# Assistant Lazy Commander – Speak Google Assistant Commands via Touch

**Assistant Lazy Commander** is a front‑end‑only web application (Progressive Web App) that helps you control Google Assistant or Gemini‑enabled smart devices without saying a word. It’s designed for anyone who finds voice commands inconvenient or inaccessible – for example, if you’re deaf or temporarily can’t speak, or if you just want to trigger a command on another Google device from across the room.

## What it does

The app is essentially a soundboard for Google Assistant—and more. Each button or control builds a spoken command and plays it through your phone or computer’s speakers. When another Assistant‑enabled device hears the command (e.g. a Google Nest Mini, Amazon Echo, iPhone with Siri, or Samsung phone listening for “Hi Bixby”), it performs the action. You can even choose your own custom hotword.


### Core features

The app organizes dozens of common assistant actions into intuitive categories.  Each category is collapsible, letting you focus on the controls you need right now.

- **Lights:** On/off buttons, a brightness slider, and preset colors (red, orange, yellow, green, blue, purple, pink and white) with one‑tap dim/brighten actions.
- **Thermostat:** Set a specific temperature or nudge it up or down in 1 °C increments, with on/off controls.
- **Locks & doors:** Commands to lock/unlock individual doors or all doors at once.
- **Timers & alarms:** Quick buttons for 5‑minute, 10‑minute, 30‑minute and 1‑hour timers, plus customizable durations; alarms for common wake‑up times and cancellation.
- **Information:** Ask for the weather, time, date, news headlines, traffic conditions, stock market updates, unit conversions, sports scores and more.
- **Media controls:** Play jazz, workout or general music; play the latest news; pause, resume, stop, skip forward/back and adjust volume.
- **Broadcasts:** Predefined announcements like “Wake up,” “Breakfast,” “Dinner,” “Movie time” and “Bedtime,” with a custom broadcast field to say whatever you need.
- **System controls:** Toggle your device’s flashlight, Bluetooth and Do Not Disturb modes; take selfies or screenshots; open YouTube or run a YouTube search.
- **Custom commands:** Type any phrase and speak it immediately, or prepend your chosen hotword.
- **Voice tuning:** Adjust the speech rate and pitch of the spoken commands; choose from any English voice installed on your device.
- **Scenes & modes:** Multi‑action routines like *Movie Night*, *Work Mode*, *Party Mode*, *Relax Mode* and *Vacation Mode* chain several commands (dim lights, play music, set thermostat) into a single press.
- **Shopping & lists:** Add items like milk or eggs to your shopping list, ask what’s currently on the list, or clear the list entirely.
- **Calendar & reminders:** Create calendar events for specific dates and times, set reminders (e.g. call Mom at 8 PM, drink water regularly) or find out what’s on your schedule.
- **Productivity:** Kick off Pomodoro‑style focus and break timers, play your study playlist or cancel all running timers and reminders.
- **Travel & navigation:** Ask for directions home or to work, locate the nearest gas station, check traffic to the airport, or find restaurants near you.
- **Cooking & recipes:** Preheat the oven, set a pizza timer, convert measurements, look up recipes (like pancakes) or start the coffee maker with one tap.
- **Health & fitness:** Start a workout or guided meditation, play your workout playlist, check your step count or set hourly hydration reminders.
- **Education & learning:** Request definitions, translations and spellings, or get quick explanations of scientific concepts like photosynthesis or quantum mechanics.
- **Routines:** Single‑tap routines like *Good Morning*, *Good Night*, *Leaving Home* and *Arriving Home* speak a series of commands (lights, thermostat, music) with brief pauses so your assistant can keep up.

- **Security & surveillance:** Show live feeds from front‑door or backyard cameras and arm or disarm your smart security system.


In addition to the core categories, the app includes several powerful enhancements:

- **Assistant & voice options:** A dedicated card at the top lets you pick which assistant to target—Google, Alexa, Siri, Bixby, Cortana or even a custom hotword. Whatever prefix you choose is automatically prepended to every command (and existing prefixes are stripped out). You can also select from any English voice installed on your device and fine‑tune the speech rate and pitch.
- **Multi‑assistant routines:** Multi‑step macros (e.g. *Good Morning*, *Good Night*, *Leaving Home*, *Arriving Home*) that speak several commands in sequence, with delays between them. Adjust the assistant prefix first and each routine will target your preferred assistant.
- **Expanded categories:** Beyond lights and thermostats, you’ll find sections for scenes & modes, shopping & lists, calendar & reminders, productivity, travel & navigation, cooking & recipes, health & fitness, education & learning, media, broadcasts, system controls, security & surveillance and fun easter eggs. Each section houses multiple one‑tap commands and sliders.

Because the app is static and runs entirely in your browser, no data is sent to any server. The service worker caches assets for offline use and updates itself when a new version is deployed.

## How to use it

1. **Install or open the web app:**
   - On mobile, open `https://assistant-lazy-commander.netlify.app` and add it to your home screen via your browser’s “Add to Home Screen” feature. This turns it into a standalone PWA.
   - On desktop, you can simply open the URL in any modern browser.

2. **Select a command category:** Tap one of the expandable sections (Lights, Thermostat, Media, etc.) to reveal its controls.

3. **Tap to speak:** Each button instantly plays an audio snippet containing the corresponding Google Assistant command. For example, tapping “On” in the Lights section says “Hey Google, turn on the lights.”

4. **Use sliders and color selectors:** For brightness and temperature, adjust the slider to your desired value and then tap the accompanying speak button. For colors, just tap the color swatch.

5. **Create custom phrases:** In the “Custom command” section, type any phrase you’d like the device to say. You can optionally tick “Prefix with ‘Hey Google’” to automatically add the hotword.

6. **Tune the voice:** If the default voice sounds too fast or slow, adjust the Rate and Pitch sliders under Voice Settings until it’s clear and audible for your Assistant device.

7. **Trigger the command on a separate device:** Place your phone or computer near another Google Assistant/Gemini device with the microphone on. The spoken command should be heard and executed. Note that many phones deliberately ignore TTS audio for hotword detection; using a separate device is the most reliable setup.

## Who it’s for

This tool is helpful for:

- **Deaf or hard‑of‑hearing users** who can’t rely on voice commands but still want to control smart home devices via Google Assistant.
- **People with temporary speech impairments** (e.g. sore throat, laryngitis) who need another way to interact with their smart devices.
- **Anyone who wants to automate Google Assistant from another room** without yelling or using Routines/API integrations.

It’s not limited to these groups; anyone can use it as a quick command launcher.

## Development notes

- **Stack:** Plain HTML, CSS and JavaScript. No frameworks or backend.
- **Service worker:** Cached for offline use with versioning. When deploying updates, change the cache name and call `self.skipWaiting()` & `clients.claim()` to ensure users get the latest version without manual refresh.
- **Contributing:** Feel free to fork this repository and add more commands, categories or local integrations (e.g. calls to smart‑home APIs like Philips Hue or Home Assistant). Pull requests are welcome!

## Origin of this project

This app was built end‑to‑end by **ChatGPT**, OpenAI’s large language model. Working solely from Andrei’s account (with his permission), ChatGPT authored every line of code, style and markup, assembled the PWA and service worker, created the README, packaged the project, provisioned the Netlify hosting, connected it to GitHub and configured continuous deployment. No human hand coded or modified the files—this is a fully AI‑written project. The intention is to showcase how generative AI can help build assistive tools rapidly while keeping all logic client‑side.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.