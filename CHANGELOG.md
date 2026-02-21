# Earleaf Changelog

## 1.0.0-beta.5 — February 21, 2026

### New Features

- **Automatic sleep timer.** Configure a time window (e.g. 9 PM to 7 AM) and the sleep timer will activate automatically whenever you start listening during that period. The auto-timer fires once per book session and never overrides a manually set timer.
- **Home screen shortcut.** Long-press the app icon for a "Resume listening" shortcut that jumps straight into your last-played book.
- **Collection cover mosaics.** Collections now show a 2x2 grid of book covers instead of a single cover, giving you a better visual overview. User-set covers are still shown as a single image.
- **Delete books.** You can now delete a book and all its data from the book detail overflow menu.
- **Sleep timer memory.** The sleep timer picker now remembers your last used duration instead of always defaulting to 30 minutes.

### Improvements

- Ignored books are now tracked by content fingerprint, so they stay ignored even if renamed or moved between syncs.

### Bug Fixes

- Fixed incorrect duration detection for some M4B files where Android reported wildly wrong values (e.g. ~1204 hours instead of ~16 hours).

---

## 1.0.0-beta.4 — February 18, 2026

### New Features

- **Bookmarks.** You can now add bookmarks while listening and jump back to them later. Bookmarks are managed directly from the player screen.
- **Pull-to-refresh.** Quickly refresh your library by pulling down on the library screen — no need to go into settings.
- **Sleep timer fade out.** A new setting that gradually fades out audio when the sleep timer ends, for a smoother transition to silence.
- **Smarter collection creation.** When importing books that are nested inside a single-book wrapper folder, the wrapper is now automatically collapsed so your collections stay clean.
- **Page Sync transcription control.** Toggling Page Sync on or off now properly pauses and resumes any in-progress transcriptions.

### Bug Fixes

- Fixed an issue where duplicate books could appear after a library sync.
- Fixed grouped (multi-file) book detection failing when the file system returned files in a different order.
- Single M4B files that don't have embedded cover art now fall back to using the folder's cover image, if one exists.

---

## 1.0.0-beta.3 — February 17, 2026

### Improvements

- **Sleep timer overhaul.** The "end of chapter" timer is now more reliable, pause/resume behavior has been improved, and you can set custom durations beyond the preset options.

### Bug Fixes

- Fixed playback controls (play/pause, skip) not responding after the app is restarted while media hasn't loaded yet.
- Fixed the progress bar snapping incorrectly when rewinding past a chapter boundary.
- Fixed top-level book directories incorrectly creating empty collections during library scan.

---

## 1.0.0-beta.2 — February 16, 2026

### New Features

- **Multi-backend support.** Added a LibrarySource abstraction layer that lays the groundwork for connecting to external audiobook servers in future releases.
- **Mark as Completed.** You can now manually mark a book as completed from the book detail overflow menu.
- **Transcription management.** Book details now include a transcription section showing the current Page Sync transcription status, with options to start, retry, or remove transcriptions.
- **Transcription notifications.** Tapping a transcription progress notification now opens the transcription list directly.
- **Automatic transcription retry.** Failed transcriptions are now automatically retried with exponential backoff, and orphaned transcriptions are resumed on app startup.

### Improvements

- Remaining time for in-progress books in the library now correctly reflects the current playback speed.
- Book status (not started, in progress, completed) is now derived from listen-through data rather than stored separately, making it more reliable.

### Bug Fixes

- Fixed the progress bar jittering or stuttering on short chapters and when resuming playback.
- Fixed the progress bar not clamping correctly at chapter boundaries for short chapters.
- Fixed an issue where pausing within the first 3 seconds of a chapter wouldn't snap the position back to the chapter start.
- Fixed playback requests being lost if they were sent before the media controller finished connecting.
- Tapping the media notification or lock screen controls now correctly opens the app to the player screen.

---

## 1.0.0-beta.1 — February 16, 2026

### First beta release

Earleaf is now officially in Beta!
