---
title: "Platform"
status: Current
last_updated: 2026-06-09
audience: [buyers, users, partners, ai-assistants]
tags: [product, platform, accounts, brands, users, security, creative-engines]
---

# Platform

Platform is the shared product foundation that supports accounts, brands, users, access control, secure brand-scoped workspaces, navigation, and the overall application surface.

For a client, the most important point is simple: Creative Engines is designed for repeated work across real organizations and brands, not for one-off anonymous drafting.

## What users can do

The platform layer helps users:

- Work inside an Account that represents an organization, client, or team.
- Create and switch between Brands inside the account.
- Keep brand knowledge, Mindsets, strategy, content, and activity scoped to the correct brand.
- Invite users and manage roles at the account level.
- Move through a consistent product surface across strategy, knowledge, content, and review areas.
- Keep work separated when one team manages multiple brands or clients.

Accounts, Brands, and Users are the basic organizing objects a client needs to understand. The account is the workspace root. A brand is the context where strategy and content live. Users belong to accounts and work with the brands they are allowed to access.

## What it helps decide

Platform helps a client decide:

- Which brand context a user is working in.
- Which people should belong to the account.
- Which roles should manage, create, or review work.
- How a multi-brand or agency workflow should stay organized.
- How to prevent one brand's context from leaking into another brand's work.

## Security posture at client level

Creative Engines uses account and brand scoping so work stays attached to the right client or brand context.

RLS is part of the security posture: data access is constrained so users and product surfaces should only operate within the account and brand scope they are allowed to use. Public documentation can name RLS as a security concept, but does not expose policy definitions or implementation internals.

The platform is also designed around human roles, authenticated users, and controlled workspace membership rather than open, shared, anonymous access.

## How it connects to other product areas

Every product module depends on Platform. [Brand Knowledge](../brand-knowledge/README.md), [Mindset Intelligence](../mindset-intelligence/README.md), [Brand Strategy](../brand-strategy/README.md), [Creative Studio](../creative-studio/README.md), and [Content Distribution](../content-distribution/README.md) all need the same account, brand, user, and permission foundation.

## Public boundary

This page explains platform structure at a client level. It does not publish private workspace controls, private access details, vendor configuration, infrastructure details, or internal operational controls.

## See also

- [Product](../README.md)
- [Accounts, Brands, Users, and Security](./accounts-brands-users-and-security.md)
- [Getting Started](../getting-started/README.md)
- [Brand Knowledge](../brand-knowledge/README.md)
- [Glossary](../../glossary/README.md)
