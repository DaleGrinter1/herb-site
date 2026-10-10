# Teaching portfolio template

A small static portfolio inspired by the reference site's structure. All pages
share `styles.css`. There is no JavaScript, framework, package installation, or build step.

The evidence pages use the three supplied Evidence Set documents, including their
reflections, source excerpts, tables and embedded images. The homepage uses the
supplied headshot. The supplied Introduction document provides the biography, teaching values and
contact details; the display name is Herb Zhou as confirmed by the owner.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | About me, introduction, evidence links, and contact |
| `philosophy.html` | Teaching philosophy and references |
| `evidence.html` | Overview of the three evidence domains |
| `evidence-1.html` | Professional Knowledge |
| `evidence-2.html` | Professional Practice |
| `evidence-3.html` | Professional Engagement |
| `evidence-template.html` | Copyable starting point for another evidence set |
| `styles.css` | Shared design settings and layout |
| `assets/images/` | Portraits and other images |
| `assets/documents/` | Evidence documents |

## Free hosting with GitHub Pages

This project is connected to https://github.com/DaleGrinter1/herb-site.
GitHub Pages can publish the static site from the public repository for free.
The `.nojekyll` file tells GitHub to serve the HTML and assets directly.

After committing and pushing the website files, open the repository's Settings
and select Pages. Under Build and deployment, choose Deploy from a branch,
select `main` and `/ (root)`, then Save. The expected site address is
https://dalegrinter1.github.io/herb-site/.

For later updates, commit and push the changed website files to `main`.
Keep local source documents out of the publishing commit unless they are intended
for public access; the site's download documents are in `assets/documents/`.

## Preview locally

Open `index.html` in a browser. Navigation works without a server.

Alternatively, if Python is installed, run this from the project folder:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000 and press Ctrl+C in the terminal to stop the server.

## Customise the design

Open `styles.css` and edit the variables in `:root` at the top.
Colours, fonts, content widths, section spacing, and corner radius are shared by all pages.
For example, change `--color-accent` to change the main blue link colour.
The pink, lilac, blue, yellow, and green variables control decorative pastel accents.
The homepage lettering is editable HTML; change `--color-portfolio` for its dark
blue colour. The letters sit straight. Remove the `portfolio-banner` div if unwanted.
Save the file and refresh the browser.

Keep text/background combinations readable. The heading font uses fonts already
on the visitor's device, so there are no external font downloads.

The layouts automatically become one column on small screens. Navigation remains
visible rather than depending on a scripted menu.

## Replace the sample content

1. Replace `Your Name` in the title, header, and footer of every HTML page.
2. Replace the bracketed writing prompts with the owner's approved content.
3. Update the page descriptions in each file's head section.
4. Confirm the teaching domains and standards match the intended portfolio.
5. Replace the contact placeholders with approved public details.
6. Remove the `template-notice` element from every page once the content is complete.
7. Review short introductory text and headings so they reflect the owner's voice.

In HTML text, write `&amp;` for an ampersand and `&lt;` for a less-than symbol.

To add a portrait, put `portrait.jpg` in `assets/images/` and replace the
contents inside the `portrait-placeholder` div on the homepage with the following.
Keep the outer div to retain the pink frame; remove it for a plain image.

```html
<img src="assets/images/portrait.jpg"
     alt="Portrait of Your Name"
     width="600" height="750">
```

Use the image's actual dimensions in the width and height attributes.

## Add an evidence document

1. Put the approved file in `assets/documents/`, for example `learning-plan.pdf`.
2. Open the appropriate evidence page and find `EVIDENCE BLOCK START`.
3. Replace the title and caption with a meaningful description.
4. Replace the `document-status` paragraph with a real file link:

```html
<p><a href="assets/documents/learning-plan.pdf">Open learning plan (PDF)</a></p>
```

The browser's settings determine whether a PDF opens or downloads. To offer a
separate download link for a locally hosted file, add:

```html
<p><a href="assets/documents/learning-plan.pdf" download>Download learning plan (PDF)</a></p>
```

For an image preview, replace the `document-placeholder` div with:

```html
<img src="assets/images/learning-plan-preview.jpg"
     alt="Learning plan showing the activity sequence and teaching goals"
     loading="lazy" width="900" height="1200">
```

Provide an accurate description and the actual image dimensions. Keep a text
caption as well. The template uses links for PDFs rather than embedded viewers
so the page stays simple and works across browsers.

To add more evidence, copy the entire figure between the evidence block comments.
Use unique IDs such as `document-2`, update the figure number, and add the matching
standards table row. A link such as `href="#document-2"` points to that document.

Files on a public static site can be accessed directly by URL. Restricted evidence
needs an access-controlled hosting or storage arrangement before upload.

## Add another evidence page

1. Copy `evidence-template.html` to a descriptive name, such as `family-partnerships.html`.
2. Edit its title, description, heading, evidence-set number, focus, and standards.
3. Replace every writing prompt and update the figure numbers.
4. Update the previous/next links at the bottom.
5. Copy a card in `evidence.html`, then change its title, description, and link.
6. Optionally add a matching homepage card.

Header and footer HTML are deliberately repeated so every page works independently
without a build tool. If you change the main navigation, update it in every HTML
file, including the blank template. The evidence navigation item stays active on
individual evidence pages because they belong to that section.

## Comments

The same labels are used throughout:

- `EDIT:` identifies content or settings a maintainer can change.
- `SHARED HEADER / FOOTER:` identifies markup repeated across pages.
- `EVIDENCE BLOCK START / END:` marks a block that can be copied.
- CSS section comments explain the responsibility of each group of rules.

Prefer comments that explain intent and editing boundaries. Update a comment
when you change the behaviour it describes.

## Before publishing

- Replace all writing prompts, names, contact details, and template notices.
- Confirm evidence and standards mappings with the owner.
- Open every page and document link.
- Check a phone-sized screen and navigate using Tab and Enter.
- Check that captions, image descriptions, and headings make sense.
- Print-preview an evidence page if reviewers may need a paper copy.

## Hosting and handover

Any host that serves static HTML files can serve this site. There is no build command.
Publish the six visitor pages, `styles.css`, and approved files inside `assets/`,
keeping their relative paths unchanged. The root entry point is `index.html`.

Do not upload `evidence-template.html`, instructions, README files, browser artifacts,
or unused working documents as visitor content. The blank page remains available
in the source project for maintainers to copy.

A hosting provider and domain have not been selected, and this template has not
been deployed. Once selected, add the exact publishing steps here.

Keep the source in version control and give another maintainer access. Save the
previous working version before making changes. Keep this guide current so the
next person can follow the same process.


## Supplied evidence and portrait

The homepage headshot is `assets/images/herbFace.jpg`. Each evidence page contains
the wording from its matching `evidence/Evidence Set N.docx` source. Download copies
live in `assets/documents/evidence-set-N.docx`; extracted images live in
`assets/images/evidence-set-N/`. Source excerpts are expandable for easier reading.

When revising evidence, update the page text and its download copy together.
The standards labels on the homepage and evidence overview match the supplied
artefacts. The original files in `evidence/` are retained unchanged.

## Introduction content

About Me and the learning journey use `assets/documents/Introduction.docx`.
The philosophy page summarises the values described in that introduction.
Herb Zhou is the confirmed display name; the introduction?s opening name was
updated accordingly. Contact links use the two supplied email addresses and phone
number. The student ID is retained in the original document.
