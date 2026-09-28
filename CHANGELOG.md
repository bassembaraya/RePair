# What's new in RePair

## 1.0.10 (2026-09-28)

- Fixed 5 GHz staying closed on some phones even though the Wi-Fi country had switched: RePair
  now restarts Wi-Fi once when that happens.
- **Disconnect Wi-Fi if connected** (was "Turn off Wi-Fi if connected"): RePair now disconnects
  from the network and keeps Wi-Fi on, which makes the switch to the fallback country more
  reliable.
- The app icon now shows next to RePair's name on the main screen.

## 1.0.8 (2026-09-28)

- Fixed a run stopping at "Wait for 5 GHz to open" on some phones, even though the Wi-Fi country
  had switched.

## 1.0.7 (2026-09-28)

- RePair now tells you when a new version is available.

## 1.0.6 (2026-09-28)

- New ⓘ button on the main screen with app info, contact and updates.
- Phones that don't show their fallback Wi-Fi country are no longer blocked: RePair shows a
  warning and tries anyway.

## 1.0.5 (2026-09-28)

- UI improvements.

## 1.0.4 (2026-09-27)

- The app shortcut is now called **Run RePair in the background** (long press the icon, or in Samsung
  Modes and Routines), to make clear it runs quietly without opening the app. Routines you
  already set up keep working.

## 1.0.3 (2026-09-27)

- **Check for updates**: in **Settings, About**, one tap opens the releases page so you can see if
  there's a newer version. RePair still has no internet permission and never checks by itself.

## 1.0.2 (2026-09-27)

- **Block saved networks during the run now really works**, without root. From the moment Wi-Fi
  turns on until Android Auto connects, your phone won't jump onto your home Wi-Fi or a hotspot.
  The log now shows whether the block really took effect.
- If the phone still manages to join a saved network during the run, RePair blocks again and
  disconnects it instead of stopping.
- If a run is ever cut off, saved networks are allowed again the next time RePair opens or runs.

## 1.0.1 (2026-09-27)

- Updated the contact email in **Settings, About** to mcbaraya.dev@gmail.com.

## 1.0.0 (2026-09-27)

First release.

- **One tap fix for wireless Android Auto**: switches the phone to its fallback Wi-Fi country so
  the car's 5 GHz channel opens, reconnects the car, waits for Android Auto (up to 90 seconds),
  then turns the mobile network back on.
- **Safe by design**: if anything fails or you tap Stop, airplane mode is turned back off. If
  Android Auto is already connected, nothing is changed.
- **Live steps and log** in the app, and the car's Bluetooth state on its card.
- **Run it your way**: in-app button, Quick Settings tile, app shortcut, Samsung Modes and
  Routines, or Tasker (with `%repair_status`, `%repair_result` and `%repair_airplane`).
- **Settings**: turn off Wi-Fi automatically before a run, toasts and notifications for results,
  Light, Dark or System theme.
- **Setup checklist** and a **Help** screen with every step and error explained.
- Works without root, through Shizuku. No internet permission.
