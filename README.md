# Awesome-Date-Time-Utilities

# Top Date & Time Utilities Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Immutable APIs, Tree-Shakeable Functions & Timezone-Aware Parsing*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Date & Time Utilities**. These tools enable developers to parse, validate, manipulate, and format dates across timezones and locales—from lightweight Moment.js-compatible alternatives to immutable, domain-driven libraries inspired by Java's `java.time` package.

**Examples** include date-fns, Day.js, Luxon, Moment.js, js-joda, Spacetime, Tempo, Chrono, Sugar.js, and DateJS (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for modern date handling, timezone support, and open utility infrastructure—ideal for frontend developers, backend engineers, and organizations seeking transparent, vendor-independent date manipulation.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Moment.js CDN / Day.js CDN**  
  CDN-hosted distributions for browser-based date manipulation. **Note**: Both libraries are fully open-source—CDN delivery is a convenience, not a commercial service. **Moment.js is in maintenance mode** and **Day.js is a 2KB alternative with a Moment-compatible API** .

## Open-Source GitHub Projects

- **[date-fns](https://github.com/date-fns/date-fns)**  
  **Modern JavaScript date utility library** (MIT) — **the tree-shakeable function library** . **v4** adds **first-class timezone support** via the `@date-fns/tz` package (`TZDate` class and `tz()` helper) and a new `in` context option that nearly every function accepts . **Pure functions**—each returns a new `Date` and **nothing mutates** . **`parseISO` for ISO strings**, **`isValid()` for validation** (v4 returns `Invalid Date` where v3 threw), and **Unicode TR35 format tokens** (`yyyy`, `dd`, `EEEE`) that differ from Moment's . **Named imports** (`import { addDays } from 'date-fns'`) enable tree-shaking—a bundler drops the 200+ functions you don't import . **The reference implementation for functional, immutable date manipulation** — **choose when you want the smallest bundle and don't need chainable syntax** .

- **[Day.js](https://github.com/iamkun/dayjs)**  
  **2KB immutable date library with a Moment.js-compatible API** (MIT) — **the drop-in Moment replacement** . **If you use Moment.js, you already know how to use Day.js** . **Chainable API** (`dayjs().startOf('month').add(1, 'day').format('YYYY-MM-DD')`) . **Immutable**—all API operations return new instances . **I18n support with on-demand locale loading** (`import 'dayjs/locale/es'`) . **Plugin architecture** for extended functionality (advancedFormat, timezone, etc.) . **The pragmatic choice for projects migrating from Moment** — **2KB versus Moment's 200KB+** .

- **[Luxon](https://github.com/moment/luxon)**  
  **A library for working with dates and times in JavaScript** (MIT) — **the modern Moment successor from the Moment team** . **DateTime, Duration, and Interval types** . **Immutable, chainable, unambiguous API** . **Native timezone and Intl support**—**no locale or timezone files to bundle** . **`DateTime.now().setZone("America/New_York").minus({ weeks: 1 }).endOf("day").toISO()`** demonstrates the chainable, timezone-aware design . **Luxon 4.0 is in planning**—the library continues active development . **Best for**: teams wanting **Moment-like ergonomics with native Intl and timezone support** .

- **[Moment.js](https://github.com/moment/moment)**  
  **Parse, validate, manipulate, and display dates in JavaScript** (MIT) — **the legacy standard** . **In maintenance mode**—**new features are not being accepted** . **A project of the OpenJS Foundation** (Linux Foundation) . **The library that defined JavaScript date handling**—**its API is the compatibility target for Day.js and the migration source for date-fns and Luxon** . **Best for**: existing projects that already use it—**migrate to Day.js or Luxon for new work** .

- **[js-joda](https://github.com/js-joda/js-joda)**  
  **Immutable date and time library for JavaScript** (BSD-3-Clause) — **the domain-driven, ISO-8601-native choice** . **A port of the ThreeTen backport**—the base for **JSR-310 implementation of Java SE 8's `java.time` package** . **Lightweight footprint: 43 kB minified and compressed** with **no third-party dependencies** . **About 2 to 10 times faster than other JavaScript date libraries** . **Supports ECMAScript 5 browsers down to IE9** . **Domain-driven design**: **`LocalDate`** (date without time/zone, for birthdays), **`LocalTime`**, **`LocalDateTime`**, **`ZonedDateTime`**, **`Instant`**, **`Duration`**, **`Period`** . **Robust and stable**—**1,700+ test cases ported from the ThreeTenBP project** . **Best for**: teams wanting **Java `java.time` semantics in JavaScript** with immutability and clean domain modeling .

- **[Spacetime](https://github.com/spencermountain/spacetime)**  
  **A lightweight timezone library** (MIT) — **the timezone-first choice** . **Release 7.17.0** adds an **experimental `spacetime/temporal` wrapper** for the upcoming Temporal standard . **Fixes for invalid dates hanging `.every()` iteration** and **overdue improvements to the `spacetime-geo` plugin** . **Handles timezone aliases**—released a fix for macOS Sonoma returning non-IANA timezone strings like `'CET'` instead of `'Europe/Madrid'`  . **Best for**: applications where **timezone correctness is the primary requirement** and you want a lightweight library .

- **[Tempo](https://github.com/formkit/tempo)**  
  **The elegant JavaScript date library** (MIT) — **the modern, type-safe choice** . **Named exports** (`format`, `addDay`, `isAfter`, `isBefore`, `isEqual`, `parse`) enable tree-shaking . **`format(addDay(new Date(), -2), 'YYYY-MM-DD')`** —**function-based like date-fns** . **Migrated from Moment in real projects**—the Aurelia-SlickGrid migration from Moment to Tempo demonstrates the API replacement pattern . **Best for**: teams wanting **a modern, lightweight alternative with a clean function-based API** .

- **[Chrono](https://github.com/NotSoBot/chrono-node)**  
  **A natural language date parser in JavaScript** (MIT) — **the NLP date parsing choice** . **Extracts dates from arbitrary text**: **"Today", "Tomorrow", "Yesterday", "Last Friday"**, **"17 August 2013 - 19 August 2013"**, **"This Friday from 13:00 - 16.00"**, **"5 days ago"**, **"2 weeks from now"** . **v2 rewritten in TypeScript** with **fully supported languages: English, Japanese, French, Dutch** (German, Portuguese, and Traditional Chinese partially supported) . **`chrono.parseDate('An appointment on Sep 12-13')`** returns a JavaScript Date . **Reference date and timezone options** for context-dependent parsing . **Best for**: applications parsing **human-written date expressions** from text input .

- **[Sugar.js](https://github.com/andrewplummer/Sugar)**  
  **A JavaScript library for working with native objects** (MIT) — **the native-object-extension choice** . **Extends native objects with helpful methods**—intuitive, unobtrusive, and designed to let you do more with less code . **v2.0.4** at **24KB gzipped** . **Date module** includes **date formatting, relative dates, ranges, and localization** . **Custom builds** via the download page or Browserify—**individual modules and methods can be required** (`sugar-date`, `sugar/number/round`) . **Date locales must be explicitly required** (`require('sugar/locales/ja')`) . **Best for**: teams wanting **prototype extensions on native Date** rather than standalone functions .

- **[DateJS](https://github.com/abritinthebay/datejs)**  
  **A JavaScript Date Library** (MIT) — **the historical, parsing-focused choice** . **Extends the built-in Date object** with **better parsing, internationalization support, and syntactic sugar** . **Started by Geoffrey McGill in 2007**, abandoned in 2008, and **forked and maintained** by the community . **Parses hundreds of string formats without providing a date format**: **`Date.parse('today')`, `Date.parse('next friday')`, `Date.parse('July 8th, 2004')`, `Date.parse('10:30 PM EST')`** . **157 languages and dialects supported** via CultureInfo files . **Best for**: legacy projects already using it—**consider date-fns or Day.js for new work** .

### Additional Strong Open-Source Options

- **Temporal (TC39 Proposal)** — The **future JavaScript standard** for date/time (Stage 3) . **Built-in timezone and calendar support**, **immutable objects**, **explicit types** (`PlainDate`, `ZonedDateTime`, `Instant`) . **Not yet available in all browsers**—polyfills exist . **The long-term replacement for all libraries in this list**.
- **moment-timezone** — Timezone support for Moment.js (MIT) . **The timezone companion** for legacy Moment projects.
- **date-fns-tz** — Legacy timezone package for date-fns v3 (MIT) . **Superseded by `@date-fns/tz` in v4** .
- Community **n8n** workflows for date parsing automation and timezone conversion pipelines.

**Frameworks for building custom systems**: Combine **date-fns** for tree-shakeable functional manipulation with **Day.js** for Moment-compatible chainable syntax, **Luxon** for native Intl timezone support, **js-joda** for domain-driven immutable types, and **Chrono** for natural language parsing—creating a comprehensive date handling stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Date libraries must be evaluated for **immutability**, **tree-shakeability**, **timezone support**, and **maintenance status**. **Moment.js is in maintenance mode**—new projects should choose Day.js, date-fns, or Luxon .
- **The "immutable vs. mutable" distinction matters.** **date-fns and Day.js return new instances**—no shared references to mutate accidentally . **Native `Date` setters mutate in place**—every holder of that reference sees the change . **Immutability is the default in modern libraries for good reason.**
- **Timezone support varies critically.** **Luxon uses native `Intl`**—no timezone files to bundle . **date-fns v4 adds `@date-fns/tz`** with `TZDate` and `tz()` . **Spacetime is timezone-first** and handles non-IANA aliases like `'CET'` from macOS Sonoma  . **js-joda provides `ZonedDateTime`** as a first-class type . **Choose based on whether timezone correctness is a core requirement.**
- **The Moment migration path is clear.** **Day.js** is the **drop-in 2KB replacement** with a compatible API—**if you know Moment, you know Day.js** . **date-fns** is the **functional replacement**—tree-shakeable and immutable, but a different API paradigm . **Luxon** is the **modern successor from the Moment team**—native Intl and chainable syntax . **The right choice depends on whether you want API compatibility (Day.js), bundle size (date-fns), or modern timezone handling (Luxon).**
- **Chrono fills a different niche.** It's **not a date manipulation library**—it's a **natural language parser** that extracts dates from text . **Use it alongside date-fns or Day.js** when you need to parse **"next Friday"** or **"5 days ago"** from user input .
- Self-hosted open-source solutions require proper bundle configuration and tree-shaking. **Date libraries are foundational**—breaking changes in parsing or formatting can cascade across applications.

---

**Made for frontend developers, backend engineers, and organizations building transparent date utility solutions.**  
Let's make Date & Time Utilities more open, data-driven, and timezone-aware.
