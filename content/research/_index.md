---
title: "Research"
type: landing
layout: landing
css_class: page-research   # <-- gives us a hook for CSS. Do not remove.

sections:
  - block: collection
    content:
      title: "Working Papers"
      filters:
        section: "publications"
        publication_types: ["3"]   # working paper / preprint
      sort_by: date_desc
    design:
      view: citation               # text-only citations

  - block: collection
    content:
      title: "Work in Progress"
      filters:
        section: "publications"
        tags: ["in progress"]      # tag your WIP with this
      sort_by: date_desc
    design:
      view: citation

  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        section: "publications"
        publication_types: ["2"]   # journal article
      sort_by: date_desc
    design:
      view: citation
---
