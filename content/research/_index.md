---
title: "Research"
type: landing
layout: landing

sections:
  - block: markdown
    content:
      title: "Research"
      text: |
        <style>
          /* citation lists: no badges/links row, tighter spacing */
          .view-citation .article{margin:0.25rem 0;padding:0}
          .view-citation .btn-links,
          .view-citation .pub-links{display:none}

          /* kill any figures/thumbs just in case */
          .view-card .card-figure,
          .view-article-grid .card-figure,
          .article-header .featured-image,
          .figure,.responsive-figure{display:none}

          /* section headings: left, tighter */
          section.block > header h2{margin:.5rem 0 .25rem 0;text-align:left}
        </style>
    design:
      columns: 1

  - block: collection
    content:
      title: "Working Papers"
      filters:
        section: "publications"
        publication_types: ["3"]
      sort_by: date_desc
    design:
      view: citation

  - block: collection
    content:
      title: "Work in Progress"
      filters:
        section: "publications"
        tags: ["in progress"]
      sort_by: date_desc
    design:
      view: citation

  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        section: "publications"
        publication_types: ["2"]
      sort_by: date_desc
    design:
      view: citation
---
