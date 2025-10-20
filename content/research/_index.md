---
title: "Research"
type: landing
layout: landing

sections:
  # ===== DEBUG 1: Should list EVERYTHING under content/publications/ =====
  - block: collection
    content:
      title: "DEBUG — All Publications (temporary)"
      filters:
        folders: ["publications"]     # matches your path content/publications/
    design:
      view: citation

  # ===== DEBUG 2: Items with NO category tag (wp/wip/journal) =====
  - block: collection
    content:
      title: "DEBUG — Uncategorized (missing wp/wip/journal tag)"
      filters:
        folders: ["publications"]
        exclude:
          tags: ["wp","wip","journal"]
    design:
      view: citation

  # ===== CSS layout for the pretty sections below =====
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
        section.blox-collection>.home-section-bg{ grid-column:1 / -1!important }
        section.blox-collection>div.flex:nth-of-type(2){
          grid-column:2!important; justify-self:start!important; text-align:left!important;
          padding-right:1rem!important; border-right:2px solid rgba(255,255,255,.1)!important;
        }
        section.blox-collection>div.flex:nth-of-type(2) .mb-6{
          margin:0!important; font-weight:800!important; font-size:2.1rem!important; line-height:1.15!important;
        }
        section.blox-collection>div.flex:nth-of-type(3){
          grid-column:3!important; justify-self:stretch!important; text-align:left!important; width:100%!important;
        }
        section.blox-collection>div.flex:nth-of-type(3) .container{
          max-width:none!important; width:100%!important; margin:0!important; padding:0!important;
        }
        section.blox-collection .pub-list-item.view-citation{
          margin:.28rem 0!important; padding:0!important; line-height:1.35!important; font-size:1rem!important;
        }
        section.blox-collection .card-figure,
        section.blox-collection .article-header .featured-image,
        section.blox-collection .figure,
        section.blox-collection .responsive-figure{display:none!important}
        section.blox-collection:nth-of-type(odd){background:rgba(255,255,255,.03)!important}
        section.blox-collection:nth-of-type(even){background:transparent!important}
        </style>
    design:
      columns: 1

  # ===== Working Papers (tag: wp) =====
  - block: collection
    content:
      title: "Working Papers"
      filters:
        folders: ["publications"]
        tags: ["wp"]
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation

  # ===== Work in Progress (tag: wip) =====
  - block: collection
    content:
      title: "Work in Progress"
      filters:
        folders: ["publications"]
        tags: ["wip"]
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation

  # ===== Journal Publications (tag: journal) =====
  - block: collection
    content:
      title: "Journal Publications"
      filters:
        folders: ["publications"]
        tags: ["journal"]
        exclude:
          folders: ["talk","event","post","project"]
      sort_by: "date"
    design:
      view: citation
---


