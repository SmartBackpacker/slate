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
  - health
  - errors

search: true
---

# Introduction

Welcome to the Smart Backpacker API! 

Easily find Visa Requirements, Currency Exchange, Airline's Baggage Policy and your Passport Ranking among others.

# Environments

### Production

[https://api.smartbackpackerapp.com/](https://api.smartbackpackerapp.com/)

### Development

[https://smart-backpacker.herokuapp.com/](https://smart-backpacker.herokuapp.com/)

<aside class="success">
Both environments work only over <b>TLS</b> / <b>SSL</b> (https). Make sure you have the right public certificate.
</aside>

# Authentication

All the endpoints require a Bearer JWT Authorization token in the headers, so make sure you have it when performing a request. It should follow the form:

`Authorization: Bearer <your_access_token>`

```bash
curl "https://api.smartbackpackerapp.com/v1/endpoint/" -H "Authorization: Bearer <your_access_token>"
```

<aside class="notice">
You must replace <code>&lt;your_access_token&gt;</code> with your API key.
</aside>

