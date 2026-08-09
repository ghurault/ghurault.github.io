---
title: Projects
cms_exclude: true
type: landing

sections:
  - block: collection
    content:
      title: Projects
      # 0 = show all. The block otherwise defaults to 5.
      count: 0
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 3
      fill_image: false
      show_date: false
      show_read_time: false
      show_read_more: false
---
