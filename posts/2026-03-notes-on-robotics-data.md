---
title: Notes on robotics data pipelines
date: 2026-03-14
---

A short note on what I've been thinking about lately. The gap between the data a robot *collects* and the data that is actually *useful* for learning is larger than most people assume.

## The collection problem

Most teleoperation setups log everything — joint states, camera frames, force readings, timestamps. The raw throughput looks impressive. But the signal-to-noise ratio depends entirely on whether the operator knew what they were demonstrating.

A few things I've found helpful:

- Segment demonstrations by *intent*, not by time window.
- Keep a separate channel for operator self-assessment ("this one was clean / messy / failed").
- Resample at the decision rate, not the sensor rate.

## What carries over from semiconductor work

Industrial data analytics taught me that the model is almost never the bottleneck. The bottleneck is the schema — whether two engineers can look at the same row and agree on what it means.

More on this another week.
