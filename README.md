# Documentation Drift Detection System

> Catching outdated knowledge before it reaches your agents — automatically.

---

## Overview

This project is a documentation health monitoring system built for a multi-client support operation. It continuously audits internal knowledge articles against real-time signals from support and engineering channels, identifies content that has drifted out of date, and generates severity-scored reports that flag issues before they affect agent responses or customer outcomes.

---

## The Problem

In a fast-moving support environment, internal knowledge bases go stale quickly. Product changes, policy updates, and process shifts happen regularly — but knowledge articles don't always keep pace. The result:

- Agents confidently follow outdated procedures
- Customers receive incorrect or inconsistent information
- Supervisors only discover documentation gaps after something goes wrong
- Knowledge audits happen manually, infrequently, and reactively

In a multi-client operation managing several different accounts simultaneously, this problem compounds quickly. What's accurate for one account may be outdated for another, and there's no reliable way to know without actively checking.

---

## The Solution

An automated drift detection system that:

- **Audits knowledge articles** against real-time signals from support tickets, engineering update channels, and team communications
- **Identifies drift** — where live operational signals contradict or no longer match what's documented
- **Scores severity** — each flagged article is assigned a severity level based on how critical the content is and how significant the gap appears to be
- **Generates structured reports** — outputs are formatted as severity-scored HTML reports that give operations leads a clear, prioritised view of what needs attention
- **Integrates with the agent workflow** — flagged articles are surfaced as warnings inside the LLM-Powered Agent Workflow Assistant, so agents are alerted before they rely on potentially outdated content
- **Runs on a batch processing model** — audits can be triggered on a schedule or on demand, covering multiple knowledge bases across different client accounts

---

## Impact

- Shifts documentation quality management from **reactive to proactive**
- Ensures agents are warned about stale content **before** it reaches a customer interaction
- Provides operations leadership with a **prioritised audit queue** rather than a flat list of all articles
- Reduces the risk of systemic misinformation across a multi-client support portfolio

---

## Key Design Principles

**Signal-driven, not schedule-driven** — Rather than flagging articles based purely on age, the system looks at whether the content still aligns with what's actually happening in the operation. An article written last week can drift; an article written two years ago can still be accurate.

**Severity-first output** — Reports are designed for triage, not reading. Operations leads can immediately see what's critical, what's moderate, and what's low priority without manually reviewing every flagged item.

**Cross-account awareness** — In a multi-client environment, documentation standards and accuracy requirements differ by account. The system is built to handle this without conflating issues across different client contexts.

**Bidirectional integration** — The system feeds into the agent workflow layer, so detection and agent-facing warnings are connected rather than siloed.

---

## Context

- **Environment:** Global BPO, multi-client support operation
- **Accounts covered:** Multiple client accounts with separate knowledge bases
- **Built by:** Support Operations (no engineering team involvement)
- **Output format:** Severity-scored HTML reports with prioritised flagging
- **Integration:** Connected to LLM-Powered Agent Workflow Assistant for real-time agent warnings

---

## Status

Live and in active use across multiple client accounts.

---

*This write-up is intentionally non-technical and omits client-specific details. It is intended to demonstrate operational problem-solving and systems thinking in a support environment.*
