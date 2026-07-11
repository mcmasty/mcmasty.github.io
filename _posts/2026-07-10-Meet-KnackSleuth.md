---
title: "KnackSleuth: Detective Work for Your Knack App"
date: 2026-07-10 21:00:00 Z
excerpt: A Python CLI and library that finds where objects, fields, and connections are used throughout your Knack application.
header:
  overlay_image: "https://ik.imagekit.io/oi1opj8xo/tr:w-1280,h-380,fo-top/tlm13/juan-rumimpunu-nLXOatvTaLo-unsplash.jpg"
  overlay_filter: 0.4
  caption: "Photo by Juan Rumimpunu on Unsplash"
  teaser: https://ik.imagekit.io/oi1opj8xo/tr:w-600,h-400/tlm13/juan-rumimpunu-nLXOatvTaLo-unsplash.jpg
categories:
- Post
tags:
- Python
- Knack
- CLI
- Data
---

If you've maintained a [Knack](https://www.knack.com/) app for any length of time, you know the moment: you're staring at a field named something like `Status (OLD - do not use?)` and wondering... can I actually delete this? Is it feeding a formula somewhere? A filter? A page rule buried three scenes deep?

The Knack builder is great for building, but answering "where is this used?" means clicking through every scene and view, one at a time, taking notes like a detective canvassing a neighborhood. I got tired of doing that by hand, so I built a tool to do the canvassing for me.

**[KnackSleuth](https://github.com/mcmasty/knack-sleuth)** investigates your Knack app's metadata and reports where objects, fields, and connections are used throughout your application — data relationships, view dependencies, and the references hiding in formulas and filters.

## Quick start

No install required if you have [uv](https://docs.astral.sh/uv/):

```bash
uvx knack-sleuth --help
```

Or install it properly:

```bash
pip install knack-sleuth
# or
uv tool install knack-sleuth
```

Point it at your app with `KNACK_APP_ID` set (or pass a metadata JSON export), and start asking questions.

## Where is this object used?

```bash
knack-sleuth search-object "Work Orders"
```

This reports every place the object shows up: connections from other objects, the views that display it, and field-level usages — columns, sorts, formulas, filters. It even prints direct links to the specific builder pages you'd want to review, so the "go check it" step is one click instead of a scavenger hunt.

## A map of your whole app

```bash
knack-sleuth list-objects --sort-by-rows
```

Beyond row and field counts, this borrows a couple of ideas from software engineering — afferent/efferent coupling and an instability score for each object:

- **High Ca, low Ce** — hub objects that everything else depends on. Change these carefully.
- **Low Ca, high Ce** — objects with lots of outbound dependencies; potentially fragile.
- **High both** — central *and* complex. Prime refactoring candidates.

It turns "I think this table is important?" into something you can actually see.

## It's a library, too

The foundation of KnackSleuth is a [Pydantic](https://docs.pydantic.dev/) model of the entire Knack application metadata, so you can build your own analysis on top of it:

```python
import json
from pathlib import Path

from knack_sleuth import KnackAppMetadata, KnackSleuth

data = json.loads(Path("my_app_metadata.json").read_text())
app_export = KnackAppMetadata(**data)

sleuth = KnackSleuth(app_export)
usages = sleuth.get_object_info("object_12")
```

Everything is typed and validated, which makes exploring the metadata in a notebook a pleasant experience instead of a `dict["nested"]["key"]["guessing"]` game.

## The details

- Metadata fetched from the Knack API is cached locally for 24 hours, so repeated queries don't hammer the API (use `--refresh` to force a fresh pull).
- Works from a local JSON export if you'd rather not touch the API at all.
- Source on [GitHub](https://github.com/mcmasty/knack-sleuth), package on [PyPI](https://pypi.org/project/knack-sleuth/).

If you try it on your own app, I'd love to hear what it finds — especially if it catches a dependency you'd forgotten about. That's the whole point: fewer surprises, faster detective work. 🕵️
