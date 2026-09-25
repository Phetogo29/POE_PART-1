# Khaya Animal Shelter Website

**Module:** Web Development (WEDE5020) - Portfolio of Evidence
**Student:** Phetogo Komane (ST10502851) | **Class:** DISD0601 | **Lecturer:** Mr Morne

## 1. Project information
A five-page, responsive website for **Khaya Animal Shelter**, a community animal shelter in Benoni, Gauteng. The site helps visitors learn about the shelter and adopt, donate, volunteer or make contact.

- **Part 1:** research, proposal, sitemap and semantic HTML pages.
- **Part 2:** external CSS styling for desktop, then responsive styling for tablet and mobile.

**Technologies:** HTML5 and CSS3 only (Grid, Flexbox, custom properties, media queries). No frameworks, libraries or JavaScript.

**Target audience:** animal lovers, pet owners, adopters, volunteers, donors and the local community.

## 2. Pages
| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Introduction, key figures, calls to action |
| About Us | `about.html` | History, mission, vision, values |
| Get Involved | `get-involved.html` | Adoption listings, donation details, volunteer sign-up form |
| Gallery | `gallery.html` | Photos of animals and shelter activities |
| Contact | `contact.html` | Address, phone, email, opening hours, message form |

## 3. Folder structure
```
khaya-shelter/
  index.html  about.html  get-involved.html  gallery.html  contact.html
  css/style.css          shared external stylesheet
  images/                logo, hero, adoption and gallery photos
  screenshots/           screenshots used in this README
  README.md  .gitignore
```

## 4. Setup instructions
No build step or installs are needed.
1. Clone the repository: `git clone <repository-url>` and open the folder.
2. Make sure the `images/` folder contains the files listed in section 9.
3. Open `index.html` in any modern browser (Chrome, Firefox or Edge), or in VS Code right-click `index.html` > **Open with Live Server**.
4. To test responsiveness, press **F12**, turn on the device toolbar and try widths of about 1280px (desktop), 768px (tablet) and 390px (mobile).

## 5. Screenshots
| View | Screenshot |
|---|---|
| Home - desktop | ![Home desktop](screenshots/home-desktop.png) |
| Home - tablet | ![Home tablet](screenshots/home-tablet.png) |
| Home - mobile | ![Home mobile](screenshots/home-mobile.png) |
| Get Involved - desktop | ![Get Involved desktop](screenshots/get-involved-desktop.png) |
| Get Involved - mobile | ![Get Involved mobile](screenshots/get-involved-mobile.png) |
| Gallery - desktop | ![Gallery desktop](screenshots/gallery-desktop.png) |
| Contact - mobile | ![Contact mobile](screenshots/contact-mobile.png) |

## 6. Documentation - how the CSS works
`css/style.css` is linked in the `<head>` of every page and is divided into commented sections:
1. **Reset + tokens** - universal reset and `:root` variables for colours, fonts, sizes and spacing (green, brown, white and cream, as proposed in Part 1).
2. **Typography** - Aptos/Arial set once on `body`; a 1.25 type scale in `rem`; weight, line-height and letter-spacing on headings.
3. **Page layout** - `grid-template-areas` gives header / main / footer; Flexbox for header and navigation; sections are full-width bands with content held to 70rem.
4. **Components** - buttons, stat tiles and cards, with `:hover`, `:focus` and `:active` states.
5. **Forms + tables** - labelled inputs with visible focus styles; bank details table.
6. **Responsive** - desktop-first breakpoints (see below).

**Classes used (8):** `.skip-link`, `.lead`, `.split` (two columns), `.btn`, `.alt`, `.stats`, `.cards`, `.callout`. Everything else is styled through element selectors and inheritance.

| Breakpoint | Width | Changes |
|---|---|---|
| Desktop | above 64em | 2-column sections, 3-column cards, sticky header |
| Tablet | 64em and below | 2-column cards, smaller headings and spacing |
| Mobile | 40em and below | single column, stacked header and nav, full-width buttons, stacked table rows |

**Accessibility:** skip link, one `<h1>` per page, `aria-current` on the active link, labelled form fields, visible focus outlines, `prefers-reduced-motion` respected.

**Code commenting:** every HTML file has a header comment and a comment before each major block (header, section, form, table, image). The stylesheet has a header and numbered section comments.

## 7. Known limitations
- Forms have no back-end: the contact form opens the visitor's email client and the volunteer form does not send data.
- Bank details and some shelter figures are placeholders.
- No JavaScript yet, so there is no gallery lightbox or mobile menu toggle.

## 8. Version control
All source files are committed to the repository:
```
git add .
git commit -m "Part 2: external CSS, README, changelog and code comments"
git push origin main
```

## 9. Images required
`images/cat-and-dog-logo.avif`, `cat-and-dog-playing.webp` (plus `-480.webp` and `-800.webp` resized copies), `about.jpg`, `gallery-1.jpg` to `gallery-6.jpg`, `adopt-bella.jpg`, `adopt-simba.jpg`, `adopt-rocky.jpg`, `adopt-whiskers.jpg`, `adopt-buddy.jpg`, `adopt-luna.jpg`.

## 10. Changelog
All edits made after Part 1 feedback, 24 September 2026.

### Feedback: "README is empty and no source code pushed"
| # | File | Change | Reason |
|---|---|---|---|
| A | `README.md` | Written in full: project information, pages, folder structure, setup instructions, screenshots, CSS documentation, limitations, image list | The README was empty. |
| B | `screenshots/` | Folder added for README screenshots | Feedback asked for screenshots. |
| C | All `.html`, `css/style.css` | Header comments and section-by-section comments added | Feedback asked for appropriate code commenting. |
| D | Repository | All source files (HTML, CSS, README, `.gitignore`) committed and pushed | No source code had been pushed. |
| E | `.gitignore` | Added | Keeps system files and zips out of the repository. |

### Corrections to Part 1
| # | File | Change | Reason |
|---|---|---|---|
| 1 | `getinvolved.htm` -> `get-involved.html` | Renamed | Every nav link pointed to `get-involved.html`, so the page could not be reached. |
| 2 | All pages | Same skip link, header (logo + `<nav>` list), `aria-current="page"` and footer on every page | Pages were inconsistent: plain header on index/contact, a different class-based header on about/gallery, an `<h1>` in the header on get-involved. |
| 3 | All pages | Logo path unified to `images/cat-and-dog-logo.avif` | Three different paths/files were used. |
| 4 | `get-involved.html` | Main title `<h2>` -> `<h1>`; header no longer contains an `<h1>` | One `<h1>` per page and correct heading order. |
| 5 | `index.html` | Content wrapped in `<section>`s; added "Get involved" and "Contact us" buttons | Semantic structure; buttons promised in the proposal. |
| 6 | `get-involved.html` | Animals wrapped in `<article>`; removed `<br>`, `border="1"`, `cols`; submit input -> button | Presentation moved into CSS. |
| 7 | `contact.html` | Form fields grouped in `<p>`; page split into sections | Same as above. |
| 8 | `about.html` | Removed inline `style`; values -> `<article>` cards; mission and vision in own section | No inline styles. |
| 9 | `gallery.html` | Lightbox buttons -> `<figure>`/`<figcaption>`; removed "click to enlarge" and placeholder note | Lightbox needed JavaScript not part of this submission. |
| 10 | `about.html`, `gallery.html` | Removed `js/script.js`, nav-toggle button, `<span id="year">` | `script.js` does not exist; broken script reference. |
| 11 | `index.html`, headers | Removed fixed `width` attributes | Sizes now set in CSS. |
| 12 | All footers | Removed "NPO registration placeholder"; one shared footer with `<address>` | No placeholder text on the site. |

### Part 2 additions
| # | File | Change |
|---|---|---|
| 13 | `css/style.css` | New external stylesheet (reset, variables, typography, Grid/Flexbox, components, forms, tables, tablet + mobile breakpoints). |
| 14 | All pages | `<link rel="stylesheet" href="css/style.css">` added. |
| 15 | `index.html` | Hero image uses `<picture>` with `srcset`/`sizes`. |