---
title: Smart Backpacker API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='http://smartbackpackerapp.com/'>Download the App now!</a>

includes:
  - visa_requirements
  - baggage_policy
  - ranking
  - errors

search: true
---

# Introduction

Welcome to the Smart Backpacker API! 

Easily find Visa Requirements, Currency Exchange, Airline's Baggage Policy and your Passport Ranking among others.

# Authentication

All the endpoints require a Bearer JWT Authorization token in the headers, so make sure you execute a request with the following header:

```bash
curl "https://api-endpoint-here/" -H "Authorization: Bearer <your_access_token>"
```

<aside class="notice">
You must replace <code>&lt;your_access_token&gt;</code> with your API key.
</aside>

