---
# An instance of the Featurette widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: featurette

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 10

title: 📚 CheatSheets
subtitle:

design:
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns: "1"
  background:
    # color: '#9fa8da'
    # Name of image in `assets/media/`.
    image: open-book.jpg
    # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
    image_darken: 1
    #  Options are `cover` (default), `contain`, or `actual` size.
    image_size: cover
    # Options include `left`, `center` (default), or `right`.
    image_position: center
    # Use a fun parallax-like fixed background effect on desktop? true/false
    image_parallax: true
    # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: false
advanced:
  css_class: fullscreen

# Showcase personal skills or business features.
# - Add/remove as many `feature` blocks below as you like.
# - For available icons, see: https://wowchemy.com/docs/page-builder/#icons
feature:
- description:
  icon: fab fa-github
  icon_pack: fab
  name: GitHub
  url: /cheatsheets/github/
- description:
  icon: fab fa-jenkins
  icon_pack: fab
  name: Jenkins
  url: /cheatsheets/jenkins
- description:
  icon: "jfrog"
  icon_pack: "custom"
  name: "JFrog"
  url: /post/artifactory
- description:
  icon: "spring"
  icon_pack: "custom"
  name: "SpringBoot"
  url: /cheatsheets/springboot
- description:
  icon: fab fa-docker
  icon_pack: fab
  name: Docker
  url: /cheatsheets/docker
- description:
  icon: "kubernetes"
  icon_pack: "custom"
  name: "Kubernetes"
  url: /cheatsheets/kubernetes
- description:
  icon: "vagrant"
  icon_pack: "custom"
  name: "Vagrant"
  url: /cheatsheets/vagrant
- description:
  icon: "splunk"
  icon_pack: "custom"
  name: "Splunk"
  url: /cheatsheets/splunk
- description:
  icon: fab fa-aws
  icon_pack: fab
  name: AWS
  url: /cheatsheets/aws
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
