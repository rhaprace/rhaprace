# Rafael Race

Software developer focused on web and mobile applications.

[LinkedIn](https://linkedin.com/in/rafael-race-54033719b) · [Email](mailto:rhap.dev@gmail.com) · [Portfolio](https://rhaprace.github.io/)

## About

I build web and mobile applications, with an emphasis on clean code and interfaces that feel obvious to use. I care about shipping work that holds up. Code the next person, including future me, can read and change without friction.

## What I work with

- **Frontend:** React, React Native, TypeScript, Next.js
- **Backend:** Ruby on Rails, Node.js, FastAPI, Flask
- **Data & infra:** PostgreSQL, GraphQL, Drizzle ORM, REST APIs, Git, Vercel
- **AI:** prompt engineering and AI-assisted product features

## How I work

- Clarity over cleverness
- Users over features
- Ship, learn, improve
- Solve real problems, not imaginary ones

## Recent work

Since January 2026 I've merged over 1,000 pull requests into a production rugby analytics platform used by clubs and governing bodies. It's a React/TypeScript single-page app on a Ruby on Rails and GraphQL backend. I own features end to end, from spec through backend, frontend, tests and rollout, and I hold merge authority on the work I ship.

The pieces I'm proud of:

- **Migrated the core analysis page onto the new SPA.** The screen coaches spend most of their time in: video player, event timeline, full stats infographic, clips, downloads and presentations. React and the legacy layer can't share a screen, so the smallest safe unit of work was the whole page. 114 files in one pass, with no loss of function for coaches mid-season.
- **Rebuilt the presentation animation engine in TypeScript.** Replaced a 4,900-line legacy canvas engine with a framework-free TypeScript class, porting the rendering pipeline, camera, undo/redo and autosave with the original math and order of operations intact, so coaches saw no change in behaviour. One implementation, fully typed, legacy layer deleted.
- **Cut the cold-load bundle back under budget.** Traced a size regression to the generated GraphQL document map, which baked every operation into the entry chunk as a parsed AST plus its query text and couldn't be tree-shaken. Switching codegen to string documents dropped the GraphQL parser from the bundle entirely: initial load 210.0 KB to 200.2 KB gzipped, entry 122.5 KB to 113.5 KB, with no call sites changed.
- **Decoupled the SPA's dependency tree.** The app declared 13 dependencies and quietly inherited 45 more from the legacy bundle, so a root-level version bump could break it and React would split across worktrees. Gave it a real, pinned dependency tree of its own and closed that whole class of bug.
- **Gave every email an unsubscribe path.** Coaches had no way out of notification emails short of marking us as spam. Added a signed-token unsubscribe page and a List-Unsubscribe header, and made every send path honour the opt-out, matching how consent already worked on the other channels.
- **Took the in-app AI assistant from answering to acting.** It now proposes real changes to a coach's data and applies them once the coach confirms, rather than just describing what to do.

---

*"Make it work. Make it right. Make it fast. Make it beautiful."*
