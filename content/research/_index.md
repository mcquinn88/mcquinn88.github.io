---
title: "Research"
type: landing
layout: landing

sections:
  # INLINE CSS ONLY — no external files needed
  - block: markdown
    content:
      title: ""
      text: |
        <style>
          /* ===== FORCE left label / right citations (works with any Blox wrapper) ===== */

          /* turn every collection block into a two-column grid */
          section.block-collection{
            display:grid !important;
            grid-template-columns: 300px 1fr !important;  /* LEFT label | RIGHT list */
            column-gap: 2rem !important;
            align-items:start !important;
            padding: 1.1rem 0 !important;
          }

          /* most themes wrap in a .container — make sure the grid applies there too */
          section.block-collection > *{
            grid-column: 1 / -1; /* default span both to avoid hidden content */
          }

          /* put the section header on the LEFT */
          section.block-collection header,
          section.block-collection > .container > header,
          section.block-collection > header{
            grid-column: 1 !important;
            text-align: left !important;
            margin: 0 !important;
            padding: .25rem 1rem .25rem 0 !important;
            border-right: 2px solid rgba(255,255,255,0.12) !important;
          }
          /* proof the CSS is active: temporarily tint the headings */
          section.block-collection header h2{ color:#c1ff72 !important; }

          /* put the list of items on the RIGHT (match any view container) */
          section.block-collection .view-citation,
          section.block-collection [class*="view-"],
          section.block-collection .items,
          section.block-collection .articles,
          section.block-collection .article-list{
            grid-column: 2 !important;
          }

          /* alternating background rows per block */
          section.block-collection:nth-of-type(odd){ background: rgba(255,255,255,.035) !important; }
          section.block-collection:nth-of-type(even){ background: transparent !important; }

          /* tighten citation spacing; kill any figures */
          section.block-collection .article{ margin:.28rem 0 !important; padding:0 !important; line-height:1.35 !important; font-size:1rem !important; }
          section.block-collection .card-figure,
          section.block-collection .article-header .featured-image,
          section.block-collection .figure,
          section.block-collection .responsive-figure{ display:none !important; }
        </style>
    design:
      columns: 1

  # Keep this first block for sanity: ensures items render
  - block: collection
    content:
      title: "All Publications (debug)"
      filters:
        section: "publications"
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  - block: collection
    content:
      title: "Working Papers"
      filters:
        section: "publications"
        publication_types: ["3"]
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  - block: collection
    content:
      title: "Work in Progress"
      filters:
        section: "publications"
        tags: ["in progress"]
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        section: "publications"
        publication_types: ["2"]
      sort_by: date_desc
      page_size: 100
    design:
      view: citation
---
