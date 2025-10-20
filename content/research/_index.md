---
title: "Research"
type: "page"            # plain page that renders blocks
# If your site needs it, some starters use: type: "widget_page"
blocks:
  - block: markdown
    content:
      title: "📚 My Research"
      text: |-
        Short blurb about your work.

        Add a line or two about methods, interests, and collaboration.

    design:
      columns: "1"

  - block: collection
    id: papers
    content:
      title: "Featured Publications"
      filters:
        # Point to the folder that holds items
        folders: ["publication"]      # <-- use ["publications"] only if you keep the plural folder (see note below)
        featured_only: true           # items need `featured: true` in their front matter
    design:
      view: article-grid              # grid of cards
      columns: 2

  - block: collection
    content:
      title: "Recent Publications"
      filters:
        folders: ["publication"]
        exclude_featured: false
      sort_by: date
      order: desc
    design:
      view: citation                  # compact citation list

  - block: collection
    id: talks
    content:
      title: "Recent & Upcoming Talks"
      filters:
        folders: ["event"]            # the default folder is **event** (singular)
      sort_by: date
      order: desc
    design:
      view: card
---
