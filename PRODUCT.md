# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Two-stage hiring audience in Taiwan tech:

1. Recruiters / HR screening in ~30 seconds: role, years, current employer, headline strengths, contact.
2. Engineering managers who pass the screen and read deeply: project scope, architecture decisions, stack, measurable results.

The page must serve both without making either wade through the other's layer.

## Product Purpose

Personal résumé site for 趙奕錡 (YICHI Chao), software / full-stack engineer. Success = the reader emails him to set up an interview. GitHub is secondary.

## Positioning

Builds industrial AI and self-hosted infrastructure from zero inside air-gapped factories: on-prem edge inference, self-hosted CI/CD + MLOps, self-hosted GPU LLM platform. Data never leaves the site. That constraint-driven, end-to-end ownership is what a generic full-stack résumé cannot claim.

## Operating Context

Visitors arrive from a link in a 104 / LinkedIn résumé or an email. Read on desktop and phones. Hosted on GitHub Pages as a single static `index.html`.

## Capabilities and Constraints

- Static HTML/CSS/JS only, no build step; GitHub Pages.
- Bilingual zh-Hant / English with a toggle — required to keep.
- Dark mode, architecture diagrams, and the hero mock panel are optional (not required to keep).
- E Ink industry label: 電子紙顯示器業 (zh) / E-paper displays (en); never 光電業.

## Evidence on Hand

All real content lives in `index.html` and in `../履歷/*.md`, `../專案/**/*.md`: four E Ink projects (TM1 Auto Layout, TM2 Cross Section, CI/CD + MLOps platform, GPU LLM platform), PChome warehouse work with stated % improvements, education, TOEIC 795, JLPT N3, side projects (Auto-Clip, AI Virtual Town, GB10 workstation). No testimonials, logos, or photos — do not invent any.

## Brand Commitments

- Blueprint palette chosen by the user (2026-11-11): cool blue-grey paper, navy ink, cobalt accent.
- Name presented as 趙奕錡 / YICHI CHAO.

## Product Principles

- Screen in seconds, prove in depth.
- Show the engineering (constraints, architecture, numbers), not adjectives.
- Every fact traceable to real work; no inflated claims.
