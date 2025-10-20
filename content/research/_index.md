---
title: "Research"
type: landing
layout: landing
css_class: page-research

sections:
  - block: markdown
    content:
      title: ""
      text: |
        <style>
        /* force left/right two-column block layout in Hugo Blox */

        section.block-collection > .container {
          display: grid;
          grid-template-columns: 280px 1fr;
          column-gap: 2rem;
          align-items: start;
          padding: 1.5rem 0;
        }

        section.block-collection:nth-of-type(odd) {
          background: rgba(255,255,255,.03);
        }
        section.block-collection:nth-of-type(even) {
          background: transparent;
        }

        section.block-collection > .container > header {
          grid-column: 1;
          text-align: left;
          margin: 0;
          padding: .25rem 0;
        }

        section.block-collection > .container > header h2 {
          font-weight: 800;
          font-size: 2rem;
          line-height: 1.1;
          margin: 0;
        }

        section.block-collection > .container > .view-citation {
          grid-column: 2;
        }

        .view-citation .article {
          margin: .3rem 0;
          padding: 0;
          line-height: 1.4;
          font-size: 1rem;
        }

        .card-figure,
        .figure,
        .responsive-figure,
        .article-header .featured-image {
          display: none !important;
        }
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

