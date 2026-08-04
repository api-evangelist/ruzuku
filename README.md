# Ruzuku (ruzuku)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Ruzuku is a hosted online course platform for coaches, authors, and subject matter experts to create, teach, and sell online courses and learning communities. **Ruzuku does not publish a documented public REST API or developer program.** Its only programmatic surface is a **Zapier integration**, authenticated with an API Key, API Secret, and Site URL generated in the dashboard under *Account → Integrations → Configure Zapier*. The APIs described below are honest logical groupings of that Zapier-mediated surface — they are modeled from the Zapier connector, not from a public Ruzuku API reference, and no public API base URL exists.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ruzuku/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ruzuku/refs/heads/main/apis.yml)

## Access Model

- **No public REST API.** Ruzuku publishes no API reference, no OpenAPI, and no developer portal.
- **Zapier only.** Programmatic access runs entirely through Zapier. You generate an API Key + API Secret + Site URL in Ruzuku and connect them in Zapier.
- **No WebSocket / realtime API.** Trigger events are delivered as Zapier-managed webhook callbacks, not a server-push transport on a Ruzuku endpoint.
- **`endpointsModeled: true`.** The operations listed here are the Zapier connector's triggers and actions, modeled as logical operations — not documented Ruzuku endpoints.

## Tags

- Online Courses
- Learning Management
- Education
- Course Platform
- Zapier
- Gated

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Ruzuku Students and Enrollments API

Student lifecycle actions exposed through Ruzuku's Zapier integration — **Enroll a Student**, **Unenroll a Student**, and **Find a Student** (by email or ID). Authenticated with the API Key, API Secret, and Site URL generated under *Account → Integrations → Configure Zapier*. No direct public REST base URL is published; the surface is modeled from the Zapier connector.

- **Human URL:** [https://support.ruzuku.com/article/796-how-to-set-up-your-zapier-intergration](https://support.ruzuku.com/article/796-how-to-set-up-your-zapier-intergration)

#### Tags

- Students
- Enrollments
- Zapier
- Gated

### Ruzuku Activity Events API

Course-activity event triggers surfaced through Ruzuku's Zapier integration:

- **New Student Enrolled** (includes pricing and coupon data)
- **Lesson Completed**
- **Course Completed**
- **Quiz Submitted** (with score)
- **Assignment Submitted** (with answers)
- **Comment Posted**
- **Subscription Canceled**

Each event carries student and course details, and many can be filtered to a specific course or lesson. These are Zapier-mediated triggers (Zapier-managed webhook callbacks), not a documented public webhook or REST API on Ruzuku.

- **Human URL:** [https://zapier.com/apps/ruzuku/integrations](https://zapier.com/apps/ruzuku/integrations)

#### Tags

- Events
- Webhooks
- Triggers
- Zapier
- Gated

## Plans

Ruzuku is priced as a course-platform subscription, not a metered API product. Zapier access is a feature of the account, not a separately priced API plan.

- **Free** — $0/month, capped at 5 students
- **Core** — $99/month (or $997/year)
- **Pro** — $199/month (or $1,997/year)

See [plans/ruzuku-plans-pricing.yml](plans/ruzuku-plans-pricing.yml). All plans advertise unlimited courses, unlimited videos, and zero transaction fees.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/ruzuku-inc-)
- [Website](https://www.ruzuku.com)
- [Documentation](https://support.ruzuku.com/article/796-how-to-set-up-your-zapier-intergration)
- [Plans](plans/ruzuku-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
