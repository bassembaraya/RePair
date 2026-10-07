# What's new in RePair

## 1.0.27 (2026-10-07)

- If you're on a call when a run starts, RePair now waits for the call to end, so it never cuts
  it. You can choose Run anyway, Wait or Don't run in Settings, On a call, and how long it waits
  (up to 2 hours, 1 hour by default).
- After an update with something new for you, RePair shows a short "What's new" once.

## 1.0.26 (2026-10-07)

- Faster runs: 5 GHz opens and the car connects a few seconds sooner. RePair now checks the
  Wi-Fi with lighter reads while it waits, so it notices the switch sooner and doesn't slow the
  phone down.
- The log shows the Wi-Fi switch time in tenths of a second.

## 1.0.25 (2026-10-02)

- RePair now recognizes a working Android Auto on more phones. On some phones it reported a
  connection that worked as failed, or interrupted one that was already running.
- If your phone joins a saved Wi-Fi (like your home Wi-Fi) during a run instead of the car's, RePair
  no longer reports success. It says so and tells you which settings to turn on.
- After the phone joins the car's Wi-Fi, RePair waits up to 30 seconds for Android Auto to start,
  and only reports success once it has.
- If Android Auto drops when airplane mode turns off, RePair waits for it to come back, and tells
  you if it doesn't.
- Saved networks now stay blocked until Android Auto has started.
- New setting: "Turn Bluetooth off and on before connecting the car" (off by default), for cars that
  stay connected over Bluetooth and then don't start Android Auto. If a run fails that way, RePair
  offers it once.
- If RePair's Shizuku helper doesn't answer at first, RePair asks once more after 2
  seconds instead of failing.
- About: "You're up to date" fits on one line, the details line up on the left, and the box is a
  little wider.
- The run log lists all your settings, says whether the car's Bluetooth stayed connected, and
  records more about Android Auto. The shared log now holds your last 5 runs.

## 1.0.24 (2026-10-01)

- The shared log now tells much more: the Wi-Fi status and nearby networks at key moments,
  every Wi-Fi join and leave during a run, and a short history of app events between runs
  (updates, problems and crashes).
- With "Block saved networks during the run" on, saved networks now stay blocked until the
  run ends. The phone could undo the block by itself when Bluetooth turned off, and join a
  saved network (like a hotspot) in the middle of a run.

## 1.0.23 (2026-10-01)

- If the phone joins your car's 5 GHz Wi-Fi during a run, RePair now keeps it instead of
  disconnecting it.
- RePair no longer stops a run just because the phone doesn't list its 5 GHz channels after
  switching country. Android Auto connecting shows whether it worked.
- New share icon at the top: send the last run's detailed log file, to help find out what went wrong.

## 1.0.22 (2026-09-30)

- About: the Update button is on its own line, so the text around it no longer wraps.
- About: even space above and below the Close button.
- The Quick Settings tile's symbol is as big as the other tiles' icons.

## 1.0.21 (2026-09-30)

- The Quick Settings tile uses the new symbol too.

## 1.0.20 (2026-09-30)

- A new app icon. Its symbol is also next to the name at the top of RePair.

## 1.0.19 (2026-09-30)

- RePair now also checks for a new version when you switch back to it from recents, not only
  when you open it fresh. A version you've already been told about isn't shown again.

## 1.0.18 (2026-09-30)

- Updating is one tap now: **Update** downloads the new version inside RePair and opens Android's
  installer. No browser, no file to find. The first time, Android asks you to allow RePair to
  install apps.
- **Check for updates** in About checks right there and tells you if you're up to date.
- About has links to RePair on GitHub and to this changelog.

## 1.0.17 (2026-09-30)

- If 5 GHz doesn't open, the run now stops right there and says so, instead of waiting for
  Android Auto.
- A clear result under the run's title: Done, Failed (with the reason) or Stopped.
- Simpler step names and log lines, and the log shows the 5 GHz channels before and after.
- After a failure, the steps show what really happened, including airplane mode being turned
  back off.
- The wait for Android Auto is 60 seconds instead of 150, and you can set it from 10 to 60
  seconds in **Settings, During a run**.
- Thin lines and card borders are easier to see, and the spacing around the Shizuku status is even.

## 1.0.16 (2026-09-29)

- A run where Android Auto never connects now counts as failed: the last line is red, the step is
  marked failed, and Tasker gets `%repair_status` = `false` and `%repair_result` = "Android Auto
  didn't connect". It used to show a green "Done, but...". Airplane mode is still turned back off.
- A step that went through with a problem now shows an orange **!** instead of a green check.
- Error messages now say what to do next, and a few log colours were fixed so red always means
  the run failed or you need to act.

## 1.0.15 (2026-09-29)

- Run your own Tasker tasks around every run: in **Settings, Tasker tasks**, pick one to run
  before (RePair waits for it, up to 30 seconds) and one to run after. The after task gets
  `%repair_status`, `%repair_result`, `%repair_airplane_on` and `%repair_airplane_off`.
- Tasker: `%repair_status` is now `true` or `false`, `%repair_result` is a few words (e.g.
  "Android Auto connected"), and there are new `%repair_airplane_on` and `%repair_airplane_off`.
  `%repair_airplane` is gone, so update tasks that used it or checked for success/fail. Every
  variable is described in Tasker's variable list.
- Clearer messages: no more raw error text, a plain reason when a phone isn't supported (e.g.
  Android 12), and the first log line shows the RePair version, phone model and Android version.
- The duplicate "Android Auto is connected" line at the end of a run is gone.
- Help starts with a use at your own risk note and explains more messages.

## 1.0.14 (2026-09-28)

- When RePair can't turn on the Wi-Fi country fallback, the message now says why: Shizuku isn't
  running, Android rejected it (with Android's own reply), or the phone doesn't support it. It
  also tries a second time before giving up.

## 1.0.13 (2026-09-28)

- Fixed Wi-Fi sometimes keeping the mobile network's country, so 5 GHz never opened. It happened
  now and then, more often after a few runs in a row. RePair now keeps the country fallback on
  while the mobile signal goes, so Wi-Fi always switches.
- RePair now waits up to 30 seconds for 5 GHz to open (it still goes on as soon as it's open).
- Bluetooth no longer turns off during the run (added in 1.0.11). Your watch or earbuds stay
  connected.
- A timer next to the steps shows how long the run takes and flashes when it ends.
- The log's times line up, and some messages are clearer.

## 1.0.12 (2026-09-28)

- More reliable on phones that turn Wi-Fi off in airplane mode: RePair now keeps Wi-Fi on during
  the run and puts your phone's setting back afterwards.
- RePair now waits up to 150 seconds for Android Auto (it still finishes as soon as it connects).

## 1.0.11 (2026-09-28)

- Fixed Android Auto sometimes not connecting after a run: Bluetooth now stays off until 5 GHz is
  open, so the car can't connect too early. A watch or earbuds may disconnect for a few seconds
  during the run.

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
