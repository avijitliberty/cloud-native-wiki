---
widget: slider
weight: 1
active: true
headless: true

design:
  # Slide height is automatic unless you force a specific height (e.g. '400px')
  slide_height: ''
  is_fullscreen: true
  # Automatically transition through slides?
  loop: false
  # Duration of transition between slides (in ms)
  interval: 2000

content:
  slides:
    - title: 👋 Welcome to cloud-native.wiki
      content: Take a look at what we're working on...
      align: center
      background:
        position: center
        color: '#666'
        brightness: 0.7
        media: wiki-temp.jpeg
    - title: CheatSheets 📚
      content: 'These Cheatsheets are for the little things you never remember :bell:'
      align: left
      background:
        position: center
        color: '#555'
        brightness: 0.7
        media: background-honeycomb.png
      link:
        icon: compass
        icon_pack: fas
        text: Explore
        url: "#skills"
    - title: Latest Project 📐
      content: 'Let&shy;s build in the :cloud:'
      align: left
      background:
        position: center
        color: '#333'
        brightness: 0.5
        media: project.jpg
      link:
        icon: compass
        icon_pack: fas
        text: Explore
        url: "#projects"
    - title: Latest HowTo&shy;s 🤝
      content: 'Follow along and have :smiley:'
      align: left
      background:
        position: center
        color: '#333'
        brightness: 0.5
        media: tutorials-header.jpg
      link:
        icon: compass
        icon_pack: fas
        text: Explore
        url: "#posts"    
    - title: Collaborate and Contribute ✨
      content: ''
      align: left
      background:
        position: center
        color: '#333'
        brightness: 0.5
        media: collaborate.jpg
      link:
        icon: graduation-cap
        icon_pack: fas
        text: Join Us
        url: "#contact"    
---
