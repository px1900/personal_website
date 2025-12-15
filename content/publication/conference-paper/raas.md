---
title: 'Reducing Tail Latency in Storage-Disaggregated Database Systems'

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

date: '2025-11-24T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2025-11-24T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: The ACM Special Interest Group on Management of Data 
publication_short: In *SIGMOD 2026*

abstract: Storage-disaggregated databases have become the standard in the cloud due to many benefits, including improved resource utilization, reduced resource fragmentation, and the ability to independently and elastically scale compute and storage, ultimately leading to cost savings. This work focuses on OLTP databases. Examples include Amazon Aurora, Microsoft Socrates, and Neon. However, a significant limitation we have identified in storage-disaggregated databases is the long tail latency. This issue arises from the unique architecture of these databases, specifically the log-as-the-database design principle. Under this design, when a transaction is committed, only the logs are sent to the storage engine over the network to minimize data movement, while the actual pages are replayed on the storage side. Thus, certain page requests may encounter a lengthy log replay chain, which lead to long latency. In this paper, we introduce a novel technique called \textit{Replay-as-a-Service} (RaaS) to address the high tail latency issue in storage-disaggregated databases. The main idea behind RaaS is to decouple the log replay logic from the storage engine and make it as an independent service. This approach provides the flexibility to utilize idle servers or even dedicated servers within the cluster to efficiently execute the log replay. To enable this, we introduce a suite of techniques and optimizations to address key technical challenges. We have implemented the RaaS technique within OpenAurora, a popular open-source storage-disaggregated database based on PostgreSQL. Experiments on SysBench show that RaaS reduces P95 tail latency by 40.1\% and improves the overall throughput by 75.9\%. 

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
url_code: 'https://github.com/purduedb/OpenAurora'
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

