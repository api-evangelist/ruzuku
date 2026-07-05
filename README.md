# Ruzuku (ruzuku)

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
