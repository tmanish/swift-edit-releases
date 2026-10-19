# SwiftEdit user guide

A short tour of SwiftEdit. The complete guide is in the app under Help ▸ SwiftEdit Help.

## Getting started

Open any text file with File ▸ Open (⌘O), or drag it onto SwiftEdit in the Dock. To work
with a whole project, choose File ▸ Open Folder (⇧⌘O). The folder appears in the sidebar
next to your open and recent documents.

When SwiftEdit starts with nothing open, the start screen offers a new document, Open,
Open Folder, and your recent files. Press Return to start typing in a new document.

## Make SwiftEdit your default editor

Choose Settings ▸ General ▸ Default editor (or the link on the start screen), pick the kinds
of files you want, and click Make SwiftEdit the Default. Those files then open in SwiftEdit
when you double-click them. SwiftEdit needs to be in your Applications folder first.

IDE code like Swift or C, and web pages, keep their current apps. You can still open them
in SwiftEdit with Finder's Open With.

## Saving and your safety net

SwiftEdit saves a file only when you choose File ▸ Save (⌘S). Until then, it keeps a private
recovery copy of every document with unsaved changes, a couple of seconds after you stop
typing. If your Mac or the app ever quits unexpectedly, your work comes back the next time
you open SwiftEdit.

Quitting doesn't nag you, either. With Settings ▸ Files ▸ Restore unsaved changes on
relaunch turned on (the default), SwiftEdit keeps your unsaved work and reopens it exactly
where you were. Your files on disk aren't touched until you save. Turn the setting off if
you'd rather be asked about each document when you quit.

## Writing in Markdown

Markdown files open with three views at the top of the window:

- **Edit** shows only the text.
- **Split** puts the text and a live preview side by side.
- **Preview** shows only the formatted result.

The sidebar lists your headings, so you can jump around a long document. File ▸ Print and
Export as PDF use the formatted version. Images load from the document's own folder only,
never from the internet.

## Finding things

| To | Do this |
|---|---|
| Find in the current document | ⌘F, then ⌘G for the next match |
| Find and replace | ⌥⌘F |
| Search every file in a folder | Find in Folder (⇧⌘F) |
| Open a file by typing part of its name | Open Quickly (⌥⌘O) |
| Jump to a heading or function | Go to Symbol (⌃6) |
| Go to a line number | ⌘L |
| Run any command by name | Command Palette (⇧⌘P) |

## Cleaning up text

Text ▸ Text Actions holds one-step tools: sort lines, remove duplicates, filter lines that
match a word or pattern, change case, reflow paragraphs, straighten quotes, and format or
validate JSON. Each one works on the selection, or on the whole document when nothing is
selected, and a single Undo reverses it.

## Earlier versions of a file

Every time you save, SwiftEdit keeps the previous version. Choose File ▸ File History to
compare an earlier version with what you have now, or restore it. Restoring is one step
you can undo, and nothing is written to disk until you save.

History is made only when you save, never when you just open a file. To turn it off or
clear it, use Settings ▸ Files. See [PRIVACY.md](PRIVACY.md) for exactly what's kept.

## Encodings and line endings

SwiftEdit keeps a file's encoding, line endings, and final newline exactly as they were,
even in a file that mixes Windows and Mac line endings. The status bar shows each of these.
Click one to change it. Nothing is converted unless you ask.

## Big files

Large files open quickly, with some features paused to keep things responsive. A banner says
exactly what's paused. Files over 64 MB open read-only until you choose Edit Anyway, and
files over 128 MB can't be opened.

## Updates

Choose SwiftEdit ▸ Check for Updates, or let SwiftEdit check once a day after you allow it.
Turn automatic checks on or off in Settings ▸ General. Updates install only when you agree.
See [PRIVACY.md](PRIVACY.md) for exactly what an update check sends.

## Troubleshooting

**"SwiftEdit can't be opened."** Make sure you're opening the copy in Applications, downloaded
from this repository's Releases page. Don't disable Gatekeeper to work around it. If it keeps
happening, [open an issue](https://github.com/tmanish/swift-edit-releases/issues).

**macOS asks whether SwiftEdit can use its existing data.** This can appear when replacing an
older test build. Allow it to keep your settings and recovery copies.

**A new version doesn't seem to start.** Quit SwiftEdit before replacing it, and open it from
Applications, not from the disk image or an old Dock shortcut.

## Uninstalling

Quit SwiftEdit and move it from Applications to the Trash. To remove its settings and
recovery copies too, delete `~/Library/Containers/com.swiftedit.SwiftEdit`. Your documents
stay where you saved them.
