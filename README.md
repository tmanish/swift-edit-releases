<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/swiftedit-icon-dark.png">
    <img src="assets/swiftedit-icon.png" width="128" height="128" alt="SwiftEdit app icon">
  </picture>
</p>

<h1 align="center">SwiftEdit</h1>

<p align="center">A calm, native editor for text, code, and Markdown on the Mac.</p>

> **About this repository:** this is where SwiftEdit's releases, update feed, and user guide
> live. SwiftEdit's source code is private and isn't published here.

SwiftEdit sits between TextEdit and a full IDE. Open a file and start working. There's no
project to set up, no account, and nothing to configure first. It's free, it runs entirely
on your Mac, and it's careful with your files: the encoding, line endings, and final newline
you opened with are the ones you save with.

## What you can do with it

- Write Markdown in Edit, Split, or Preview, with a heading outline, printing, and PDF export.
- Edit code and configuration files with syntax coloring for Swift, Python, JavaScript, Go,
  Rust, and about twenty more languages and formats.
- Find and replace in a document, or search every file in a folder at once.
- Jump to any file with Open Quickly, and to any heading or function with Go to Symbol.
- Clean up text in one step: sort and filter lines, change case, reflow paragraphs, format JSON.
- Compare two documents, or a document with its last saved version.
- Pick up where you left off. Unsaved work survives crashes, and it can survive quitting too.

## Requirements

macOS 14 Sonoma or later, on Apple silicon or Intel.

## Download and install

1. Download the latest `.dmg` from [Releases](https://github.com/tmanish/swift-edit-releases/releases/latest).
2. Open it and drag SwiftEdit to the Applications folder.
3. Eject the disk image, then open SwiftEdit from Applications.

Each release is signed with the developer's Apple Developer ID and notarized by Apple.

What each download is:

- **`SwiftEdit-VERSION-BUILD.dmg`** is the app. This is the one to download.
- **`.dmg.sha256`** is the file's checksum, if you want to confirm the download is intact.
- **`.md`** holds that version's release notes, which SwiftEdit shows when it offers an update.
- **Source code (zip / tar.gz)** links are added automatically by GitHub to every release.
  They contain only this repository's documentation, app icon, and update feed, not
  SwiftEdit's source code, which is private.

Releases labeled **Pre-release** are test builds used to check the update process before a
public version ships. They look for updates on a separate test feed, so they won't receive
regular updates. Please use the latest release without that label.

## Updates

SwiftEdit can look for new versions on its own. It asks you first, and you can change your
answer any time in Settings ▸ General. To check right now, choose SwiftEdit ▸ Check for Updates.

Nothing is downloaded or installed until you say so. Every update is verified against the
developer's signature before it's installed. With Restore unsaved changes on relaunch turned
on (the default), documents you hadn't saved reopen after the update.

## Privacy

Your documents never leave your Mac through SwiftEdit, and nothing about you or how you use
the app is collected. SwiftEdit goes online for one reason: checking for updates.
[PRIVACY.md](PRIVACY.md) spells out exactly what that involves and what the app keeps on your Mac.

## Help

- [User guide](HELP.md)
- In the app: Help ▸ SwiftEdit Help, and Help ▸ Keyboard Shortcuts

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/tmanish/swift-edit-releases/issues).
Please describe the problem rather than attaching documents with private content.

## License

SwiftEdit is free to download and use. It includes [Sparkle](https://sparkle-project.org) for
updates, used under its MIT license; the full notice ships inside the app.
