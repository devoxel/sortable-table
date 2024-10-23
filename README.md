## sortof-sortable

### Overview

Sortable is an open-source JavaScript and CSS library which adds sorting
functionality to tables. It is tiny (`<2kb` min+gzip) and has no dependencies.

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
