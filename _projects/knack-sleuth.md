---
title: KnackSleuth
date: 2026-07-10 21:00:00 Z
excerpt: A Python CLI and library that finds where objects, fields, and connections are used throughout a Knack application.
header:
  overlay_image: "https://ik.imagekit.io/oi1opj8xo/tr:w-1280,h-380,fo-top/tlm13/juan-rumimpunu-nLXOatvTaLo-unsplash.jpg"
  overlay_filter: 0.4
  caption: Photo by Juan Rumimpunu on Unsplash
  teaser: https://ik.imagekit.io/oi1opj8xo/tr:w-600,h-400/tlm13/juan-rumimpunu-nLXOatvTaLo-unsplash.jpg
categories:
- Project
tags:
- Python
- Knack
- CLI
last_modified_at: 2026-07-10 21:00:00 Z
---

**Detective work for your Knack applications.** 🕵️

KnackSleuth investigates your Knack app's metadata to uncover where objects, fields, and connections are used throughout your application — data relationships, view dependencies, and references hiding in formulas and filters. Useful before refactoring a complex app, auditing data dependencies, or deleting that field you're *pretty* sure nothing uses.

Built in Python on a fully-typed Pydantic model of the Knack application metadata, so it works as both a CLI and a library.

```bash
uvx knack-sleuth search-object "Work Orders"
```

- Read the introduction post: [KnackSleuth: Detective Work for Your Knack App](/2026/post/Meet-KnackSleuth/)
- Source on [GitHub](https://github.com/mcmasty/knack-sleuth)
- Install from [PyPI](https://pypi.org/project/knack-sleuth/)
