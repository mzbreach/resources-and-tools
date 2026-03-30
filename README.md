# Red Teaming and OT Security Resource Hub

A curated MkDocs site focused on red teaming, OT/ICS security, physical security crossover, RFID research, and ethical security learning.

This repository is meant to serve as a clean, navigable collection of publicly available resources for beginners and intermediate learners who want a structured starting point. The emphasis is on **context, reputable references, and responsible use** rather than operational attack guidance.

## What this site covers

The site currently includes pages for:

- **Communities** — forums, subreddits, Discord servers, and other places to learn from practitioners
- **Researchers** — notable individuals, organizations, and labs worth following
- **Tools** — commonly referenced security and research tools, organized by category
- **Writeups and Case Studies** — public incident analyses, blog posts, and educational technical writeups
- **Events and Conferences** — conferences, villages, talks, and archives
- **Rabbit Holes** — interesting subtopics that are worth deeper exploration
- **Obscure Resources** — niche references, blogs, newsletters, and smaller communities
- **Starter Projects** — safe beginner-friendly project ideas for building hands-on skill
- **RFID Research** — references related to Proxmark3, RFID ecosystems, and community troubleshooting resources

## Project goals

This project is designed to be:

- **Beginner-friendly** without being shallow
- **Useful to intermediate learners** who want curated jumping-off points
- **Ethically framed** around authorized testing, research, and defensive understanding
- **Easy to extend** with additional markdown pages and curated links over time

## Ethics and scope

All content in this repository is intended for **legal, authorized, and educational** use only.

This project does **not** aim to provide unauthorized intrusion guidance. In particular:

- Only perform testing against systems you own or have explicit written permission to assess.
- OT/ICS systems can have real-world safety consequences; lab-first learning matters.
- Physical and RFID research should be conducted within legal and ethical boundaries.
- Community links are included as references and learning resources, not endorsements of every post or technique discussed there.

## Running the site locally

This repository uses [MkDocs](https://www.mkdocs.org/) with the Material theme.

A simple local workflow looks like this:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
pip install mkdocs mkdocs-material pymdown-extensions
mkdocs serve
```

Then open the local address shown in your terminal, usually `http://127.0.0.1:8000`.

To build the static site:

```bash
mkdocs build
```

## Repository layout

```text
.
├── README.md            # Repository landing page
├── mkdocs.yml           # Site configuration and navigation
└── docs/
    ├── README.md        # Homepage for the published site
    ├── communities.md
    ├── researchers.md
    ├── tools.md
    ├── writeups.md
    ├── conferences.md
    ├── rabbit-holes.md
    ├── obscure-resources.md
    ├── starter-projects.md
    └── rfid.md
```

## Editing and adding content

Most content changes only require editing markdown files in `docs/`.

A few practical conventions that help keep the site consistent:

- Use a short introductory paragraph at the top of each page.
- Group links into clear thematic sections.
- Keep summaries concise and explanatory.
- Prefer public, reputable, and stable sources when possible.
- Frame sensitive topics around research context, ecosystem understanding, and defensive value.

If you add a new page, remember to also add it to the `nav:` section in `mkdocs.yml`.

## Deployment

This repository is configured as an MkDocs-based GitHub Pages site. Once GitHub Pages and the repository workflow are configured, pushes to the main branch can be used to publish updates.

Key files involved in deployment and site behavior:

- `mkdocs.yml` — site name, theme, navigation, and plugins
- `docs/` — page content
- `.github/` — repository automation and update configuration

## Notes

This is a personal educational resource hub and does not represent any employer, institution, or organization. External links are provided for reference and learning convenience.
