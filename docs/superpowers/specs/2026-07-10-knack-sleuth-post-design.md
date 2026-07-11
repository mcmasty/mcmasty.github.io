# KnackSleuth post + homepage refresh — design

Date: 2026-07-10

## Goal

Introduce the knack-sleuth tool (github.com/mcmasty/knack-sleuth, on PyPI) on tlm13.com.

## Changes

1. **New post** `_posts/2026-07-10-Meet-KnackSleuth.md` — ~700-word tool intro:
   problem (tracing where objects/fields are used in a Knack app), what the tool
   does, install (uvx / uv / pip), CLI examples (`list-objects` with coupling
   metrics, `search-object`), short library-usage snippet (Pydantic
   `KnackAppMetadata`), links to GitHub + PyPI.
   Front matter follows existing conventions: `categories: [Post]`,
   `tags: [Python, Knack, CLI, Data]` → listed under Python at `/tags/#python`.
   URL: `/2026/post/Meet-KnackSleuth/`.
2. **Homepage** `_pages/home.md` — replace the retired Coronavirus `feature_row4`
   with a KnackSleuth row linking to the post. The covid-splash page remains
   reachable at its permalink, just not featured.
3. **Projects grid** `_projects/knack-sleuth.md` — short entry (hero + teaser +
   excerpt) linking to the post and repo; `categories: [Project]`,
   `tags: [Python, Knack, CLI]`.
4. **Images** — `juan-rumimpunu-nLXOatvTaLo-unsplash.jpg` (pondering monkey),
   uploaded to ImageKit `/tlm13/`; hero `tr:w-1280,h-380,fo-top`, teaser/card
   `tr:w-600,h-400`. Original archived in `imagekit_staging/`.

## Out of scope

Re-enabling the commented-out Tags/Categories nav links; any covid page cleanup.

## Approved

Approach, image choice (monkey), and COVID-row replacement approved by Tyler in
conversation on 2026-07-10.
