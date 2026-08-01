---
title: "Support"
description: "Help with Nitpitch — tuning tips, troubleshooting, and how to get in touch."
---

Nitpitch is a hobby project, maintained in spare time. Bug reports and
suggestions are welcome — the fastest route is
[a GitHub issue](https://github.com/vlumi/nitpitch/issues), or email
[ville@misaki.fi](mailto:ville@misaki.fi).

## Using it

Play a note and the dial fills toward the side you're off on: **left is flat,
right is sharp**. In tune, the fill disappears and only the centre needle
remains — nothing showing is the goal.

The row of lights underneath is the fine reading. They're spaced
logarithmically — ±2, 4, 8, 16, 32 cents — so there's real resolution near the
centre, where tuning actually happens, and just direction out at the edges.

Set the **reference pitch** with the − and + either side of the reading below
the dial. Set the **instrument** from the menu at the top left; it narrows the
frequency range being searched, which is what keeps a cello's low C from being
found as a violin harmonic. **Chromatic** searches the whole range and names
whatever it hears.

## It says "Play a note" and nothing happens

- **Check the microphone permission.** iOS: Settings → Nitpitch → Microphone.
  macOS: System Settings → Privacy & Security → Microphone.
- **Watch the level bar** at the top of the screen. If it doesn't move when you
  play, the app isn't hearing anything — a different input device may be
  selected, or something else may have the microphone.
- **Play a bit louder, or closer.** Frames that aren't confidently periodic are
  deliberately ignored rather than displayed, so bow noise and room reflections
  don't make the readout flicker nonsense.

## The reading jumps around

A little movement is the instrument, not the app — vibrato and bow noise both
move the pitch genuinely. But:

- **Two strings sounding at once** will give an unstable reading that flickers
  between them. This includes an open string ringing sympathetically. Damp the
  strings you're not tuning.
- **A very slack string** may read as an entirely different note. That's
  correct — it *is* a different note — so keep raising it and the name will
  come round.

## It disagrees with my other tuner

Check both are set to the same **reference pitch** first. An app at A=440
against one at A=442 will differ by about 8 cents on every note, consistently.
That's not an error in either one: it's what those two references mean.

## Which instruments are supported

Violin, viola, cello, double bass, guitar, and bass guitar, plus a chromatic
mode that will name any note in range. The detector is the same for all of
them; the instrument choice only sets the frequency range searched.

Nitpitch is built violin-first — that's the case every default is chosen for —
but nothing about it is violin-only.

## Requirements

iPhone and iPad on iOS 16 or later, and Mac on macOS 14 or later. One purchase
covers all of them, though there's nothing to purchase: the app is free.

On the Mac, an electric instrument through an audio interface or DI usually
gives a much cleaner signal than the built-in microphone, which is
voice-processed and noisier than the detector deserves.
