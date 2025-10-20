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
        /* ===== Classic Research layout: left labels, right citations, shaded rows ===== */

        section.block-collection > .container{
          display:grid;
          grid-template-columns: 320px 1fr; /* LEFT label, RIGHT list */
          column-gap: 2.25rem;
          align-items:start;
          padding:1.1rem 0;
        }

        /* alternating background */
        section.block-collection:nth-of-type(odd){
          background:rgba(255,255,255,.035);
        }
        section.block-collection:nth-of-type(even){
          background:transparent;
        }

        /* LEFT column: section title */
        section.block-collection > .container > header{
          grid-column:1;
          text-align:left !important;
          margin:0;
          padding:.25rem 0;
          border-right:2px solid rgba(255,255,255,0.10);
          padding-right:1rem;
        }
        section.block-collection > .container > header h2{
          font-weight:800;
          font-size:2.05rem;
          line-height:1.15;
          letter-spacing:.1px;
          margin:0;
        }

        /* RIGHT column: citation list */
        section.block-collection > .container > .view-citation{
          grid-column:2;
        }

        /* tighten citations */
        .view-citation .article{
          margin:.28rem 0;
          padding:0;
          line-height:1.35;
          font-size:1rem;
        }

        /* badge tweaks (keep but make small) */
        .view-citation .btn-links,
        .view-citation .pub-links{
          margin-top:.15rem;
          gap:.35rem;
        }
        .btn,
        .badge,
        .btn-outline-primary{
          padding:.08rem .35rem;
          font-size:.72rem;
          line-height:1.1;
          border-radius:.3rem;
        }

        /* hide any images/cards */
        .card-figure,
        .article-header .featured-image,
        .figure,
        .responsive-figure{display:none!important;}
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
