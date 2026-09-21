# brother + Mission — practice website

Website for **brother + Mission**, a coaching practice I co-founded with friends. It ran mostly pro bono. Earlier names for the same practice were Mizpah Coaching and Your Brother Consulting, which is why both appear in the code and content.

Live: https://brothermission.com

## What is here

- **Next.js 14** (App Router), **TypeScript** and **Tailwind CSS**, with page content managed in **Prismic** through Slice Machine.
- The project started from Prismic's minimal Next.js starter and Prismic's "Glisten" landing-page course. The page sections from that course (Hero, Bento, Showcase, Case Study, Call To Action, Integrations, Rich Text) were adapted to the practice's copy and branding.
- Two sections are my own additions for booking: `src/slices/Calendar` and `src/slices/Appointments`. Both embed a Calendly inline scheduler through `src/components/CalendlyForm.tsx` (`react-calendly`).
- `brand/` holds the current brother + Mission logo.

Most commits are from April to July 2024. In September 2026 the production build was repaired (a client-component directive was missing on the Calendly component) so the scheduler sections deploy again.

## Run it locally

```sh
npm install
npm run dev
```

The site reads content from the public Prismic repository named in `slicemachine.config.json`; no API token is needed to build.

## Honest limits

This is a small marketing site built on top of a course project, not a custom application. Some pages in the CMS still carry placeholder sections from the course. Analytics packages listed in `package.json` (PostHog, HubSpot client) are not wired into the layout.
