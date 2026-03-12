# 99 Bottles of Beer — Feature Documentation

> **Audience:** This document is written for non-technical users and stakeholders. No coding knowledge is required to understand it.

---

## 1. Feature Summary

**99 Bottles of Beer** is a web page that automatically displays the lyrics to the classic sing-along song *"99 Bottles of Beer on the Wall."* It exists as a straightforward, self-contained demonstration that generates and shows song content without any manual input from the user. Anyone who can open a web browser can use it — no account, login, or installation is required.

---

## 2. How It Works

When you open the page in a web browser, the page immediately begins building the song lyrics and displaying them on screen. Starting from 100 and counting all the way down to 0, the page adds one line at a time — each line reading "[number] bottles of beer on the wall" — until every line has appeared. The entire list loads instantly when the page opens; there is no waiting or loading spinner. Once the page has finished, all 101 lines are visible and the page is complete.

---

## 3. How to Use It

1. **Open the page.** Locate the file named `index.html` and open it with any modern web browser (Chrome, Firefox, Safari, or Edge all work).
2. **Wait for it to load.** The page will display the song lyrics automatically. No buttons need to be clicked and nothing needs to be typed.
3. **Read the lyrics.** Scroll down the page to see all the lines of the song, from 100 bottles down to 0.
4. **To restart or refresh,** simply reload the page in your browser (usually by pressing F5 or clicking the circular arrow icon in your browser's toolbar). The lyrics will regenerate and display again from the top.

> **Note:** The page works entirely offline. No internet connection is required once you have the files.

---

## 4. Configuration & Settings

This feature currently has **no user-facing settings panel or controls.** All behavior is fixed at the time the page was built. The table below describes what is locked in and what effect it has:

| Setting | Current Value | Effect |
|---|---|---|
| Starting number | 100 | The song begins at "100 bottles of beer on the wall" |
| Ending number | 0 | The song counts all the way down to "0 bottles of beer on the wall" |
| Step size | Counts down by 1 each line | Every number between 100 and 0 appears — none are skipped |

To change any of these values, the underlying page files would need to be edited by a developer.

---

## 5. Known Limitations & Edge Cases

The following are known gaps between what this page does and what a user might naturally expect:

- **Only one line per verse.** The real song has a multi-line verse structure: the number is announced, then repeated, then the "take one down, pass it around" line follows. This page shows only the opening line of each verse. The rest of the verse does not appear.
- **Starts at 100, not 99.** The project is named "99 Bottles," but the page actually starts counting from 100. The traditional song begins at 99.
- **Grammar is always plural.** Every line says "bottles" (plural), even when the count reaches 1 or 0. A user will see "1 bottles of beer on the wall" and "0 bottles of beer on the wall" rather than the grammatically correct "1 bottle" or "no more bottles."
- **No interactivity.** There is no way to pause the display, jump to a specific number, or change the starting point from within the page itself.
- **No visual feedback during loading.** On most devices the page loads so fast that this is unnoticeable, but on a very slow device the lyrics might appear to "pop in" with no progress indicator.

---

## 6. Troubleshooting

| Problem | Likely Cause | What To Do |
|---|---|---|
| The page opens but no lyrics appear — just a blank white page | The browser may have blocked the page's scripts from running, or the files may have been moved and some are now missing | Make sure all the original files are in the same folder together and have not been renamed or moved. Try a different browser. If the problem persists, see "Who to Contact" below. |
| The page shows an error message instead of lyrics | A required file is missing or the page could not find it | Check that the folder contains both the `index.html` file and a sub-folder called `js` with the script files inside it. Do not rename or relocate any files. |
| Only some of the lines appear (song cuts off early) | The browser tab was closed or the page was navigated away from before loading finished | Reload the page and let it finish completely before scrolling or clicking away. |
| The lyrics look broken or unstyled (numbers appear as plain text with no spacing) | [NEEDS ENGINEERING INPUT] A stylesheet referenced in the page may be missing or inactive | Try reloading the page. If the appearance remains wrong, contact the team (see below). |
| The page does not open at all | The file may not be associated with a browser on your computer | Right-click the `index.html` file, choose "Open with," and select a web browser (Chrome, Firefox, Edge, or Safari). |

---

## 7. Who to Contact

If you have tried the troubleshooting steps above and the problem is not resolved, please gather the following information before reaching out:

1. **What you expected to happen** — describe what the page should have shown.
2. **What actually happened** — describe exactly what you saw (or did not see).
3. **Which browser and version you used** — e.g., "Chrome 122 on Windows 11." (You can find this in your browser's Help > About menu.)
4. **Whether the problem happens every time or only sometimes.**
5. **A screenshot of the page if possible.**

Send this information to the project's development team. Based on the project records, the original developers are **David Wynn** and **Amber Ward.** Contact them through whatever channel your organization uses for bug reports or support requests.

---

*Document prepared for non-technical stakeholders. Last reviewed: March 2026.*
