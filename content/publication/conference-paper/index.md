---
title: 'Understanding the Performance Implications of the Design Principles in Storage-Disaggregated Databases'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Xi Pang
  - Jianguo Wang 

# Author notes (optional)
#author_notes:
#  - 'Equal contribution'
#  - 'Equal contribution'

date: '2024-02-23T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2024-02-23T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: The ACM Special Interest Group on Management of Data 
publication_short: In *SIGMOD 2024*

abstract: Storage-compute disaggregation has recently emerged as a novel architecture in modern data centers, particularly in the cloud. By decoupling compute from storage, this new architecture enables independent and elastic scaling of compute and storage resources, potentially increasing resource utilization and reducing overall costs. To best leverage the disaggregated architecture, a new breed of database systems termed storage-disaggregated databases has recently been developed, such as Amazon Aurora, Microsoft Socrates, Google AlloyDB, and Huawei Taurus. However, little is known about the effectiveness of the design principles in these databases since they are typically developed by industry giants, and only the overall performance results are presented without detailing the impact of individual design principles. As a result, many critical research questions remain unclear, such as the performance impact of storage-disaggregation, the log-as-the-database design, shared-storage, and various log-replay methods. In this paper, we investigate the performance implications of the design principles that are widely adopted in storage-disaggregated databases for the first time. As these databases were usually not open-sourced, we have made a significant effort to implement a storage-disaggregated database prototype based on PostgreSQL v13.0. By fully controlling and instrumenting the codebase, we are able to selectively enable and disable individual optimizations and techniques to evaluate their impact on performance in various scenarios. Furthermore, we open-source our storage-disaggregated database prototype for use by the broader database research community, fostering collaboration and innovation in this field.

# Summary. An optional shortened abstract.
#summary: 

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: 'https://github.com/px1900/OpenAurora'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
#projects:
#  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---

