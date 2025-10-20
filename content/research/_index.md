---
title: "Research"
type: landing
layout: landing

sections:
  - block: markdown
    content:
      title: ""
    # 🔴 Keep the 8-space indent under `text: |` or the CSS won't render.
      text: |
        <style>
        /* ===== FINAL RESEARCH LAYOUT: Left label / Right citation list ===== */

        section.blox-collection{
          display:grid!important;
          grid-template-columns:300px 1fr!important; /* Left title | Right list */
          column-gap:2.25rem!important;
          align-items:start!important;
          padding:1.25rem 0!important;
        }

        /* Background layer spans both columns */
        section.blox-collection>.home-section-bg{grid-column:1/-1!important}

        /* LEFT column = the title wrapper (first .flex after bg) */
        section.blox-collection>div.flex:nth-of-type(2){
          grid-column:1!important;
          justify-self:start!important;
          text-align:left!important;
          padding-right:1rem!important;
          border-right:2px solid rgba(255,255,255,.1)!important;
        }
        section.blox-collection>div.flex:nth-of-type(2) .mb-6{
          margin:0!important;
          font-weight:800!important;
          font-size:2.1rem!important;
          line-height:1.15!important;
        }

        /* RIGHT column = the list wrapper (second .flex) */
        section.blox-collection>div.flex:nth-of-type(3){
          grid-column:2!important;
          justify-self:stretch!important;
          text-align:left!important;
          width:100%!important;
        }
        /* kill the theme’s narrow/centered container inside the list */
        section.blox-collection>div.flex:nth-of-type(3) .container{
          max-width:none!important;
          width:100%!important;
          margin:0!important;
          padding:0!important;
        }

        /* Compact citation spacing & hide figures */
        section.blox-collection .pub-list-item.view-citation{
          margin:.28rem 0!important;
          padding:0!important;
          line-height:1.35!important;
          font-size:1rem!important;
        }
        section.blox-collection .card-figure,
        section.blox-collection .article-header .featured-image,
        section.blox-collection .figure,
        section.blox-collection .responsive-figure{display:none!important}

        /* Alternating background */
        section.blox-collection:nth-of-type(odd){background:rgba(255,255,255,.03)!important}
        section.blox-collection:nth-of-type(even){background:transparent!important}
        </style>
    design:
      columns: 1

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


