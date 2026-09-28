# What's new in RePair

## 1.0.5 (2026-09-28)

- **Refreshed Settings screen**: a cleaner layout with your settings first, a new "Ways to run
  RePair" section with clear steps for Samsung Modes and Routines, the Quick Settings tile, the
  shortcut and Tasker, and an About card with version, contact and Check for updates.

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
