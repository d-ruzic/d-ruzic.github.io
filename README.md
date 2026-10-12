# druzic.com

Source of Dimitrije Ruzic's academic website. GitHub Pages rebuilds and
publishes the site automatically about a minute after every `git push`.
Live at https://druzic.com.

## Where to edit what

| To change… | Edit |
|---|---|
| About, Teaching, Contact text | `index.md` (plain text with light Markdown) |
| Papers (add / reorder / update links) | `_data/papers.yml` (instructions at the top) |
| Name, title, email, CV file | `_config.yml` |
| PDFs (papers, CV) | put the file in `papers/`, link it as `/papers/<name>.pdf` |
| Colours, fonts, spacing | `assets/css/style.css` (`--accent` = the blue) |
| Photo, background sketch, visitor counter | `_config.yml` (`photo`, `intro_bg`, `goatcounter`) |

To update the CV: copy the new `Ruzic_CV_Web.pdf` over `papers/Ruzic_CV_Web.pdf`,
then commit and push.

## Rules that keep the site reachable from China

- Host PDFs here in `papers/`, not on Dropbox or Google Drive (both blocked).
- Never add Google Fonts, Google Analytics, YouTube embeds, or other
  third-party scripts/styles. Plain *links* to such sites are fine.
- The one script on the page, the GoatCounter visitor counter, is a copy kept
  in `assets/js/count.js` (GoatCounter's own script address is blocked in
  China). Visitor statistics: https://druzic.goatcounter.com
