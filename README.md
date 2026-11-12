# Cookie Lab — QA2 Basic

A minimal static site for CookieYes banner QA testing against the **QA2** environment,
for a **Basic-plan** site. Dark violet theme; every page shows a `QA2 · Basic` tag in the nav.

**Live:** https://arunshaju-mozilor.github.io/cookie-lab-qa2-basic/

## Pages

| Page | Purpose |
|---|---|
| `index.html` | **Cookie Lab** home page — loads real third-party trackers and sets cookies in every category on load, with a live consent-status dashboard |
| `about.html` | About page for multi-page navigation tests |
| `privacy-policy.html` | Privacy policy (linked from banner) with the auto cookie policy placeholder |
| `cookie-policy.html` | Renders the CookieYes cookie policy for the QA2 account |
| `terms-and-conditions.html` | Terms and Conditions page — heading only, blank body |

## CookieYes script

The QA2 Basic scripts are not wired in yet. Every page except `cookie-policy.html` has a
commented-out banner tag in `<head>`; uncomment it and fill in the QA2 CDN host and client ID:

```html
<script id="cookieyes" type="text/javascript"
  src="https://QA2_CDN/client_data/YOUR_CLIENT_ID/script.js">
</script>
```

`cookie-policy.html` has a commented-out `.../client_data/YOUR_CLIENT_ID/cookie-policy/script.js` tag.

## Hosting

GitHub Pages: **Deploy from a branch → `main` → `/` (root)**.
Pushing to `main` redeploys the site within a minute or two.

Use https://arunshaju-mozilor.github.io/cookie-lab-qa2-basic/ as the domain when adding the website
in the QA2 CookieYes dashboard.
