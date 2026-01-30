# Research Lab - Public Log Website

This website serves as the public research log and knowledge base for our Research Lab.

We document ongoing work-in-progress updates, decisions, and lessons learned so results are easy to track over time and simple for new researchers to pick up. Each project page links to relevant code, datasets, experiment artifacts, and meeting logs to promote reproducibility and smooth handovers.

## Website Structure

- **Home** (`index.md`) - Overview and quick links
- **People** (`people.md`) - Lab members and their contributions
- **Projects** (`projects.md`) - Summary of all research projects
- **WIP Log** (`wip-log.md`) - Latest work-in-progress entries across all projects

### Directories

| Directory | Description | README |
|-----------|-------------|--------|
| `people/` | Individual lab member pages | [people/README.md](people/README.md) |
| `projects/` | Individual project pages | [projects/README.md](projects/README.md) |
| `wip/` | Work-in-progress log entries | [wip/README.md](wip/README.md) |
| `assets/` | Images, icons, and other static files | - |

## Quick Start Guides

### Adding a New Person

1. Copy `people/TEMPLATE.md`
2. Rename to `firstname__lastname.md` (lowercase, double underscore)
3. Remove `published: False` from frontmatter
4. Fill in the frontmatter and content sections

See [people/README.md](people/README.md) for detailed instructions.

### Adding a New Project

1. Copy `projects/TEMPLATE.md`
2. Rename to `<project-slug>.md` (lowercase, hyphens)
3. Remove `published: False` from frontmatter
4. Fill in the frontmatter and content sections

See [projects/README.md](projects/README.md) for detailed instructions.

### Adding a WIP Entry

1. Copy `wip/TEMPLATE.md`
2. Rename to `YYYY-MM-DD__<project-slug>__<presenter>.md`
3. Remove `published: False` from frontmatter
4. Fill in the frontmatter and content sections
5. The entry will automatically appear on the WIP Log, Project, and People pages

See [wip/README.md](wip/README.md) for detailed instructions.

## Naming Conventions

| Type | Format | Example |
|------|--------|---------|
| Project slugs | lowercase with hyphens | `sonar-cv`, `acoustic-modem-energy-management` |
| Project files | `<project-slug>.md` | `sonar-cv.md` |
| People files | `firstname__lastname.md` | `juan__perez-ochoa.md` |
| WIP files | `YYYY-MM-DD__<project-slug>__<presenter>.md` | `2026-01-29__acoustic-modem-energy-management__mikasa-ackermann.md` |

## Status Values

Projects and WIP entries use consistent status values:

- `exploring` - Initial research and feasibility study
- `implementing` - Active development
- `experiments` - Running experiments and collecting data
- `writing` - Writing papers or documentation
- `wrapping-up` - Finalizing results
- `maintenance` - Ongoing maintenance
- `concluded` - Project completed

## Technical Details

This site uses:
- [Jekyll] static site generator
- [Just the Docs] theme
- [GitHub Pages] for hosting
- GitHub Actions workflow for automatic deployment

### Building and Previewing Locally

1. Install [Jekyll] and [Bundler]
2. Run `bundle install`
3. Run `bundle exec jekyll serve`
4. Preview at `localhost:4000`

The built site is stored in the `_site/` directory.

### Publishing on GitHub Pages

The site automatically builds and deploys via GitHub Actions when changes are pushed to the main branch.

To set up:
1. Go to Settings > Pages > Build and deployment
2. Select Source: GitHub Actions
3. Push changes to trigger deployment

---

[Jekyll]: https://jekyllrb.com
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[Bundler]: https://bundler.io
