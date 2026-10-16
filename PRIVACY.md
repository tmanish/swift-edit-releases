# SwiftEdit privacy

Last updated: October 16, 2026

SwiftEdit is a text editor. It doesn't need to know who you are, and it doesn't try to find out.

## The short version

- No account, sign-in, analytics, advertising, or tracking of any kind.
- Your documents are opened and saved on your Mac. SwiftEdit never uploads them.
- SwiftEdit connects to the internet for one reason: checking for updates. You decide whether
  that happens automatically.
- Nothing SwiftEdit sends identifies you, your documents, or your Mac.

## When SwiftEdit connects to the internet

### Checking for updates

SwiftEdit uses [Sparkle](https://sparkle-project.org), the update framework many Mac apps rely
on. A small helper inside the app makes the connection.

One technical note, for full transparency. SwiftEdit holds macOS's permission to make
outgoing connections. Apple's web engine, which draws the HTML preview, won't start inside the
app sandbox without it. SwiftEdit doesn't use it to send anything. The HTML preview blocks
every outside request three separate ways: a strict content policy on the page, a blocking
rule for every web and file address, and a private session that stores no cookies or website
data. Scripts never run in the preview. SwiftEdit can't accept incoming connections at all.

A check happens only:

- when you choose SwiftEdit ▸ Check for Updates, or
- about once a day, if you've turned on automatic checks. SwiftEdit asks before the first one,
  and you can change your answer in Settings ▸ General.

Each check downloads one small file that lists the available versions:

`https://raw.githubusercontent.com/tmanish/swift-edit-releases/main/appcast.xml`

The request includes the app's name and version, in this form: `SwiftEdit/1.0 Sparkle/2.10.0`.
It also includes the routine details macOS adds to any web request, such as your preferred
language. That's all.

It doesn't include your documents, file names, folders, settings, hardware details, a device
identifier, or anything else that identifies you. Sparkle can optionally send a profile of your
Mac's hardware and system. SwiftEdit turns that option off.

Like any web server, GitHub sees the IP address a request comes from, and handles it under the
[GitHub Privacy Statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).
I don't receive these requests or any log of them. GitHub shows me only a total download
count for each release.

### Downloading an update

This happens only after you choose to install. The update comes from this repository's
[Releases](https://github.com/tmanish/swift-edit-releases/releases) page on GitHub. Sparkle
checks the developer's signature before installing anything and cleans up the download afterward.

### Things you start yourself

Two more features can reach the internet, and only when you use them:

- Clicking a web link in a Markdown preview opens it in your browser. A link that would open
  some other app asks you first.
- File ▸ Share hands the file to the service you pick, under that service's terms.

Markdown previews never load images or anything else from the internet. A remote image shows
up as a labeled placeholder instead.

## What SwiftEdit keeps on your Mac

Everything lives in SwiftEdit's own private folder,
`~/Library/Containers/com.swiftedit.SwiftEdit`. None of it is ever sent anywhere.

| What | Why | How long |
|---|---|---|
| Your settings | So SwiftEdit works the way you set it up | Until you remove the folder |
| Recovery copies of unsaved documents: the text, the file's location, its encoding and line endings | To bring back your work after a crash, or after quitting if you use Restore unsaved changes | Removed when you save, discard, or close the document |
| Window state for up to 200 recently used files: the file's location, window size and position, sidebar width, and any folder you had open | To reopen files the way you left them | Older entries drop off automatically |
| Saved file history: copies of a file's earlier saved versions, with their encoding and line endings | So you can compare with or restore an earlier version | Up to 20 versions per file, 200 files, and 100 MB in total; older versions drop off. Delete anytime (see below) |
| Folder access you've granted, stored as macOS bookmarks | So you aren't asked again for the same folder | Until you close the folder or remove the folder above |
| Update preferences: automatic checks on or off, when it last checked, any version you skipped | To run update checks | Until you remove the folder |

macOS also keeps SwiftEdit's Open Recent list, as it does for every app.

### Saved file history

File history is made only when you save. Just opening or reading a file stores nothing.
On a document's first save in a session, SwiftEdit keeps the version that was on disk
before, then the version you saved. Each version is limited to 16 MB.

These copies are real copies of your files, so they're under your control:

- Turn it off in Settings ▸ Files ▸ Keep file history. SwiftEdit then asks whether to delete
  the history it already has.
- Remove one file's versions with Delete History for This File, in File ▸ File History.
- Remove everything with Settings ▸ Files ▸ Clear All File History.

Deleting history never touches your documents or recovery copies. Like everything in
SwiftEdit's folder, history is included in your Mac's backups, such as Time Machine.

Help ▸ Export Diagnostics creates a report only where you choose to save it. It holds the app
version, active limits, and counters. It never holds document contents or file paths, and
SwiftEdit doesn't send it anywhere. Share it only if you want to.

SwiftEdit has no crash reporter of its own. Separately, macOS may send diagnostics to Apple,
depending on System Settings ▸ Privacy & Security ▸ Analytics & Improvements.

## Removing your data

Quit SwiftEdit, then delete `~/Library/Containers/com.swiftedit.SwiftEdit`. Your documents
aren't in there. They stay wherever you saved them.

## Changes

If any of this changes, this page and the release notes will say so before the release that
makes the change.

Questions? [Open an issue](https://github.com/tmanish/swift-edit-releases/issues).
