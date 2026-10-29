# Awesome-App-Marketplace-Platform

# Awesome-App-Marketplace-Platform

**Top App Marketplace Platform (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Extension Registries, Federated App Stores, Marketplace Infrastructure & Multi-Vendor Commerce Platforms*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **App Marketplace Platforms**. These tools enable organizations to operate extension registries, federated app catalogs, and multi-vendor marketplaces—from fully managed ecosystem marketplaces with review pipelines and billing infrastructure to self-hosted registries and marketplace engines that give operators complete control over listings, distribution, and revenue.



**Examples** include Shopify App Store, Salesforce AppExchange, Atlassian Marketplace, Google Workspace Marketplace, Zendesk Marketplace, AWS Marketplace, Stripe App Marketplace, Slack App Directory, and QuickBooks App Store (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosting, federated distribution, and open marketplace infrastructure. **Critical note**: No open-source project replicates the full scope of Salesforce AppExchange or Shopify App Store—with billing, review workflows, and enterprise ecosystem integrations. The projects below address specific slices: federated registries, VS Code extension marketplaces, multi-vendor commerce engines, and specialized vertical marketplaces.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Shopify App Store](https://apps.shopify.com/)**

  **Shopify's official app marketplace** for merchants to discover and install apps. **Pricing**: Revenue share model (Shopify takes a percentage of app revenue; terms vary by plan). **Free tier**: Free app listings available; paid apps require billing setup. **Best for**: developers building Shopify apps wanting distribution to millions of merchants with integrated billing.



- **[Salesforce AppExchange](https://appexchange.salesforce.com/)**

  **Enterprise app marketplace** for Salesforce ecosystem. **Pricing**: Listing fees and revenue share vary; security review required. **Free tier**: None for commercial listings; free apps available. **Best for**: ISVs and partners building on Salesforce wanting enterprise distribution with trust signals.



- **[Atlassian Marketplace](https://marketplace.atlassian.com/)**

  **App marketplace** for Jira, Confluence, and other Atlassian products. **Pricing**: Revenue share model; free and paid apps supported. **Free tier**: Free app listings available. **Best for**: developers building Atlassian ecosystem extensions wanting access to a large enterprise user base.



- **[Google Workspace Marketplace](https://workspace.google.com/marketplace)**

  **App marketplace** for Google Workspace integrations. **Pricing**: Free listings; Google takes a share of paid app revenue. **Free tier**: Free app listings available. **Best for**: developers building Google Workspace add-ons and integrations.



- **[Zendesk Marketplace](https://www.zendesk.com/marketplace/)**

  **App marketplace** for Zendesk customer service platform. **Pricing**: Revenue share model; free apps available. **Free tier**: Yes. **Best for**: developers building Zendesk integrations for support teams.



- **[AWS Marketplace](https://aws.amazon.com/marketplace)**

  **Cloud software and services marketplace** for AWS customers. **Pricing**: AWS takes a percentage of sales; private offers available. **Free tier**: Free trials and free products available. **Best for**: software vendors wanting enterprise distribution through AWS procurement.



- **[Stripe App Marketplace](https://marketplace.stripe.com/)**

  **App marketplace** for Stripe ecosystem integrations. **Pricing**: Free listings; Stripe handles billing for apps. **Free tier**: Yes. **Best for**: developers building Stripe-connected apps wanting distribution to Stripe merchants.



- **[Slack App Directory](https://slack.com/apps)**

  **Official directory of publicly available Slack apps** . **Pricing**: Free listings; paid apps handled through Slack billing. **Free tier**: Yes. **Best for**: developers building Slack integrations wanting discovery by workspace admins.



- **[QuickBooks App Store](https://apps.intuit.com/)**

  **App marketplace** for QuickBooks accounting ecosystem. **Pricing**: Revenue share model; free apps available. **Free tier**: Yes. **Best for**: developers building accounting and finance integrations for SMBs.



## Open-Source GitHub Projects



- **[World Vibe Web (WVW)](https://github.com/f/wvw.dev)**

  **Federated app store for open-source, vibe-coded projects** (license per repo) — **the most innovative open-source approach to app marketplace architecture** found in this research. **Features**: Each developer maintains their own `apps.json` in their own GitHub repo; WVW indexes and aggregates them into a unified catalog; **no central authority, no review queue, no 30% cut**; live GitHub stats fetched (declared stars are ignored); categories enforced; deduplication by app ID; AI-curated featured apps via GitHub Agentic Workflows; weekly AI-generated showcase banners . **Tech stack**: Static site generation, GitHub Actions, Tauri + Rust (desktop app), PWA support. **Deploy**: Static hosting (GitHub Pages, wvw.dev) or native desktop app. **Trade-off**: **Not a monetized marketplace**—no billing, no transaction processing, no vendor payouts. It is a discovery layer for free open-source apps. **Best for**: developers wanting a federated, zero-fee alternative to centralized app stores for open-source projects.



- **[Open VSX](https://github.com/eclipse/openvsx)**

  **Vendor-neutral, open-source alternative to the Visual Studio Marketplace** (EPL-2.0) — **the most mature open-source extension registry**, now at **1.0.0** with **600M+ extension downloads per month** . **Features**: Extension publishing, discovery, and distribution for VS Code-compatible editors (VSCodium, Eclipse Theia, Gitpod, Google Cloud Workstations, Salesforce Code Builder); web application for browsing; CLI for publishing; TLS-secured Redis connections; read-only mode; security hardening . **Tech stack**: Java (Eclipse Vert.x), PostgreSQL, Redis. **Deploy**: Self-hosted (Docker) or public Open VSX Registry. **Trade-off**: **VS Code extension ecosystem specific**—not a general-purpose app marketplace. **Best for**: editor/IDE vendors wanting to offer a vendor-neutral extension registry independent of Microsoft's marketplace.



- **[Code Extension Marketplace (Coder)](https://github.com/coder/code-marketplace)**

  **Open-source extension marketplace for VS Code-compatible editors** (license per repo) — **designed for air-gapped and regulated environments**. **Features**: Single binary deployment; reads extensions from local file storage or Artifactory; provides VS Code-compatible API (`/api/extensionquery`); no frontend or author publishing mechanism—extensions are added via CLI (`code-marketplace add`); Helm chart for Kubernetes; `/healthz` endpoint . **Tech stack**: Go. **Deploy**: Single binary, Docker, Kubernetes (Helm). **Trade-off**: **Read-only registry**—no publishing workflow, no browsing UI, no monetization. Extensions must be sourced externally (Open VSX, GitHub, build from source). **Best for**: enterprises running Coder or VSCodium in air-gapped/regulated networks needing a local extension mirror.



- **[Mercur](https://github.com/mercurjs/mercur)**

  **Open-source, headless platform for building multi-vendor marketplaces** (MIT for core; Enterprise modules licensed) — **the strongest open-source engine for building a multi-vendor app/commerce marketplace**. **Features**: Vendor onboarding with lifecycle states (pending_approval → open → suspended); shared catalog with seller allowlists; **offers against master products** (multiple sellers compete on the same product); one checkout splits into per-seller orders; commission computation per order; **automated payouts via Stripe Connect**; admin panel and vendor panel; event-driven, API-first architecture . **Tech stack**: Medusa.js, TypeScript, Node.js, PostgreSQL, Redis, React. **Deploy**: Self-hosted (Docker, Kubernetes) or Medusa Cloud. **Trade-off**: **Commerce marketplace engine, not an app/extension registry**—no extension manifest validation, no plugin lifecycle management, no developer SDKs for app packaging. It is for marketplaces where multiple sellers sell products, not where developers publish apps. **Best for**: operators building B2C/B2B multi-vendor commerce marketplaces who want full source control and no per-transaction platform fees.



- **[BotHive](https://github.com/rishabh3562/BotHive)**

  **Open-source marketplace platform for AI agents and automation tools** (license per repo) — **a purpose-built vertical marketplace** with builder and buyer roles. **Features**: Multi-platform agent listings (Make, Zapier, n8n, Voiceflow, Dialogflow, custom); file uploads (.json, .yaml, .zip); demo videos; pricing options (free, one-time, subscription); builder analytics dashboard; leaderboards and badges; Stripe payments; search and filtering . **Tech stack**: Next.js 14, TypeScript, Supabase/MongoDB, Stripe, Radix UI, Tailwind. **Deploy**: Self-hosted (Node.js + Supabase/MongoDB). **Trade-off**: **Vertical-specific** (AI agents/automation, not general apps); **early-stage** with limited community validation. **Best for**: developers wanting to operate a marketplace for AI agents and automation workflows with monetization built in.



- **[Sandstorm](https://github.com/sandstorm-io/sandstorm)**

  **Open-source platform for running sandboxed web apps on personal servers** (Apache 2.0) — **a self-hosted app store with security-hardened isolation**. **Features**: Curated app marketplace for discovering and installing sandboxed web applications; one-click install; each app runs in an isolated container using Linux kernel security features; centralized authentication (sign in once for all apps); no separate accounts per app . **Tech stack**: C++, Cap'n Proto, Linux containers. **Deploy**: Self-hosted (Linux server). **Trade-off**: **Niche ecosystem**—the Sandstorm app catalog is smaller than mainstream marketplaces; primarily for personal/team self-hosted use, not commercial distribution. **Best for**: individuals and small teams wanting a curated, secure app store for self-hosted web applications.



- **[Tujjar Marketplace Module](https://github.com/dev-taherm/Tujjar)**

  **AI-powered, open-source e-commerce platform** (license per repo) with a **plugin marketplace module** within its Django backend. **Features**: Multi-tenant SaaS architecture; 19 modular Django apps including a `marketplace` app for plugins; AI provider management; drag-and-drop page builder; full REST API . **Tech stack**: Django, Next.js, PostgreSQL, MinIO/S3, Celery. **Deploy**: Docker Compose. **Trade-off**: **The marketplace is a module within a broader e-commerce platform**, not a standalone app marketplace. It manages plugins for the Tujjar ecosystem, not third-party app distribution. **Best for**: developers building on Tujjar wanting an integrated plugin marketplace, or those wanting a reference implementation for Django-based marketplace modules.



### Additional Strong Open-Source Options



- **Medusa Multivendor Marketplace Plugin** (`@techlabi/medusa-marketplace-plugin`) — Medusa 2 plugin (Apache 2.0) that adds vendor stores, super-admin impersonation, and entity separation to a Medusa store . **Note**: Commerce marketplace plugin, not an app registry. **Best for**: Medusa developers wanting multi-vendor capabilities.

- **Saleor Apps** — Open-source apps for Saleor commerce platform (BSD-3 for most apps). Saleor App Store is a Cloud feature; self-hosters install apps manually . **Note**: Individual apps, not a marketplace platform. **Best for**: Saleor users wanting open-source integrations.

- **BlackRoad App Store** — PWA marketplace with 5% platform fee (proprietary license) . **Note**: **Not open source** despite GitHub hosting—"All rights reserved." **Best for**: reference only, not adoption.



**Frameworks for building custom systems**: Combine **Mercur** as the multi-vendor commerce engine for paid app/plugin distribution with **Open VSX** as the registry infrastructure for extension discovery, **WVW** as a federated discovery layer for free open-source apps, and **Code Extension Marketplace** for air-gapped enterprise mirroring—creating an app marketplace stack matched to each ecosystem's distribution model and monetization requirements.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- App marketplace platforms handling developer credentials, billing data, and app permissions must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate security controls for app distribution.

- **The "extension registry" vs. "federated discovery" vs. "multi-vendor commerce" vs. "vertical marketplace" distinction is critical.** **Open VSX and Code Extension Marketplace** are **extension registries**—they distribute editor extensions but do not handle payments or vendor onboarding. **WVW** is a **federated discovery layer**—it indexes apps but does not host, review, or monetize them. **Mercur** is a **multi-vendor commerce engine**—it handles sellers, offers, commissions, and payouts, but for products, not apps. **BotHive** is a **vertical marketplace** for AI agents. **None replicate the full scope of Salesforce AppExchange** (security review, billing, enterprise trust signals).

- **Open VSX is the most mature open-source marketplace infrastructure** in this list—1.0.0 release, 600M+ monthly downloads, and adoption by Google, Salesforce, SAP, and Gitpod . **The trade-off**: it is VS Code extension-specific, not a general-purpose app marketplace.

- **Mercur is the strongest open-source engine for building a monetized marketplace** with vendor onboarding, commissions, and Stripe Connect payouts . **The trade-off**: it is built for product commerce (sellers competing on the same product with offers), not app/plugin distribution. Adapting it for app marketplaces would require custom work on app packaging, manifest validation, and developer SDKs.

- **WVW represents a fundamentally different model**—federated, zero-fee, no gatekeeping . **This is philosophically aligned with open-source values but practically limited**: no monetization, no security review, and discovery depends entirely on GitHub repos. **It is a directory, not a marketplace.**

- **BotHive and Tujjar's marketplace modules are early-stage or embedded.** BotHive has limited community validation and is vertical-specific . Tujjar's marketplace is a plugin module within a larger e-commerce platform, not a standalone offering . **Evaluate maturity carefully before committing production marketplace operations.**

- **Pricing opacity is universal across commercial ecosystem marketplaces.** Shopify, Salesforce, Atlassian, Google, Zendesk, AWS, Stripe, Slack, and QuickBooks all have revenue share or listing fee models that vary by app type, volume, and negotiation. **Validate with direct vendor conversations against your app's pricing model and target ecosystem.**

- Self-hosted open-source solutions require proper server setup, backup configuration, and ongoing maintenance. **Marketplace platforms handle payments and developer credentials**—ensure your hosting meets PCI DSS requirements where applicable and your organization's security standards before processing transactions.



---



**Made for developers, platform teams, and organizations building transparent app marketplace solutions.**

Let's make App Marketplace Platforms more open, data-driven, and developer-friendly.
