---
title: "Accounts, Brands, Users, and Security"
status: Current
last_updated: 2026-06-09
audience: [buyers, users, partners, ai-assistants]
tags: [product, platform, accounts, brands, users, security, rls, creative-engines]
---

# Accounts, Brands, Users, and Security

Accounts, Brands, Users, and Security are the platform foundations that make Creative Engines usable for real teams, agencies, and multi-brand workflows.

The product is designed around scoped workspaces. A client should understand where the work lives, who can access it, and which brand context the product is using.

## Account

An Account represents the organization or client workspace.

For a direct brand, the account may represent the company. For an agency, the account may represent the agency team managing multiple client brands. For a partner, it may represent the workspace where leads, brands, and handoff artifacts are organized.

The account is the root for membership and workspace organization.

## Brand

A Brand is the working context for strategy, knowledge, Mindsets, narratives, content, and activity.

The brand boundary matters because Creative Engines uses brand-specific knowledge and buyer context. Work for one brand should not accidentally borrow another brand's source material, narrative, or Mindset.

Users can switch brand context so the product knows which brand the current work belongs to.

## User

A User is an authenticated person who belongs to one or more accounts.

Users can be invited into an account and assigned a role. Roles help decide who can manage the workspace, create work, review content, or operate inside the product.

The public docs describe roles at a client level only. They do not publish permission matrices or policy definitions.

## Security posture

Creative Engines is designed around account and brand scoping.

RLS is part of that posture. At a client level, RLS means access is constrained so product surfaces and users should only operate within the scope they are allowed to use.

The platform combines authenticated users, account membership, brand context, and scoped access control so multi-brand work can stay organized and separated.

## What this enables for clients

This foundation supports:

- Agency teams managing several client brands.
- Internal teams separating multiple products or business units.
- Partners creating public entry points that route into the right workspace.
- Review processes where the right people can inspect the right brand context.
- Safer use of source knowledge, Mindsets, and content assets across repeated work.

## Public boundary

This page explains workspace and security concepts at a client level. It does not publish private data structures, access-policy details, vendor configuration, operator controls, or infrastructure details.

## See also

- [Platform](./README.md)
- [Product](../README.md)
- [Brand Knowledge](../brand-knowledge/README.md)
- [Getting Started](../getting-started/README.md)
- [Glossary](../../glossary/README.md)
