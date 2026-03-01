---
title: 'KVSwap: Disk-aware KV Cache Offloading for Long-Context On-device Inference'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Huawei Zhang
  - Chunwei Xia
  - Zheng Wang
# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2026-03-01T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2026-03-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *The 24th ACM International Conference on Mobile Systems, Applications, and Services* (Conditional Accepted) 
publication_short: In *ACM MobiSys '26*

abstract: Language models (LMs) underpin emerging mobile and embedded AI applications like meeting and video summarization and document analysis, which often require processing multiple long-context inputs. Running an LM locally on-device improves privacy, enables offline use, and reduces cost, but long-context inference quickly hits a memory capacity wall as the key-value (KV) cache grows linearly with context length and batch size. Existing KV-cache offloading schemes are designed to transfer cache data from GPU memory to CPU memory; however, they are not suitable for embedded and mobile systems, where the CPU and GPU (or NPU) typically share a unified memory and the non-volatile secondary storage (disk) offers limited I/O bandwidth. We present KVSwap, a software framework tailored for local devices that achieves high memory efficiency while effectively leveraging disk storage. KVSwap stores the full cache on disk, uses highly compact in-memory metadata to predict which entries to preload, overlaps computation with hardware-aware disk access, and orchestrates read patterns to match storage device characteristics. Our evaluation shows that across representative LMs and storage types, KVSwap delivers higher throughput under tight memory budgets while maintaining generation quality over existing KV cache offloading schemes.

# Summary. An optional shortened abstract.
summary: ''

tags:
  - Large Language Models
  - KV Cache Offloading
  - Sparse KV Cache
  - Mobile AI

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/pdf/2511.11907'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'KVSwap'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

<!-- {{% callout note %}}
Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the _Slides_ button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->
