# Conversation Epi — announcement page

**Domain:** https://conversationepidemiology.com
**Message:** AI hears. Humanity understands.

A single static page. No scripts, no build step, no dependencies.

## Files to upload

- `index.html` — the page
- `styles.css` — styling
- `favicon.svg` — tab icon
- `CNAME` — custom domain for GitHub Pages / Netlify

The photos (`AliJaved.jpg`, `AliJaved.HEIC`, `BobGramling.jpg`, `DonnaRizzo.png`) are not used on this page — leave them out of the upload. Browsers can't display the `.HEIC` original anyway.

## Preview locally

```bash
cd ~/Desktop/AskApple/ConversationEpideimology
python3 -m http.server 8000
```

Open http://localhost:8000.

## Host on GitHub Pages (free)

1. Create a public GitHub repo named `conversationepidemiology` and upload the four files above.
2. Repo **Settings → Pages** → Source: **Deploy from a branch** → `main` / `/ (root)` → Save.
3. In GoDaddy (**My Products → conversationepidemiology.com → Manage DNS**), remove the parking A records and add:

   | Type | Name | Value |
   | --- | --- | --- |
   | A | `@` | `185.199.108.153` |
   | A | `@` | `185.199.109.153` |
   | A | `@` | `185.199.110.153` |
   | A | `@` | `185.199.111.153` |
   | CNAME | `www` | `your-github-username.github.io` |

4. In GitHub Pages settings, set **Custom domain** to `conversationepidemiology.com`, save, then enable **Enforce HTTPS** once DNS resolves.

Alternative: drag the four files to https://app.netlify.com/drop, then add the custom domain under **Domain settings** and use the DNS values Netlify shows.

## Before publishing

- Add a contact link when you're ready (there is none on the page yet).
- Confirm the domain spelling: `conversationepidemiology.com` is the one registered with GoDaddy.
