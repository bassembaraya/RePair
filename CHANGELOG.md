# What's new in RePair

## 1.0.57 (2026-10-28)

### Changed

- With "Debugging off between runs" on, developer options and USB debugging now turn off as soon as each run ends, even while Android Auto is still connected.
- Turning on "Debugging off between runs" now works when developer options are already off.
- The update notice shows one point per line, easier to read.

### Fixed

- A RePair run or status check from Tasker or the tile that fails no longer cancels the runs and checks queued after it.

## 1.0.56 (2026-10-27)

### Fixed

- With "Debugging off between runs" on, Android no longer stops RePair when the car disconnects while another of your apps is using wireless debugging.

## 1.0.55 (2026-10-27)

### Fixed

- After a restart, Vexer now starts on any Wi-Fi, even one without internet, like a car's.
- On a new Wi-Fi, Vexer waits for your answer to Android's wireless debugging question instead of giving up.
- If Vexer's pairing is removed, RePair stays on Vexer and asks you to pair again, instead of switching to Shizuku.
- After pairing, Wireless debugging turns itself off again, also after you allow a new Wi-Fi for it.
- If you leave Android's wireless debugging question unanswered or tap Deny, it isn't asked again and again. Opening RePair asks again.
- On phones that turn wireless debugging off while they ask (stock Android), Vexer now waits for your Allow.
- Pairing with USB debugging off now works: RePair turns USB debugging on, as Vexer needs it.
- With "Reconnect Vexer automatically" off, nothing reconnects after a restart either.

## 1.0.54 (2026-10-26)

### Changed

- When your car doesn't connect and the phone is on another car's Bluetooth, RePair says which car.
- If the helper stops during a run, the log says why, for example a USB cable was plugged in.
- Updating waits until a run is done.
- Clearer messages everywhere, and they name the helper you use (Vexer or Shizuku).
- The car card shows the RePair car in the app's colors, in light and dark.
- Vexer comes back by itself after a USB cable or USB mode change.
- RePair asks once to run without battery limits, so Vexer can come back on its own. It's your choice.
- With no Wi-Fi after a restart, RePair says Vexer needs Wi-Fi once, instead of "Connecting...".

### Fixed

- Vexer starts again by itself after an update, even when the phone put RePair to sleep.

## 1.0.53 (2026-10-25)

### Changed

- Vexer has a new icon: a fox.

## 1.0.52 (2026-10-25)

### Changed

- Ghostack is now called **Vexer**, with a little robot icon. It's the same helper: nothing to set up again.
- The status at the top starts with a capital: "Vexer: Connected".
- Turning on "Debugging off between runs" now says debugging goes off again when the car disconnects, the same as its line in Settings.

### Fixed

- "Debugging off between runs" now turns Wireless debugging off too. Before, it stayed on if you had turned it on yourself, and some bank apps still refused to open.
- "Debugging off between runs" can't be turned on during a run any more. Before, it stopped the helper in the middle of the run.
- It also waits while another app is using USB debugging.
- A new run that starts while RePair still waits for the car to leave keeps debugging on until the run ends. Before, the car leaving in the new run turned it off mid-run.
- If RePair is stopped during a run, debugging is turned back off the next time RePair starts.
- Picking **Off** as the helper keeps "Debugging off between runs" as you set it. Only Shizuku turns it off.
- The switch in **Settings > Helper** shows the right state when it changes by itself.
- **Connect** works without Wi-Fi when it can.
- Picking Shizuku while Vexer works now asks Shizuku first. If you say no, or Shizuku isn't running, Vexer stays picked and keeps working. Before, Vexer stopped and nothing worked.

## 1.0.51 (2026-10-24)

### Fixed

- Picking the helper again after **Off** connects at once, without the setup guide flashing up.

## 1.0.50 (2026-10-24)

### Fixed

- If you uninstall RePair, Ghostack stops by itself.
- "Debugging off between runs" turns on only when Ghostack is really connected. If it can't, it tells you why.
- If you use Shizuku and back out of pairing, Shizuku stays as it was.
- The Share log button works as soon as there is something in the log.

## 1.0.49 (2026-10-23)

### Fixed

- "Debugging off between runs" works together with another app that has the same option: the last one done turns them off.
- If you turn notifications off when pairing asks, then turn them on, pairing goes on by itself when you come back.
- The "Apps using Ghostack" list is up to date when you come back to Settings.
- The Allow and Revoke boxes follow your light or dark look.
- The Revoke box says which app stops using Ghostack.
- When Ghostack isn't connected on Wi-Fi, it says "Tap Connect".

## 1.0.48 (2026-10-22)

### New

- For bank apps that won't open with Developer options on: **Settings > Helper > Debugging off between runs**.
- Developer options and USB debugging stay off. RePair turns them on only while it runs, and off again after.
- It works only with Ghostack. If you use Shizuku, RePair asks before switching to Ghostack.
- After the phone restarts, connect to Wi-Fi once.
- It's a workaround and may not be stable yet. It's off unless you turn it on.

### Fixed

- Setting up Ghostack on a new phone no longer gets stuck on "connecting".
- Pair waits until you're on Wi-Fi, and says so.
- The pairing notification tells you each step, from turning on Developer options to the code.
- After a restart without Wi-Fi, RePair says Ghostack needs Wi-Fi once.
- Shizuku is offered only when it's installed.

## 1.0.47 (2026-10-22)

### Look

- Icons next to every setting and step, so you see what each one is about at a glance.
- Appearance shows System, Light and Dark with their icons.
- In Help, each message shows an icon: a warning for a problem, an info mark for what is going on, a tick when it worked, a bulb for a tip.
- Every page was checked and tidied: rows, icons and buttons line up evenly.
- The checklist at the top no longer jumps when the app opens.
- Every problem line has a button that fixes it, for example allow notifications, get Tasker or set up the helper.
- "Get Shizuku" opens the store when Shizuku isn't installed.

### Fixed

- Ghostack starts by itself more reliably after the phone restarts, also when you have other apps that use it.
- Wireless debugging is put back the way you had it. Before, it could stay on after a restart.

## 1.0.46 (2026-10-20)

### Helper

- Setting up the helper is easier: RePair picks one for you the first time you open it.
- Tapping the status box does the next step.
- Shorter setup steps that say where to go.

### Look

- Help is easier to read: each part in its own box.

## 1.0.45 (2026-10-20)

### Look

- The status box at the top is easier to tap.

## 1.0.44 (2026-10-19)

### Look

- Button borders are easier to see in dark mode.
- Cards, boxes and borders are easier to see in light mode.

### Helper

- Picking Ghostack, Shizuku or Off shows at once; the switch happens in the background.
- Picking Ghostack again after Off takes your other app's pairing by itself.

## 1.0.43 (2026-10-19)

### Pick your helper

- Choose Ghostack, Shizuku or Off, on the main screen or in Settings > Helper.
- Picked Ghostack? The same box asks how to pair: use the pairing of another of your apps, or a code.
- Picked Shizuku? If it isn't installed or running, RePair tells you what to do first.
- Settings has Appearance (Light, Dark, System) and Helper.
- Settings > Helper lists the apps using Ghostack. Tap Revoke to stop one.

## 1.0.42 (2026-10-18)

### New

- The update card now shows what's new in an update before you tap Update. Long notes scroll inside the card.
- You can turn the update card off in Settings > Updates. It's on.
- After updating, What's new tells you what changed, also for 1.0.41.

## 1.0.41 (2026-10-17)

### Map behind the wheel

- Works again with the newest Android Auto and Google Maps.
- The short route starts without opening Maps on your phone, so you can keep using it, and nothing shows in Recents.
- The route is ended as soon as it starts, so the whole thing takes about 12 s.

### Fixed

- Ghostack now tries a few more times to come back by itself after it drops, for example when you plug in a car's cable or leave a Wi-Fi. Before, it tried once and could stay off until you tapped Fix.

### Changed

- The icons at the top are in a new order: Share the run log, About, Help, Settings. About, Help and Settings sit in the same places as in all our apps.

## 1.0.40 (2026-10-17)

### Fixed

- Ghostack no longer drops after RePair is updated or reinstalled.

## 1.0.39 (2026-10-15)

### More than one car

If you drive more than one car, RePair can now remember all of them.

- Tap **Change** on the car card and tick every car you use.
- RePair uses the car your phone is connected to over Bluetooth.
- You don't have to choose your car again when you switch cars.
- The card's title shows **Connected car** or **Last connected car**.

### Each car remembers its Wi-Fi

Before, RePair could wait for nothing when your phone was on another Wi-Fi, like a weak home
Wi-Fi.

- After Android Auto connects once, RePair remembers that car's Wi-Fi.
- Next time, it waits only when your phone is really on your car's Wi-Fi.
- If your car's Wi-Fi changes (for example after a car update), open the car list and tap the
  unlink icon next to it.

### Wi-Fi and Bluetooth during a run

These three settings are now on:

- **Disconnect Wi-Fi if connected**
- **Block saved networks during the run**
- **Turn Bluetooth off and on before connecting the car**

They help your car connect: your phone leaves other Wi-Fi networks, and the car's Bluetooth
connects again from the start. You can turn them off in **Settings > Before a run**.


### When Android Auto doesn't connect

- RePair now checks if your car's Wi-Fi is nearby and tells you what it found.

## 1.0.38 (2026-10-13)

- Ghostack setup is now right under the status at the top of the main screen, the same as in my
  other apps. Tap the status to jump to it.
- Ghostack now reconnects by itself right after USB debugging is switched back on (for example
  after Masker), instead of showing "connecting..." when you open the app.
- Ghostack also reconnects by itself right after RePair updates.
- While an app that blocks debugging is open (for example a banking app with Masker), Ghostack
  waits and doesn't switch debugging back on. RePair shows "Paused while a protected app is open".

## 1.0.37 (2026-10-12)

### New: Ghostack, RePair's own helper

**What it is:** RePair changes a few phone settings that normal apps can't change, like the Wi-Fi
country and airplane mode. To do that, it needs a helper with more rights. Ghostack is that
helper, built into RePair.

**Why use it:** before, RePair needed the Shizuku app, and Shizuku stops every time the phone
restarts. Ghostack starts again by itself after a restart, when the phone joins Wi-Fi.

**How to set it up (once, no computer needed):**

1. Connect your phone to Wi-Fi.
2. Open RePair and tap **Pair**. If Developer options are off, RePair shows you how to turn them
   on.
3. In Wireless debugging, tap **Pair device with pairing code**.
4. Type the code into RePair's notification.

Already set up Ghostack in another of my apps? Tap **Use Ghostack pairing**, then **Allow**. No
code needed.

You can still use [Shizuku](https://shizuku.rikka.app/) if you prefer: **Settings > Helper**.

### Also in this version

- Map behind the wheel no longer touches Google Maps when it's already navigating, so a route
  you started keeps going.
- New installs: "Disconnect Wi-Fi if connected" and "Block saved networks during the run" are now
  on from the start. If you already use RePair, your settings stay as they are.
- RePair's notifications now always show in full, with an "Open RePair" button, and they clear
  when you open RePair.

## 1.0.33 (2026-10-09)

- Map behind the wheel is back. Google Play Protect no longer blocks installing RePair because
  of it. Turn it on in Settings > During a run.

## 1.0.32 (2026-10-09)

- Map behind the wheel is removed for now: Google Play Protect started blocking RePair from being
  installed because of it. It may come back once it works without that. Everything else works as
  before.
- After an update that skips versions, the "What's new" title now says "What's new since your
  last update", so older news isn't shown as part of the newest version.
- "What's new" now lists the newest changes first.

## 1.0.31 (2026-10-09)

- The message "RePair (version) is available" now comes back each time you open RePair, until
  you tap Update or Later. Before, it showed only once and was easy to miss.
- After an update that skips versions, "What's new" now shows everything you missed, not only
  the most important points.

## 1.0.30 (2026-10-09)

- Only for Map behind the wheel: Google Maps no longer adds a new place to its history every
  time.
- Only for Map behind the wheel: Google Maps no longer says "You've arrived" when you start
  near the place where you first used it.

## 1.0.29 (2026-10-09)

- New: Map behind the wheel (Settings > During a run, off by default). Made for the Renault
  Austral, which shows the map behind the steering wheel only after a navigation has started:
  when Android Auto connects, RePair starts a short Google Maps navigation on the car screen and
  ends it after 2 s, so the map stays there. It works with the phone locked and opens nothing on
  the phone. It takes about 15 s, as Google Maps counts down before it starts.
- Turning the car off and on again quickly no longer makes RePair cut Android Auto's connection:
  RePair now waits for Android Auto to reconnect by itself.

## 1.0.28 (2026-10-08)

- RePair can start your Samsung routines: one when a run starts and one when it ends. Pick them
  in Settings > Samsung routines. Only routines that you start manually can be picked.
- Settings is easier to read: each group now sits in its own card.
- The "What's new" message is shorter and easier to read.

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
