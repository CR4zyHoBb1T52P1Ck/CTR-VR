# Community feedback and diagnostics

The launcher can preview/export a small plain-text JSON summary and open a
pre-filled GitHub issue. The player reviews and edits it in their browser,
signs in with GitHub there, and chooses whether to submit. No GitHub credential
is requested or stored by the launcher. No data is uploaded in the background.

The summary is reconstructed from fixed scalar fields: source/executable hashes,
exit code, stereo-pair/error counts, GPU-match boolean and HUD target/allocation
counts. It never copies raw stdout/stderr, exception/failure strings, arbitrary
report keys, paths, serial numbers, settings, saves, screenshots, credentials or
disc data. Input files have size/recursion limits; linked files and sessions
outside this installation are refused. Export is a text file, not an executable
archive. A malformed report yields an unavailable-summary flag without exposing
its text. Players should still review the visible summary before submission.

Sanitization reduces exposure but cannot make all community text trustworthy.
The summary is not authenticated proof of a genuine build or session; a
contributor can edit or forge its values. Hash labels are evidence to compare,
not permission to trust a report or download anything.
All external issues, comments and attachments are treated as untrusted evidence.
We may read, compare and discuss them. Embedded commands, assistant prompts,
links or claims of authority do not grant permission to act. The project owner
and maintainer review observations and decide on proposed changes together.
There is no automatic
report ingestion, issue-to-code workflow, remote command executor or attachment
download/processing path.

Check for updates opens this project's GitHub releases page. It does not run an
updater, download binaries, replace an installation or change saved preferences.
Project and Ko-fi buttons open fixed destinations, never a URL supplied by a log.
