# d-ruzic.github.io — personal academic website

## What this is

Source of Dimitrije Ruzic's academic website. It replaces the Google Site at
`druzic.com`, which is unreachable from China (all Google domains are blocked
there). Live now at **https://d-ruzic.github.io**; the goal is to serve it at
**druzic.com** once the user is happy with it.

- Repo: `github.com/d-ruzic/d-ruzic.github.io` (public — required for free GitHub Pages)
- Local: `~/projects/d-ruzic.github.io` (created on Livia, 2026-10-11)
- Hosting: GitHub Pages, "legacy" build from `main` / root. GitHub runs Jekyll
  itself; every `git push` republishes in ~1 minute.
- Domain: `druzic.com`, registered at **Namecheap**.

## The user

Economist (Associate Professor, INSEAD); expert in the domain, new to the
command line, Git, and web tooling. Explain web/DNS concepts from first
principles, with everyday analogies. See also `~/projects/coffeeproject/CLAUDE.md`.

## Requirements (from the user)

1. Lin Tian–style site (coauthor's https://lin-tian.github.io/ — Jekyll
   "Personal"/grayscale theme)
2. Reachable from China
3. Secure / safe
4. Easy to edit
5. Default address `druzic.com`

## Layout of the repo

| File | Holds |
|---|---|
| `index.md` | About, Teaching, Contact text (Markdown inside `<section markdown="1">` blocks) |
| `_data/papers.yml` | All papers: `working:` and `published:` lists; editing instructions at top |
| `_includes/papers.html` | Liquid template that renders papers.yml (title, authors, journal, Abstract toggle, link buttons) |
| `_layouts/default.html` | Page shell: fixed nav, full-screen intro, footer |
| `_config.yml` | Name, position, email, CV path, description, `url`; kramdown `auto_ids: false` |
| `assets/css/style.css` | All styling; colours as variables in `:root` (`--accent` = link colour) |
| `assets/fonts/` | Self-hosted Lora (variable + italic) and Montserrat (variable) woff2, latin subset |
| `papers/` | The 8 PDFs the old site linked: 7 papers + `Ruzic_CV_Web.pdf` |
| `README.md` | Short "where to edit what" for the user (excluded from the build) |

The site is one scrolling page (like Lin's), no JavaScript. Abstracts use
HTML `<details>`.

## Design decisions (keep these)

- **No third-party resources on the page.** No Google Fonts, Google Analytics,
  YouTube, CDNs (jsDelivr is also unreliable in China), Font Awesome, etc.
  Fonts were downloaded once and live in `assets/fonts/`. Plain outbound
  links (NBER, CEPR, DOI, Google Scholar) are fine.
- **PDFs hosted in the repo, not Dropbox** (Dropbox is blocked in China). The
  source copies live in `Dropbox/Public/Website/` (`/mnt/d/Dropbox/...` on
  Livia). Only files the old site linked were copied; six unlinked older files
  in that folder (2012/13 syllabi, research/teaching statements, older VW
  drafts) were deliberately left out.
- Hosting inside mainland China would need an ICP licence (Chinese entity) —
  not an option; GitHub Pages + custom domain is the standard workaround.
- Ruby/Jekyll is **not installed locally**, so there is no local preview;
  pushing to GitHub is the preview. Check builds with
  `gh api repos/d-ruzic/d-ruzic.github.io/pages/builds/latest`.
  (Optionally install Ruby + Jekyll later for local previews — needs sudo.)

## Content source

Copied verbatim on 2026-10-11 from the Google Site (`www.druzic.com`: `/home`,
`/research`, `/teaching`, CV link). The old site had no photo.

## Done (2026-10-11)

- Built the Jekyll site (Lin-style dark grayscale look), all content migrated
- Self-hosted fonts and PDFs; verified the live page loads zero external resources
- Created the GitHub repo, Pages enabled, site live at d-ruzic.github.io;
  verified all 9 papers, 7 abstracts, every PDF, CSS and fonts return 200
- Fixed two first-build bugs (empty paper lists — Liquid nested lookup; duplicate
  heading ids)

## Still to do

1. **User reviews the site** (desktop + phone) and asks for changes. Ideas raised:
   - background photo for the intro (e.g. Fontainebleau bouldering), as in
     Lin's theme — put it in `assets/img/`, keep it < ~300 KB
   - headshot in the About section
   - accent colour: light theme with dark royal blue `#1f3c88` is the default (2026-10-12)
   - intro background: pale blue pencil-style sketches of Pobednik made from
     Wikimedia Commons photos (CC BY-SA, so the footer credits the photographer
     and licence). Trials `/preview-bg-kalemegdan/` and `/preview-bg-sava/` await
     a verdict; to adopt one, move its `intro_bg:` block into `_config.yml`.
     Sketch recipe (Pillow, colour-dodge): scratchpad scripts, not in repo
   - possibly show the user 2–3 alternative layouts/themes before settling
2. **Point druzic.com at the site** (only when the user is happy):
   - In the repo: add a file `CNAME` containing `druzic.com`; set
     `url: "https://druzic.com"` in `_config.yml`; push.
     Or set the custom domain via repo Settings → Pages (creates the same file).
   - At Namecheap → Domain List → druzic.com → Advanced DNS:
     - delete the current URL-redirect record(s) and anything else pointing to
       Google Sites (today: bare `druzic.com` hits a Namecheap redirect server at
       162.255.119.76 that only works over http; `www` goes to Google Sites)
     - add 4 **A** records, host `@`: `185.199.108.153`, `185.199.109.153`,
       `185.199.110.153`, `185.199.111.153`
     - (optional) 4 **AAAA** records, host `@`: `2606:50c0:8000::153`,
       `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
     - **CNAME** record, host `www` → `d-ruzic.github.io.`
   - Recommended: verify the domain in GitHub (profile Settings → Pages →
     Add a domain → TXT record at Namecheap) to prevent domain takeover.
   - Wait for DNS (minutes to a few hours), then tick **Enforce HTTPS** in
     repo Settings → Pages. Check both `https://druzic.com` and
     `https://www.druzic.com` work (bare https is broken on the old setup).
3. **Test from China**: e.g. `17ce.com` or `ping.chinaz.com` (load the page
   from servers in several Chinese cities).
4. **Retire the Google Site** (unpublish it) once druzic.com serves the new site.
5. Clone on the other machines when needed:
   `gh repo clone d-ruzic/d-ruzic.github.io ~/projects/d-ruzic.github.io`
   (Tiberius, Diocletian), and update the repo lists in coffeeproject's CLAUDE.md.

## Progress log

| Date | Milestone |
|---|---|
| 2026-10-11 | Site built and published at d-ruzic.github.io (from a coffeeproject session on Livia) |
