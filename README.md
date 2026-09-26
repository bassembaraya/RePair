# RePair

**Fixes wireless Android Auto on phones whose Wi-Fi country blocks the car's 5 GHz channel.** No root needed.

[Download the latest version](../../releases/latest) · [What's new](CHANGELOG.md)

## The problem

Wireless Android Auto runs over 5 GHz Wi-Fi. Your phone decides which Wi-Fi channels it may use
from the country of the mobile network it sees. In some countries (Egypt, for example) the channel
some cars use, like channel 149 on Renault, isn't allowed. The phone can't join the car's Wi-Fi,
and Android Auto never connects.

## What RePair does

With one tap, RePair makes the phone briefly forget the mobile network's country, so Wi-Fi switches
to the phone's own fallback country (e.g. India), which opens the 5 GHz channels. It reconnects the
car, waits for Android Auto to connect, and turns your mobile network back on. Android Auto keeps
working after that, because the phone doesn't change the Wi-Fi country while it's connected.

The run takes about 30 seconds (up to 2 minutes with a slow car). If anything fails, or you tap
Stop, airplane mode is turned back off so you keep your mobile signal. If Android Auto is already
connected, RePair does nothing.

## Requirements

- Android 12 or newer. Tested on a Samsung Galaxy S24 Ultra (Android 16).
- [Shizuku](https://shizuku.rikka.app/) installed and running. It has to be started again after
  every phone restart.
- A phone CSC (region software) whose country allows the car's channel, e.g. **INS** (India).
  RePair checks this for you.
- The car paired with the phone over Bluetooth.

## Install and set up

1. Download `RePair-x.y.z.apk` from [Releases](../../releases/latest) and install it (allow
   installing from your browser or file manager if Android asks).
2. Start Shizuku (Shizuku app, then Start, with Wireless debugging).
3. Open RePair and allow Shizuku permission.
4. Tap **Choose**, allow Nearby devices, and pick your car.
5. The checklist on the main screen shows anything still missing.

## Ways to run it

- **The button** in the app: *RePair Android Auto*. You can watch every step and a log.
- **Quick Settings tile**: edit your Quick Settings panel and add the *RePair* tile. One tap runs it
  in the background (the phone must be unlocked).
- **App shortcut**: long press the RePair icon, then *Run RePair*.
- **Samsung Modes and Routines**: add an action: Apps, *Open an app or do an app action*, RePair,
  *Run RePair*.
- **Tasker**: a plugin action *RePair* that returns:
  - `%repair_status`: `success`, `skipped` (Android Auto was already connected) or `fail`
  - `%repair_result`: the final message, or the reason it failed
  - `%repair_airplane`: `true` if the run used airplane mode, `false` if it stopped before that
  - and *Check status*, which reads `%repair_country`, `%repair_5ghz` and `%repair_fallback`
    without changing anything.

To see how a background run went, turn on a toast or notification in **Settings, Run results**.

## Settings

- **Turn off Wi-Fi if connected** (off by default). Without it, a connected Wi-Fi stops the run.
- **Run results**: toast and notification, each Off, Failures only or Always.
- **Theme**: Light, Dark or System.

## Tips

- **Samsung**: switching USB to file transfer can stop Shizuku. To avoid it, dial `*#0808#` in the
  Phone app and choose **MTP + ADB**.
- The in-app **Help** screen explains every step and every error message.

## Privacy and battery

- No internet permission: RePair never sends anything anywhere.
- Nothing runs in the background unless you start a run. The tile and shortcut don't keep anything
  running either.
- The log is kept in memory only and is gone when the app closes.

## About

RePair is made by Bassem Baraya. This repository only holds the app's releases and notes; the
source code isn't published. Found a problem? Open an issue here with what happened and, if you
can, a screenshot of the log.
