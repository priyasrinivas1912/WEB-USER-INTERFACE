
# My First Web Page

A simple webpage built using separate **HTML**, **CSS**, and **JavaScript** files. It demonstrates the basic structure of an HTML document and shows how `localStorage` can save data that survives page reloads and browser restarts.

## Files

| File         | Purpose                                                      |
|--------------|---------------------------------------------------------------|
| `index.html` | Page structure/content (head, body, button, message area)    |
| `style.css`  | Visual styling (colors, layout, card design)                  |
| `script.js`  | Page behavior — handles clicks and saves data with `localStorage` |

## How to run it

1. Keep all three files in the **same folder**.
2. Double-click `index.html` (or right-click → Open with → your browser).
3. No server or installation needed — it just runs in the browser.

## What it does

- Click the **"Click me!"** button to see a rotating welcome message.
- Every click is counted and saved using `localStorage.setItem()`.
- **Refresh the page** — the click count is still remembered, because `localStorage` data is *not* cleared on reload.
- **Close the browser completely and reopen the file** — the count is still there. `localStorage` persists until it's explicitly cleared (it has no expiry).

## Key concept: localStorage

```javascript
// Save a value (always stored as a string)
localStorage.setItem("clickCount", 5);

// Read a value back (returns null if it doesn't exist)
localStorage.getItem("clickCount");

// Remove a value
localStorage.removeItem("clickCount");
```

`localStorage` is different from a normal JavaScript variable because it survives page reloads, browser restarts, and even computer restarts — the data stays until it's manually cleared (via code, or by clearing browser site data).

## Notes

- Data saved here is specific to this file's location and to the browser you open it in. Opening it in a different browser (or from a different folder/server) will not show the same saved data.
- To reset the click count, open the browser console and run `localStorage.removeItem("clickCount")`, or clear the site's storage from browser settings.
