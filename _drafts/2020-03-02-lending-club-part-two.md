---
title: Lending Club Investing Performance, Part 2
date: 2020-03-03 19:34:30 Z
categories:
- Post
tags:
- Data
- Python
- Finance
last_modified_at: 2020-03-03 21:20:02 Z
project_id: lc_analysis_2020
---




## Strategies  

- **Haphazard**  Inconsistent, no methodology, no timing, at arbitrary times, jump on trading platform and buy arbitrary notes  

- **Looking for Yield**  Automated investing now available, create an automated portfolio with high risk & high yield  

- **Skew to Name Brands**   Tweak automated investing weight to shift portfolio to have a higher percentage of Grade A & B notes

- **Halfway Home**   No longer buy new issue, focus on secondary market for loans that are past the midway point of their term (18 months for 36 month notes and 30 months for 60 month notes)  


Note:  I didn't keep great notes, so I don't have a record of the looking for yield mix ... but the skew to name brands  A: 18%, B: 38%, C: 32%, D: 0%,


This mix has an Average Historical Return of 5.69% base on historical Note performance and volume by grade.



{% include figure image_path="/assets/images/lc/auto_blend_avg_hist_return.png" alt="Expected Historical Return" caption="Expected Historical Return." %}


# Testing this


Analysis of Expected Payments
(confirm what I see on the portal)


- [ ]  orig note amount missing from api
- [ ]  load from CSV download
- [ ]  some othe thing
