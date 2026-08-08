---
title: Projects
cms_exclude: true
type: landing

# This page is not in the navigation - projects are shown on the homepage -
# but it exists so that direct links render with the same presentation.
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
      columns: 2
      fill_image: false
      show_date: false
      show_read_time: false
      show_read_more: false
---
