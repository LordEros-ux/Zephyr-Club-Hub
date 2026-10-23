# Club Hub

A small admin site for a literary club with a core team, four domains (Design, PR, Operations, Sponsorships) and six sub-clubs (Reading, Creative Writing, Oratorical Union, Cultural, Translation & Media, Theatre).

Built with plain HTML, CSS and JavaScript. No build step, no backend.

## Features

- **Members:** add and remove members, each with one role, one domain and any number of sub-clubs. Search and filter by role, domain or sub-club.
- **Domain tasks:** one column per domain. Assign tasks, set due dates, and click the status button to move a task through To do, In progress and Done.
- **Events:** create events for a sub-club and mark attendance for that sub-club's members.
- **Summary:** member counts by domain and sub-club, open tasks and upcoming events.
- **Export:** download members and events as CSV.
- Burgundy, cream and gold theme based on the club artwork.

Data is saved in your browser with `localStorage`, so it stays on your device.

## Run it

Open `index.html` in a browser.

## Put it online with GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Branch**, choose `main` and `/ (root)`, then save.
4. Your site appears at `https://<your-username>.github.io/<repo-name>/`.

## Ideas for next steps

- Add a screenshot to this README
- Edit existing members, tasks and events
- Sponsorship pipeline (Contacted, Negotiating, Confirmed)
- Replace `localStorage` with a real database so the whole team shares one set of data

## Password gate

The site asks for a password before showing anything. The password is stored only as a SHA-256 hash in `index.html` (`PASS_HASH`).

To change it, run `printf '%s' 'your-new-password' | sha256sum` and paste the result into `PASS_HASH`.

**Limitation:** this runs entirely in the browser, so it keeps casual visitors out but is not real security. Anyone who can read the page source can bypass it, and the code in a public repo is visible to everyone. Don't put sensitive data in this version. For real protection, use a private repo with a host that supports access control (Cloudflare Access, Netlify password protection) or add a backend.
