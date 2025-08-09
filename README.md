# Assistant Lazy Commander – Speak Google Assistant Commands via Touch

**Assistant Lazy Commander** is a front‑end‑only web application (Progressive Web App) that helps you control Google Assistant or Gemini‑enabled smart devices without saying a word. It’s designed for anyone who finds voice commands inconvenient or inaccessible – for example, if you’re deaf or temporarily can’t speak, or if you just want to trigger a command on another Google device from across the room.

## What it does

The app is essentially a soundboard for Google Assistant. Each button or control builds a spoken command and plays it through your phone or computer’s speakers. When another Assistant‑enabled device hears the command (e.g. a Google Nest Mini, another phone with “Hey Google” enabled), it performs the action.

### Core features

- **Lights:** On/off buttons, a brightness slider, preset color buttons (red, green, blue, warm white, etc.) and one‑touch dim/brighten actions.
- **Thermostat:** Set a specific temperature or adjust in 0.5 °C increments, with on/off controls for HVAC systems.
- **Locks & doors:** Commands to lock/unlock doors or check status.
- **Timers & alarms:** Quick buttons for timers (1 min, 5 min, 10 min) and alarms (morning, bedtime). You can also set custom durations.
- **Information:** Ask for the time, date, weather, news, traffic, unit conversions, stock prices, sports scores and more.
- **Media controls:** Play, pause, stop or skip music, podcasts and radio streams, with optional volume controls.
- **Broadcasts:** Predefined announcements like “Dinner is ready,” “Time to wake up” or “Movie time,” plus a field for custom broadcast messages.
- **System controls:** Toggle flashlight, Bluetooth and Do Not Disturb; take a selfie or screenshot; launch YouTube with a search query; and other common assistant shortcuts.
- **Custom commands:** Type any phrase you want and speak it immediately, or prepend “Hey Google” automatically.
- **Voice tuning:** Adjust the speech rate and pitch of the spoken commands to suit your environment or preference.

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

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.