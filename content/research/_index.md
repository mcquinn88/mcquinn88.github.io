---
title: "Research"
type: landing
layout: landing

sections:
  - block: markdown
    content:
      title: "Research"
      text: ""
    design:
      columns: 1

  - block: collection
    content:
      title: "Working Papers"
      filters:
        folders: ["publications"]
        publication_types: ["3"]     # 3 = working paper/preprint
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation                  # ← compact citations, no images

  - block: collection
    content:
      title: "Work in Progress"
      filters:
        folders: ["publications"]
        tags: ["in progress"]         # tag your WIP items with: tags: ["in progress"]
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        folders: ["publications"]
        publication_types: ["2"]      # 2 = journal article
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation
---
