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
          /* ===== Left label / Right list for Hugo Blox (blox-collection markup) ===== */

          /* Make each collection section a 2-column grid */
          section.blox-collection{
            display:grid!important;
            grid-template-columns:300px 1fr!important; /* LEFT label | RIGHT list */
            column-gap:2rem!important;
            align-items:start!important;
            padding:1.1rem 0!important;
          }

          /* Background layer spans both columns */
          section.blox-collection>.home-section-bg{grid-column:1/-1!important}

          /* LEFT column = the title wrapper (first .flex after bg) */
          section.blox-collection>div.flex:nth-of-type(2){
            grid-column:1!important;
            justify-self:start!important;
            text-align:left!important;
          }
          /* style the visible title text */
          section.blox-collection>div.flex:nth-of-type(2) .mb-6{
            margin:0!important;font-weight:800!important;line-height:1.15!important;
          }

          /* RIGHT column = the list wrapper (second .flex after bg/title) */
          section.blox-collection>div.flex:nth-of-type(3){
            grid-column:2!important;
            justify-self:stretch!important;
            text-align:left!important;
            width:100%!important;
          }
          /* break the theme’s centered, narrow container inside the list */
          section.blox-collection>div.flex:nth-of-type(3) .container{
            max-width:none!important;width:100%!important;margin:0!important;padding:0!important;
          }

          /* Compact citations & hide figures */
          section.blox-collection .pub-list-item.view-citation{
            margin:.28rem 0!important;padding:0!important;line-height:1.35!important;font-size:1rem!important;
          }
          section.blox-collection .card-figure,
          section.blox-collection .article-header .featured-image,
          section.blox-collection .figure,
          section.blox-collection .responsive-figure{display:none!important}

          /* Alternating background per section */
          section.blox-collection:nth-of-type(odd){background:rgba(255,255,255,.035)!important}
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

