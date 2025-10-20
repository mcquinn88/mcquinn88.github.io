---
title: "Research"
type: landing
layout: landing
css_class: page-research

sections:
  # Inline CSS that only affects this page.
  - block: markdown
    content:
      title: ""
      text: |
        <style>
        /* ===== Classic two-column research layout for Hugo Blox ===== */

        /* make each collection section a 2-column grid */
        body.page-research section.block-collection > .container{
          display:grid;
          grid-template-columns: 320px 1fr;   /* LEFT label | RIGHT list */
          column-gap: 2.25rem;
          align-items:start;
          padding: 1.1rem 0;
        }

        /* alternating background by section */
        body.page-research section.block-collection:nth-of-type(odd){
          background: rgba(255,255,255,.035);
        }
        body.page-research section.block-collection:nth-of-type(even){
          background: transparent;
        }

        /* LEFT column: the section header */
        body.page-research section.block-collection > .container > header{
          grid-column:1;
          text-align:left !important;
          margin:0;
          padding:.25rem 0;
          border-right: 2px solid rgba(255,255,255,0.10);
          padding-right: 1rem;
        }
        body.page-research section.block-collection > .container > header h2{
          font-weight:800;
          font-size:2.05rem;
          line-height:1.15;
          letter-spacing:.1px;
          margin:0;
        }

        /* RIGHT column: the citation list */
        body.page-research section.block-collection > .container > .view-citation{
          grid-column:2;
        }

        /* tighten citations */
        body.page-research .view-citation .article{
          margin:.28rem 0;
          padding:0;
          line-height:1.35;
          font-size:1rem;
        }

        /* optional: keep badges compact (remove this block to hide them) */
        body.page-research .view-citation .btn-links,
        body.page-research .view-citation .pub-links{
          margin-top:.15rem;
          gap:.35rem;
        }
        body.page-research .btn,
        body.page-research .badge,
        body.page-research .btn-outline-primary{
          padding:.08rem .35rem;
          font-size:.72rem;
          line-height:1.1;
          border-radius:.3rem;
        }

        /* never show images/cards inside research lists */
        body.page-research .card-figure,
        body.page-research .article-header .featured-image,
        body.page-research .figure,
        body.page-research .responsive-figure{ display:none !important; }
        </style>
    design:
      columns: 1

  - block: collection
    content:
      title: "Working Papers"
      filters:
        section: "publications"
        publication_types: ["3"]   # working paper / preprint
      sort_by: date_desc
    design:
      view: citation

  - block: collection
    content:
      title: "Work in Progress"
      filters:
        section: "publications"
        tags: ["in progress"]      # tag your WIP items accordingly
      sort_by: date_desc
    design:
      view: citation

  - block: collection
    content:
      title: "Refereed Journal Publications"
      filters:
        section: "publicitions"    # <-- typo would break; keep "publications"
        publication_types: ["2"]   # journal articles
      sort_by: date_desc
    design:
      view: citation
---
