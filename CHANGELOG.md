# What's new in RePair

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
