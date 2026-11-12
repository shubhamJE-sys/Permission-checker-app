# PermCheck

Test app that shows every Android permission and special access, lets you ask for it,
tests that it really works, and builds a bug report to send to Claude.

## Build
Push this project (or the zip in the repo root) to a GitHub repo. The workflow in
`.github/workflows/build.yml` builds `PermCheck.apk` (artifact `PermCheck-apk`).
The APK is signed with `app/permcheck.keystore` (keep that file; new builds then install as updates).

## Bug report process
1. Open a row's **Ask** (pop-up) or **Open settings** (special access) and change the permission.
2. Press **Test** on the row (or **Test all**) to see if it really works.
3. If something is wrong, tick **Bug** on that row and write what happened.
4. Optionally write a general note at the top.
5. Press **Copy report** (or **Share report**) and paste it to Claude.

The report holds: phone and Android version, every status, last test results,
flagged bugs with your notes, an event log (asks, answers, status changes, with timings)
and the last crash, if any.
