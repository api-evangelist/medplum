---
title: Medplum Self-Hosted Performance Benchmarks
url: https://www.medplum.com/blog/medplum-performance-test-2026
date: '2026-03-30'
author: ''
feed_url: https://www.medplum.com/blog/rss.xml
---
One of the most common questions we hear from teams evaluating Medplum is: "Can it handle our scale?" We wanted to answer that question with real data. We recently ran a formal performance evaluation against a self-hosted Medplum deployment that mirrors one of our largest production clusters, and the results speak for themselves - peak throughput exceeding 46,000 requests per second for read-only traffic and nearly 7,000 requests per second for full read/write/search FHIR workflows, with zero HTTP failures across all scenarios.
