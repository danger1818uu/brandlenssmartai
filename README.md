<div align="center">

<img src="assets/brandlens-banner.gif" alt="BrandLens — AI-powered brand governance" width="100%" />

### **Every brand has a standard. Make every post count.**

An AI-powered brand governance workspace for reviewing content against company context, role permissions, and publishing guidelines.

<p>
  <img src="https://img.shields.io/badge/AI-Content%20Governance-a995ff?style=for-the-badge&labelColor=101018" alt="AI Content Governance" />
  <img src="https://img.shields.io/badge/Role-Aware-8ce6d2?style=for-the-badge&labelColor=101018" alt="Role-aware" />
  <img src="https://img.shields.io/badge/Workflow-Review%20%7C%20Improve%20%7C%20Publish-9edfff?style=for-the-badge&labelColor=101018" alt="Review Improve Publish" />
</p>

<!-- Replace the href below with your real hosted application URL. -->
<!-- <a href="YOUR_LIVE_APP_URL"><img src="https://img.shields.io/badge/OPEN-LIVE%20APP-a995ff?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Open live app" /></a> -->

</div>

---

## ✦ What is BrandLens?

**BrandLens helps teams create content that fits the company, the author's role, and the intended platform—before it goes live.**

Instead of checking spelling alone, BrandLens considers the bigger picture: Is this content relevant to the organization? Is the author allowed to make this announcement or commitment? Are the message and media consistent with the configured guidelines and available facts?

The current demo workspace is configured for **Nova Unlimited**, a server and hosting provider. The governance configuration is designed to be adapted for other organizations.

## ⚡ What it can do

| Capability | What it does |
|---|---|
| **Company-aware review** | Checks whether a post relates to the organization's configured business and services. |
| **Role-aware governance** | Evaluates content against the author's assigned responsibilities and permissions. |
| **AI text review** | Reviews titles and captions, explains meaningful concerns, and suggests practical corrections. |
| **Image analysis** | Reviews visual content in the context of the proposed post. |
| **AI image generation** | Creates a concise visual prompt from post context and sends it to the configured image-generation service. |
| **Review workflow** | Tracks content through review, correction, and ready-to-post states. |
| **Post history** | Keeps saved posts, review outcomes, and relevant activity available for later reference. |
| **Social publishing** | Supports the configured account-connection and publishing workflow when platform credentials, permissions, and account authorization are in place. |

## 🧭 How the review works

<div align="center">

`DRAFT` **→** `CHECK` **→** `IMPROVE` **→** `REVIEW AGAIN` **→** `READY TO POST`

</div>

1. **Draft** — choose a platform and add the title, caption, and media.
2. **Check** — review company relevance, role scope, content quality, and supported claims.
3. **Improve** — inspect suggested corrections and apply only the changes you choose.
4. **Review again** — recheck changed content so old findings do not masquerade as current results.
5. **Prepare to publish** — use the connected publishing workflow when the account and platform permissions are configured.

> **Important:** `Ready to Post` is not the same as `Posted`. A post should only be marked published after the applicable publication has actually been confirmed.

## 🛡️ Governance by context

The current **Nova Unlimited** starter configuration distinguishes between three workspace roles:

- **Employee** — product-level and operational content within assigned authority.
- **Manager** — campaigns, team initiatives, project updates, and management-level communications within assigned authority.
- **Administrator** — organization-wide messaging and approved corporate communications within assigned authority.

These are configurable starter guidelines for the current demo organization, not universal rules for every company. BrandLens should flag unsupported claims for verification rather than inventing facts or pretending uncertain information is verified.

## 🧱 Architecture at a glance

BrandLens combines a web workspace with server-side AI integrations and persistent post/task data. The exact framework and deployment-specific services are defined by the source code and environment configuration in this repository.

- **Web experience** — landing page, authenticated workspace, post editor, review states, and history.
- **AI services** — configured text/multimodal review and image-generation integration.
- **Governance context** — organization facts, company guidelines, role scopes, and platform selection.
- **Persistence** — saved posts, media references, review results, and activity/task records supported by the configured backend.
- **Publishing** — platform-specific OAuth and API permissions must be configured before real publication is available.

## 🔐 Configuration & security

- Keep AI API keys, OAuth client secrets, access tokens, and encryption keys on the server.
- Use environment variables or your hosting provider's secret manager for private configuration.
- Do not commit `.env` files, credentials, private tokens, or real customer data.
- Keep a safe `.env.example` with placeholder values only.
- Social publishing requires the relevant developer application, callback URL, permissions, and authorized account.
- Do not describe a platform as connected or a post as published unless the application has confirmed that state.

## 🚀 Getting started

1. Clone this repository.
2. Install dependencies using the package manager indicated by the committed lockfile.
3. Configure the server-side environment variables required by the project. Use a safe `.env.example` as the reference and keep real secrets out of Git.
4. Start the frontend and backend using the development scripts defined by the repository.

> Exact commands depend on the current project configuration. Use the scripts and deployment settings in this repository as the source of truth.

## ✨ Project principles

- **Context over keywords** — evaluate the meaning of a post, not just isolated words.
- **Explainable review** — show useful reasons and actionable corrections.
- **Human decisions** — suggestions assist the author; they are not a substitute for required company approval.
- **Safe integration** — keep API keys and social tokens on the server.
- **One source of truth** — saved posts, review results, and workflow states should stay consistent across the app.

## 🤝 Contributing

Contributions and practical feedback are welcome. Before proposing a change, please preserve the existing governance rules, avoid exposing secrets, and include a brief description of the behaviour being changed.

---

<div align="center">

**Built for clarity. Designed for trust.**

<sub>BrandLens · Company context + Role-aware governance</sub>

</div>

<!-- Maintainer checklist before publishing this README:
1. Replace the commented live-app link with the real hosted URL.
2. Add real screenshots or a short demo GIF to assets/ when available.
3. Replace generic setup guidance with commands verified against this repository.
4. Confirm which social integrations are actually available in production.
-->
