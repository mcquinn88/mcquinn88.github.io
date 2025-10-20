---
title: "Research"
type: landing
layout: landing

sections:
  # INLINE CSS: left-hand labels + right-hand citation lists
  - block: markdown
    content:
      title: ""
      text: |
        <style>
        /* ===== FINAL TWO-COLUMN RESEARCH LAYOUT ===== */

        section.blox-collection {
          display: grid !important;
          grid-template-columns: 320px 1fr !important; /* Left title | Right list */
          column-gap: 2.5rem !important;
          align-items: start !important;
          padding: 1.75rem 3rem !important; /* Shift both columns right */
        }

        /* LEFT column (section titles) */
        section.blox-collection > div.flex:nth-of-type(2) {
          grid-column: 1 !important;
          justify-self: start !important;
          text-align: left !important;
          padding-right: 1.25rem !important;
          border-right: 2px solid rgba(255,255,255,0.1) !important;
        }
        section.blox-collection > div.flex:nth-of-type(2) .mb-6 {
          margin: 0 !important;
          font-weight: 800 !important;
          font-size: 2.1rem !important;
          line-height: 1.15 !important;
        }

        /* RIGHT column (citations) */
        section.blox-collection > div.flex:nth-of-type(3) {
          grid-column: 2 !important;
          justify-self: stretch !important;
          text-align: left !important;
          width: 100% !important;
        }
        section.blox-collection > div.flex:nth-of-type(3) .container {
          max-width: none !important;
          width: 100% !important;
          margin: 0 !important;
          padding: 0 !important;
        }

        /* Compact citations */
        section.blox-collection .pub-list-item.view-citation {
          margin: 0.28rem 0 !important;
          padding: 0 !important;
          line-height: 1.35 !important;
          font-size: 1rem !important;
        }

        /* Hide figures/cards */
        section.blox-collection .card-figure,
        section.blox-collection .article-header .featured-image,
        section.blox-collection .figure,
        section.blox-collection .responsive-figure {
          display: none !important;
        }

        /* Alternating background for readability */
        section.blox-collection:nth-of-type(odd) {
          background: rgba(255,255,255,0.03) !important;
        }
        section.blox-collection:nth-of-type(even) {
          background: transparent !important;
        }
        </style>

    design:
      columns: 1

  # Working Papers
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

  # Work in Progress
  - block: collection
    content:
      title: "Work in Progress"
      filters:
        section: "publications"
        publication_types: ["4"]
      sort_by: date_desc
      page_size: 100
    design:
      view: citation

  # Refereed Journal Publications
  - block: collection
    content:
      title: "Journal Publications"
      filters:
        section: "publications"
        publication_types: ["2"]
      sort_by: date_desc
      page_size: 100
    design:
      view: citation
---


