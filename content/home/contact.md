---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 90

title: 📧 Contact
subtitle: '**I love learning and teaching new things. If you have questions about my work or see an opportunity to collaborate, please reach out.**'

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
#  email: test@example.org
#  phone: 888 888 88 88
#  address:
#    street: 450 Serra Mall
#    city: Stanford
#    region: CA
#    postcode: '94305'
#    country: United States
#    country_code: US
  coordinates:
    latitude: '34.1851'
    longitude: '-118.6090'
#  directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
#  office_hours:
#    - 'Monday 10:00 to 13:00'
#    - 'Wednesday 09:00 to 10:00'
  appointment_url: 'https://calendly.com/cloud-native-wiki/30min'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: DM Me
      link: 'https://twitter.com/avijit_tweeter'

design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '2'
  background:
    # Background color.
    #color: '#9fa8da'
    # Background gradient.
    #gradient_start: "DeepSkyBlue"
    #gradient_end: "SkyBlue"
    # Name of image in `assets/media/`.
    image: contact.jpeg
    # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
    image_darken: 0.6
    #  Options are `cover` (default), `contain`, or `actual` size.
    image_size: cover
    # Options include `left`, `center` (default), or `right`.
    image_position: center
    # Use a fun parallax-like fixed background effect on desktop? true/false
    image_parallax: true
    # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: true
---
