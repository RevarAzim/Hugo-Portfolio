---
title: Signalize
description: A mobile app that maps real-world cellular signal strength across Iraq and the Kurdistan Region.
dek: Crowdsourced cellular signal mapping
status: Under development
draft: true
weight: 1
tags:
  - Flutter
  - Dart
  - Kotlin
  - MapLibre
  - Geolocator
  - Laravel
  - PostgreSQL
  - H3
---

A mobile app that maps real-world cellular signal strength (dBm) across Iraq and the Kurdistan Region for local carriers (Asiacell, Korek, Zain, and Fastlink). Users can filter by carrier to check real coverage in any neighborhood before choosing a SIM or visiting an area, and can opt in to anonymously contribute live signal readings.

## Interactive hexagonal map

Full-screen MapLibre map with dynamic light/dark themes that renders coverage as color-coded H3 hexagons (resolution 10, ~140 m city-block cells).

## Verified and cold-start coverage

Bootstrapped with OpenCelliD baseline data, labeled as unverified estimates, and replaced with higher-opacity verified hexagons as real user measurements come in.

## Privacy-first opt-in telemetry

Users control data sharing through a first-launch prompt and a clean iOS-style Settings screen. Readings are only collected in the foreground when enabled, and they must pass a 20 m GPS accuracy filter.

## Stack

**Mobile:** Flutter (Dart), native Android Kotlin (MethodChannel + TelephonyManager for reading SIM MCC/MNC and cellular dBm), geolocator, and maplibre_gl.

**Backend and spatial:** Laravel 13, PostgreSQL, Uber H3 spatial indexing (h3-php), and standard GeoJSON API endpoints.
