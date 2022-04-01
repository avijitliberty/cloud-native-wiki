---
# An instance of the Featurette widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: featurette

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 10

title:
subtitle:

design:
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns: "1"
  background:
    # Name of image in `assets/media/`.
    image: background.jpg
    # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
    image_darken: 0.8
    #  Options are `cover` (default), `contain`, or `actual` size.
    image_size: cover
    # Options include `left`, `center` (default), or `right`.
    image_position: center
    # Use a fun parallax-like fixed background effect on desktop? true/false
    image_parallax: true
    # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: true
advanced:
  css_class: fullscreen

# Showcase personal skills or business features.
# - Add/remove as many `feature` blocks below as you like.
# - For available icons, see: https://wowchemy.com/docs/page-builder/#icons
feature:
- description:
  icon: devops
  icon_pack: custom
  name: DevOps
- description:
  icon:
  icon_pack:
  name:
- description:
  icon: fab fa-docker
  icon_pack: fab
  name: Containers
  url: /cheatsheets/docker
- description:
  icon: cicd
  icon_pack: custom
  name: CI/CD
- description:
  icon:
  icon_pack:
  name:
- description:
  icon: microservice
  icon_pack: custom
  name: Microservice
# Uncomment to use emoji icons.
#- icon: ":smile:"
#  icon_pack: "emoji"
#  name: "Emojiness"
#  description: "100%"  

# Uncomment to use custom SVG icons.
# Place your custom SVG icon in `assets/media/icons/`.
# Reference the SVG icon name (without `.svg` extension) in the `icon` field.
# For example, reference `assets/media/icons/xyz.svg` as `icon: 'xyz'`
#- icon: "your-custom-icon-name"
#  icon_pack: "custom"
#  name: "Surfing"
#  description: "90%"
---
