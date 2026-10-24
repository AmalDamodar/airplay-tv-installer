# The settings, and why

The receiver app keeps its settings inside itself. They cannot be changed from a computer, so you set them once on the
TV with the remote. Open the app, choose **Settings** in the left menu.

## The ones that matter

| Setting | Value | Where | Why |
| --- | --- | --- | --- |
| Advertise AirPlay video support | **OFF** | Settings, bottom, Developer group (turn on **Developer options** first) | This is the fix. See below |
| Advertise AirPlay audio support | **ON** | same place | The receiver stays visible to the iPhone's sound and media controls, and sound plays on the TV |
| Server name | your choice | top of Settings | The name the iPhone shows in Screen Mirroring. Change it from the default if you like, for example "Living Room" |
| Start server at boot | ON (default) | Server group | The receiver is ready after the TV starts |
| Run in background | ON (default) | Server group | Keeps it reachable after you leave the app |

Leave everything else at its default unless you have a reason.

## Why "video support" is off

When an iPhone sees a receiver that supports AirPlay **video**, apps like YouTube try a "hand-off": instead of mirroring
the screen, the app asks the TV to play the video itself. On the TV this was built on, that hand-off failed, and the
failure ended the whole session, so the picture on the TV froze or disappeared as soon as YouTube was opened.

With video support switched off, the iPhone does not try the hand-off. It keeps mirroring the screen, and YouTube, Shorts
and other videos play with sound on the TV.

**The trade-off:** the small AirPlay button inside a video app now sends audio only. To put the picture on the TV, use
**Control Center, Screen Mirroring** on the iPhone instead.

## Things that were tried and were not the cause

On the test TV these did not change the problem, so you can leave them alone:

- Turning H.265 (HEVC) off.
- Turning "Allow new connections" off.

## If sound plays on the iPhone and not on the TV

Check that **Advertise AirPlay audio support** is **ON**. With it off, the sound was sent to the phone in testing.

## Changing a setting later

Open the app from the TV's app list, **Settings**, change it. To be safe, choose **Stop** and then **Start** on the Overview screen
afterwards, so the receiver announces itself again with the new settings.

## What was verified

These values were read off the app's own Settings screen on the test TV (screenshot at the top of the README): video
support off, audio support on, ALAC off, AAC on. Mirroring of YouTube, Shorts and videos with sound from an iPhone was
confirmed working by the TV's owner. Other TVs and other iPhone/iPad/Mac models were not tested.
