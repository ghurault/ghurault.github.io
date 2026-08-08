---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

# Page sections. Each `block` maps to a Hugo Blox in the `blox` module.
# Documentation: https://docs.hugoblox.com/
sections:
  - block: resume-biography-3
    content:
      # A profile in `data/authors/`
      username: admin
      text: ''
      button:
        text: CV
        url: uploads/cv.pdf
    design:
      # Plain background, closer to the previous site than the default mesh.
      background:
        gradient_mesh:
          enable: false
      avatar:
        size: medium
        shape: circle

  - block: collection
    id: projects
    content:
      title: Projects
      # 0 = show all. The block otherwise defaults to 5.
      count: 0
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 2
      fill_image: false
      show_date: false
      show_read_time: false
      show_read_more: false

  - block: collection
    id: publications
    content:
      title: Selected Publications
      text: |-
        > [!NOTE]
        > Browse the [full list of publications](/publications/).
      count: 5
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: citation
---
