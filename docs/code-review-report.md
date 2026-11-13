# W02 Team: Code Review Report

## Rendered Site

- **Site reviewed:** https://wdd430-portfolio-phi-one.vercel.app/
- **Author shown on the site:** Diego Ledesma.
- **Linked project repositories:** https://github.com/repoProgD/cse340 and
  https://github.com/repoProgD/periodic-elements-visualizer-wdd330
- **Code review issue:** Not yet created. This browser/GitHub access is
  read-only, and the portfolio does not identify its source repository. Confirm
  the assigned teammate repository before filing an issue.

## Findings

- **Minimum requirements:** The home page displays a portfolio heading,
  introduction, two project cards, and a navigation menu. The About page
  displays a short biography and frontend/backend skills.
- **Responsive behavior:** The home page was checked at a mobile-sized browser
  setting and had no horizontal document overflow in that session. The embedded
  browser reported a 300 CSS-pixel layout viewport despite a requested 375
  pixel viewport, so repeat this check in a standard mobile emulator before
  submission.
- **Links:** Home, About, and both project links are present. The About route
  returned HTTP 200. Both project links resolve to public GitHub repositories.
- **`/api/hello`:** The endpoint returned HTTP 200 with
  `{"message":"Hello from Next.js API!"}`.
- **Lighthouse mobile scores:** Performance — 99; Accessibility — 100; Best
  Practices — 100; SEO — 100. Measured with Lighthouse 12.8.2 against the
  deployed home page.
- **CSS Overview:** Chrome DevTools' CSS Overview was not available in this
  browser session. Manual stylesheet inspection found a gray `#ccc` light-mode
  background, `#171717` foreground text, Arial/Helvetica body fonts, and a dark
  color-scheme override. The observed media-query rule was for dark mode; run
  DevTools' CSS Overview to capture color, font, media-query, and unused-CSS
  summaries.
- **Strength:** The portfolio is simple to navigate and presents project
  descriptions alongside direct repository links.
- **Actionable improvement:** Replace the generic browser title “Create Next
  App” with a descriptive title and meta description for Diego's portfolio.

## Issue Draft (Do Not File Until the Repository Is Confirmed)

**Suggested label:** `should-fix`

**Title:** Replace the generic page title and add portfolio metadata

**Problem:** The deployed portfolio uses the browser title “Create Next App,”
which does not identify the site or its owner.

**Impact:** Visitors see a generic title in browser tabs and search previews,
making the portfolio harder to recognize and less discoverable.

**Suggested fix:** Set descriptive page metadata such as “Diego Ledesma |
Portfolio” and a concise description of the portfolio in the app's metadata
configuration.

**Acceptance criteria**

- The home page title identifies Diego Ledesma and the portfolio.
- A meaningful meta description is present.
- The updated title and description are visible in the rendered document head.
