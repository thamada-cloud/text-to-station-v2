# text-to-station-v2

> **Publish mirror.** The source lives in the private iheartradio/UXD repo at `prototypes/text-to-station-v2`. This repo only exists to serve the pages publicly, so edit the source there and copy it here. Edits made here get overwritten.
>
> Live page https://thamada-cloud.github.io/text-to-station-v2/design-f.html

A separate copy of [`text-to-station-prototype`](../text-to-station-prototype) for exploring a new Talkback and text flow. Nothing here links back to the original, and the original is left untouched.

The new direction is `design-f.html`, built from the Figma "Option 1" flow ([Text to Station, Section 1](https://www.figma.com/design/5mvQCUXzqyffkOogeoEdAV/Text-to-Station?node-id=3345-14801)). It started from `design-c.html` and reuses that file's station page, illustration, icons, recording engine and permission dialogs.

## Files

| File | What it is |
| --- | --- |
| `design-f.html` | The new flow. Station or Contests banner (or the mic button) opens a Talkback intro with Send Talkback and Send Text. Talkback asks for the microphone (Don't Allow shows Microphone Disabled), then runs the existing design-c recording screens, then a dark success screen with an optional contact form. Send Text is a single message form that leads to the same success screen in light. Both end on a push notification primer. |
| `design-a.html` to `design-e.html`, `index.html` | Unchanged copies of the original directions, kept for reference. |

## Notes

No build step. Open a file directly, or serve the folder with any static server.

The mic and notification prompts follow the device. iOS alerts show on desktop and iPhone, Material dialogs on Android.

Choices made where the Figma was silent
* Submit stays dimmed until there is something to send, on both the text form and the contact form.
* Allow Once records this time only and asks again next time.
* The recording screens (countdown, recording, review with Try Again and Send) are design-c's, reused without changes. Closing one returns to the Talkback intro.
