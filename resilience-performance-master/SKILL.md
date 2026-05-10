---
name: resilience-performance-master
description: "Ensure the app works on high-latency (Noronha) or limited-resource (Hostinger) environments."
---

# Resilience & Performance Master

## 🎯 Goal
Guarantee usability under stress, latency, or hardware limits.

## 🛠️ Mandatory Checks
- **Latency (Noronha):** Does it have Skeletons? Optimistic updates? Are we avoiding large waterfalls of API calls?
- **Resources (Hostinger):** Is the PHP code doing too many disk writes? Are assets (images/CSS) optimized?
- **Next.js (AWS):** Are we over-using 'use client'? Can we use Server Components to reduce bundle size?

## 🚫 Anti-patterns
- Blocking the whole UI while waiting for a response (Bad for Noronha).
- Unfiltered database queries that grow over time (Bad for Hostinger).
- Hard-coding URLs or configs that change per environment.

## 📋 Output Format
1. **Performance Risks identified.**
2. **Resilience Improvements** (e.g., adding SWR cache).
3. **Expected Impact.**
4. **Plain-language summary.**