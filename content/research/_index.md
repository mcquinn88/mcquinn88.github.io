---
title: "Research"
type: landing
layout: landing

sections:
  # ===== Working Papers (publication_types: ["3"]) =====
  - block: collection
    content:
      title: "Working Papers"
      filters:
        folders:
          - publications        # EXACT match to your example
        publication_type: ["3"] # Wowchemy type code for working papers
        exclude_featured: false
    design:
      view: citation

  # ===== Work in Progress (publication_types: ["4"]) =====
  - block: collection
    content:
      title: "Work in Progress"
      filters:
        folders:
          - publications
        publication_type: ["4"]
        exclude_featured: false
    design:
      view: citation

  # ===== Refereed Journal Publications (publication_types: ["2"]) =====
  - block: collection
    content:
      title: "Journal Publications"
      filters:
        folders:
          - publications
        publication_type: ["2"]
        exclude_featured: false
    design:
      view: citation
---
