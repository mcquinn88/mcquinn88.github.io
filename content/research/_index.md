---
title: "Research"
type: landing
layout: landing

sections:
  # ===== Inline CSS layout (left title, right list, full-width row shading) =====
  - block: markdown
    content:
      title: ""
      text: |
        <style>
        section.blox-collection{
          display:grid!important;
          grid-template-columns:80px 320px 1fr!important; /* gutter | title | list */
          column-gap:2.25rem!important;
          align-items:start!important;
          padding:1.25rem 0!important;
        }
        /* keep alternating background spanning full width */
        section.blox-collection>.home-section-bg{ grid-column:1 / -1!important }

        /* left title column */
        section.blox-collection>div.flex:nth-of-type(2){
          grid-column:2!important;
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

        /* right list column */
        section.blox-collection>div.flex:nth-of-type(3){
          grid-column:3!important;
          justify-self:stretch!important;
          text-align:left!important;
          width:100%!important;
        }
        section.blox-collection>div.flex:nth-of-type(3) .container{
          max-width:none!important;
          width:100%!important;
          margin:0!important;
          padding:0!important;
        }

        /* compact citations; hide figures/thumbnails */
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

        /* alternating background per section row */
        section.blox-collection:nth-of-type(odd){background:rgba(255,255,255,.03)!important}
        section.blox-collection:nth-of-type(even){background:transparent!important}
        </style>
    design:
      columns: 1

  # ===== Working Papers (publication_types = "3") =====
  - block: collection
    content:
      title: "Working Papers"
      filters:
        folders: ["publications"]        # matches content/publications/
        publication_type: ["3"]          # filter key is singular
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation

  # ===== Work in Progress (publication_types = "4") =====
  - block: collection
    content:
      title: "Work in Progress"
      filters:
        folders: ["publications"]
        publication_type: ["4"]
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation

  # ===== Refereed Journal Publications (publication_types = "2") =====
  - block: collection
    content:
      title: "Journal Publications"
      filters:
        folders: ["publications"]
        publication_type: ["2"]
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation

  # -- DEBUG (optional): uncomment to list everything under publications
  # - block: collection
  #   content:
  #     title: "All publications (debug)"
  #     filters:
  #       folders: ["publications"]
  #   design:
  #     view: citation
---

