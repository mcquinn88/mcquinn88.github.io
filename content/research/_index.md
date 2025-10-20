---
title: "Research"
type: landing            # ← this enables blocks on non-home pages
sections:
  - block: collection
    content:
      title: "Publications"
      subtitle: ""
      filters:
        folders: ["publications"]   # stays plural, matching your tree
        featured_only: false
      sort_by: date_desc
      page_size: 50
    design:
      view: card        # options: card | article-grid | citation
      columns: 2
---
