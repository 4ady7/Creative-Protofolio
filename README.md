# Shady Nashed — Portfolio

A static personal site: home, projects, contact, a video demonstration, and a short site report. It is plain HTML and CSS, with no build step and no JavaScript.

## Pages

| Page | File | What it is |
| --- | --- | --- |
| Home | `index.html` | Short introduction |
| Projects | `project.html` | Four project cards |
| Contact | `contact.html` | A form that opens the visitor’s email app |
| Video | `videoDemo.html` | Embedded walkthrough of the site |
| Site report | `siteReport.html` | Notes on what was learned, plus validation screenshots |

## View it locally

The pages are in `visual studio code files copy`. From the repository root:

```bash
cd "visual studio code files copy"
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

Opening `index.html` directly in a browser also works. A local server is the more reliable option, because the video embed and Google Fonts load over the network.

## Layout

Styles are split so shared rules stay separate from the two screen sizes.

- `main.css` is loaded on every screen: type, color, header, cards, form, and the report.
- `desktop.css` applies at `800px` and wider. The logo and links share one bar, and projects sit in two columns.
- `mobile.css` applies below `800px`. Navigation is a full-screen menu opened from the icon in the header.

The breakpoint is `799px` / `800px`, so the two files never apply at the same time.

## Project structure

```text
visual studio code files copy/
├── index.html
├── project.html
├── contact.html
├── videoDemo.html
├── siteReport.html
├── main.css
├── desktop.css
├── mobile.css
├── project-1.svg … project-4.svg
└── Screenshot*.png
```

Project covers are local SVG files. The screenshots in the site report are the validation images linked from that page.
