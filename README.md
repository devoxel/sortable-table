## sortof-sortable

### Overview

Sortable is an open-source JavaScript and CSS library which adds sorting
functionality to tables. It is tiny (`<2kb` min+gzip) and has no dependencies.

### Usage

Two ways to use this fork:

1. Use the unpkg CDN. Simply include the two following tags in your HTML:

  ```html
  <script
    src="https://unpkg.com/sortof-sortable@1.0.0/js/sortable.min.js"
    integrity="sha384-K0taKuySEnwNDkZEDTO52NXRHPRXwe93nX6FGiODxw5npAbsDHdTloLRU0I8UoUE"
    crossorigin="anonymous" referrerpolicy="no-referrer"></script>
  ```

  The CDN provides access to the CSS too, for example:
  ```html
  <link
    rel="stylesheet"
    href="https://unpkg.com/sortof-sortable@1.0.0/css/sortable-theme-light.css"
    integrity="sha384-UPNLQvcJ/lO4hTRxASq3ZM+QKAVj7/sKoaxhlMfUzqLFRd9xJfzMrVhpm2o/AE8Q"
    crossorigin="anonymous" referrerpolicy="no-referrer" />
  ```

2. Grab the JS & CSS files from Github or the latest release.

### Fork Status

This is a fork of [HubSpot/sortable](https://github.com/HubSpot/sortable).
Due to a lack of maintenance, I felt it prudent to open a fork.

I will only look at PRs for critical / performance issues - I like the
simplicity of the original.

Changes include:

- Updates dev tooling to latest version (as of Oct 2024).
- Merged Hubspot/sortable#54 - "Fix performance issues with large tables". Thanks @hjacobs for writing this code.
- Addressed Hubspot/sortable#46 - "touch devices fires sorting twice". This if fixed to just use the touchstart event on mobile.
- Addressed a race with the DOM - I didn't file an issue for this one, but the script can run before DOM is ready, meaning the onclick events are not setup. I encoutered this when creating large tables and having the script in the `<head>`.

I will make this available on a CDN for easy access.
