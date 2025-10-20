---
title: "Research"
type: landing
layout: landing

sections:
  - block: header
    content:
      title: "Research"
      subtitle: ""
    design:
      align: left

  # ===== Working Papers =====
  - block: collection
    content:
      title: "Working Papers"
      filters:
        folders: ["publications"]
        publication_types: ["3"]     # 3 = preprint/working paper in Wowchemy
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation                 # <<< citation style (no images)

  # ===== Work in Progress =====
  - block: collection
    content:
      title: "Work in Progress"
      filters:
        folders: ["publications"]
        tags: ["in progress"]        # tag your WIP items with:  tags: ["in progress"]
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  # ===== Refereed Journal Publications =====
  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        folders: ["publications"]
        publication_types: ["2"]     # 2 = journal article
        featured_only: false
      sort_by: date_desc
      page_size: 100
    design:
      view: citation
---
