# Jaemoon Lee's homepage

Source for [jmoon-lee.github.io](https://jmoon-lee.github.io), built with Jekyll and hosted on GitHub Pages.

## Updating the site

Updates can be requested in the Codex chat for this project. The files used most often are:

| Content | Location |
| --- | --- |
| Biography and academic background | `_pages/about.md` |
| Publications | `_publications/` |
| Publication list formatting | `_pages/publications.html` |
| CV download page | `_pages/cv.md` |
| CV document | `files/CV.pdf` |
| Profile photo | `images/profile.jpg` |
| Site title, contact details, and theme | `_config.yml` |
| Navigation links | `_data/navigation.yml` |

Keep the CV filename and download link in sync when replacing the PDF.

## Site structure

- `_pages/` contains the homepage, publications index, CV page, sitemap, and 404 page.
- `_publications/` contains one Markdown entry per publication.
- `_includes/`, `_layouts/`, `_sass/`, and `assets/` provide the shared theme and its dependencies.
- `images/` contains the profile photo and site icons.
- `files/` contains downloadable documents.

The shared theme files include fonts, navigation behavior, and light/dark styles. They are needed to maintain the site's appearance and should be changed with a site preview or build check.

## Preview and deployment

With Ruby and Bundler installed, run `bundle install` followed by `bundle exec jekyll serve` to preview the site at `http://localhost:4000`. `bundle exec jekyll build` checks that the site can be generated. `Gemfile` defines the build dependencies. The optional Docker, notebook, and content-generator tools from the original template have been removed.

For JavaScript changes, `npm install` and `npm run build:js` regenerate `assets/js/main.min.js` from its source files. Normal content edits do not require this step.

GitHub Pages manages the published site. Review changes before merging them into `master` and check the Pages deployment result afterward. Deleted template examples remain recoverable through Git history.

## Attribution

Based on [Academic Pages](https://github.com/academicpages/academicpages.github.io), which derives from Michael Rose's [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme. Original license notices are retained in `LICENSE`.
