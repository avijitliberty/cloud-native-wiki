---
# An instance of the Portfolio widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: 📐Projects
subtitle: ''

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
  - name: All
    tag: '*'
  - name: Spring Boot
    tag: Spring Boot
  - name: AWS
    tag: AWS
  - name: Kubernetes
    tag: Kubernetes
  - name: Other
    tag: Demo

design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '2'
  background:
    # Background color.
    # color: '#9fa8da'
    # Background gradient.
    #gradient_start: "DeepSkyBlue"
    #gradient_end: "SkyBlue"
    # Name of image in `assets/media/`.
    image: open-book.jpg
    # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
    image_darken: 1
    #  Options are `cover` (default), `contain`, or `actual` size.
    image_size: cover
    # Options include `left`, `center` (default), or `right`.
    image_position: right
    # Use a fun parallax-like fixed background effect on desktop? true/false
    image_parallax: true
    # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: false

  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   5 = Showcase
  view: Showcase

  # For Showcase view, flip alternate rows?
  flip_alt_rows: false

---
