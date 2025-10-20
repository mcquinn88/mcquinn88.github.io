---
title: "Research"
type: landing
layout: landing

sections:
  # INLINE CSS (no external files). If this does nothing visually, HTML is being stripped.
  - block: markdown
    content:
      title: ""
      text: |
        <style>
          /* VISUAL PROOF this CSS is active: make section titles red temporarily */
          section.block-collection > .container > header h2 { color:#c23616 !important; }

          /* Left/Right layout */
          section.block-collection > .container{
            display:grid;
            grid-template-columns: 300px 1fr; /* LEFT label | RIGHT list */
            column-gap:2rem;
            align-items:start;
            padding:1rem 0;
          }
          section.block-collection:nth-of-type(odd){ background:rgba(255,255,255,.035); }
          section.block-collection:nth-of-type(even){ background:transparent; }

          section.block-collection > .container > header{
            grid-column:1; text-align:left; margin:0; padding:.25rem 0;
            border-right:2px solid rgba(255,255,255,0.10); padding-right:1rem;
          }
          section.block-collection > .container > .view-citation{ grid-column:2; }

          /* Tight citations; kill any figures */
          .view-citation .article{ margin:.28rem 0; padding:0; line-height:1.35; font-size:1rem; }
          .card-figure, .article-header .featured-image, .figure, .responsive-figure{ display:none !important; }
        </style>
    design:
      columns: 1

  # DEBUG: single bucket first to verify items render
  - block: collection
    content:
      title: "All Publications (debug)"
      filters:
        section: "publications"   # <- your plural section
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  # After the debug block works, you can keep these grouped lists.
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
