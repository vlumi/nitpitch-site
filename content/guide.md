---
title: "Guide"
description: "How to use Nitpitch on iPhone, iPad, and Mac — what each screen shows, and what every state means."
url: /guide/
---

Nitpitch is built to explain itself, so this page is less a manual than a tour: what each screen is for, and what the states you'll see actually mean. Everything here applies to iPhone, iPad, and Mac alike; the few places the Mac differs are marked. The watch has [its own page](/guide/watch/) — same ideas, different hands.

## The launch screen

{{< figure src="/img/guide/launch-iphone.png" alt="The chromatic tuner above the instrument list" class="shot" >}}

The app opens on the **chromatic tuner**: play anything and it names the nearest note, with the error in cents. Below it sit **your instruments** — starred ones lead, each with one-tap chips for its pinned presets — and two doors: *All instruments…* and *All presets…*.

{{< figure src="/img/guide/listening-iphone.png" alt="The tuner waiting, showing Play a note" class="shot" >}}

**"Play a note"** means the tuner is listening but nothing confident is sounding. It is deliberately picky: bow noise, room rumble, and the gap between notes are filtered out rather than shown, so when a number appears you can trust it. If it says this while you're playing, get closer to the microphone or pluck a little harder.

## Reading the readout

The note name is the nearest note; the **cents** say how far you are from it — negative is flat, positive is sharp, and ±5¢ counts as in tune (that's when things turn green). The dot strip below is the same story at a glance: the lit dot walks outward as the error grows, doubling its distance per dot, and the centre dot means done. For the last fraction of a cent, the **strobe band** shows error as motion — crawling right is sharp, left is flat, standing still is true.

## An instrument: a dial per string

{{< figure src="/img/guide/grid-iphone.png" alt="The violin grid with two strings sounding" class="shot" >}}

Choose an instrument and every string gets its own dial, lit only by pitches near its own target — so a wildly flat string still lights *its* dial, not a neighbour's. Bow or pluck **two adjacent strings at once** and the interval chip appears: the pulse rate it shows is the beating you hear between the strings' shared harmonics, and it stills exactly as the interval comes true. That is how violinists tune fifths, rendered on screen.

## The string view

{{< figure src="/img/guide/string-view-iphone.png" alt="One string's dial with steppers and the strobe" class="shot" >}}

Tap a dial to work on one string: a big dial, the target note with − / + steppers (nudging a target relabels the tuning *Custom* — the name follows the pitches), a speaker to sound the reference tone, and the strobe band. Swipe sideways or use the arrows to walk strings.

{{< figure src="/img/guide/follow-iphone.png" alt="The Follow toggle lit in the string view" class="shot" >}}

The **location arrow** is the Follow toggle: lit, the screen walks to the string you're actually playing — a brushed neighbour never steals it, only a string played on purpose, and a *sympathetic ring* (an unmuted string singing along) never qualifies. Off by default, because a screen must never jump while you're mid-turn on a peg.

## Harmonics

{{< figure src="/img/guide/harmonic-iphone.png" alt="The readout labelled 3rd harmonic" class="shot" >}}

Touching a string's node instead of playing it open — the 12th-fret harmonic, or the 7th-fret one — works without any mode: the error shown is still the string's own, and the readout says *· 2nd harmonic* or *· 3rd harmonic* so the screen and your ear agree about what's sounding. Where a harmonic is genuinely ambiguous between two strings (on a violin, D's 3rd harmonic *is* the A's octave), the tuner stays silent rather than guessing.

## The intonation check

{{< figure src="/img/guide/intonation-iphone.png" alt="The intonation panel showing a delta" class="shot" >}}

For fretted instruments' setup work: toggle the intonation layer from the grid's toolbar, play a string open, then at the 12th fret (or its harmonic). Each sample locks once it has *held* — a wobbly attack or a stray resonance can't pollute it — and the **Δ** is the verdict: how far the octave sits from where the open string promises it. Positive means the octave is sharp; on a guitar, the saddle wants to move back. Re-play either note after an adjustment and the newer sample simply replaces the older.

## Presets and pins

{{< figure src="/img/guide/presets-iphone.png" alt="The All presets browser" class="shot" >}}

A **preset** is a setup under your name — pitches, and optionally the reference and temperament it was saved with. The built-in tunings (Drop D, DADGAD, Open G…) arrive as ordinary presets: rename, delete, share, or pin them like your own. A **pin** binds a preset to one instrument as a launch-screen chip — instrument and setup, one tap. In any preset list, the **⊜ mark** shows the row you're already on: tapping it would change nothing.

{{< figure src="/img/guide/share-iphone.png" alt="The share sheet with QR code and link" class="shot" >}}

**Sharing** a preset gives a link and a QR code carrying the whole setup — strings, reference, temperament. Nothing but the setup travels, and never through any server of ours.

## Reference and temperament

The reference steps a hertz at a time, A=390 through 466 — 440 by default, 442–443 for many European orchestras, 415 for baroque. Temperament decides how string targets divide their intervals: **pure fifths** is the default on bowed instruments, because beatless fifths tuned by ear *are* pure; everywhere else it's equal, the temperament frets are cast in. Each instrument carries its own reference and temperament; the chromatic tuner's A lives in Settings.

## iCloud sync

{{< figure src="/img/guide/settings-sync-iphone.png" alt="Settings with the iCloud Sync switch" class="shot" >}}

Off by default — nothing leaves your device until you flip it. On, your instruments, presets, and favorites stay the same on every device signed into your iCloud, merged **setting by setting**: two devices edited apart both keep their changes, an unstar sticks everywhere, and a fresh device adopts your existing setup instead of announcing its factory state. Audio is never part of it; there is no server of ours.

## On the Mac

Everything above, plus: an **audio interface or DI** beats any microphone — plug an electric instrument straight in for the cleanest signal the detector will ever see. **Escape** walks up a level, the keyboard's answer to the phone's edge swipe. And in a wide window the grid can show **strips** instead of dials — a Settings toggle, with the low string at the bottom or the top as you prefer.
