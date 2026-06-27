# 03 — Product Overview

Discovr is a social discovery platform with familiar social mechanics and a differentiated distribution model.

This chapter is intentionally neutral. It contains no founder-specific examples, private references, location references, personal project names, or examples drawn from prior conversations.

The product has five primary objects: users, posts, profiles, projects, and communities. Supporting systems include feed ranking, search, messaging, notifications, analytics, account controls, administrative tooling, and monetization.

Home is the main feed. Discover is the intentional exploration surface. Create is the publishing flow. Projects organize collaboration. Communities organize interest. Inbox supports follow-up. Profile represents identity.

The early product should prove one loop: a user publishes content, the platform tests it with a relevant audience, the creator receives understandable feedback, and viewers have clear ways to act on what they discover.

---

# Product architecture

Discovr should be designed as a connected product rather than a collection of isolated features.

A post should connect to an author, a profile, topics, analytics, ranking state, and user actions. A project should connect to its owner, members, applications, updates, messages, and discovery surfaces. A community should connect to posts, members, moderators, projects, and recommendations. A message should connect to the relationship or object that created the conversation context.

This connected model is important because discovery should not end at exposure. When a user finds something useful, the product should support the next step. The next step may be following, saving, searching, joining, applying, messaging, or returning later.

The system should therefore be built around object relationships. Those relationships should be clear in the data model, the interface, and the recommendation system.

---

# Core surfaces

Home is the primary passive discovery surface. It should combine followed content, recommended content, first-test content, project updates, community content, and later labeled sponsored placements. It must remain relevant enough that users return frequently.

Discover is the active discovery surface. It should support search, topics, recommended creators, recommended projects, recommended communities, and interest tuning. Discover should feel more structured than Home.

Create is the publishing surface. It should support fast posting while collecting enough context for classification and distribution. It should not force long forms before publication.

Projects are structured collaboration surfaces. They make organized work visible and actionable. They should support descriptions, roles, applications, updates, members, media, links, and project-related conversations.

Communities are recurring interest surfaces. They provide context for content and give users a place to belong beyond the main feed.

Inbox supports follow-up. It should include regular conversations, message requests, and project-related contexts without becoming cluttered.

Profile is the identity surface. It should show who the user is, what they publish, what they are associated with, and which actions are available.

---

# Navigation model

The early navigation should be simple and stable.

A practical mobile structure is Home, Discover, Create, Projects, and Profile, with Inbox available as a persistent top-level icon. Communities can begin within Discover and become more prominent if usage proves the need.

This structure maps to the main product behaviors. Home is browsing. Discover is searching and exploring. Create is publishing. Projects are organized collaboration. Profile is identity. Inbox is follow-up.

Desktop can expose more depth through wider layouts, side navigation, project dashboards, analytics views, and administrative tools. The product should feel consistent across devices, but it does not need to be identical on every screen size.

---

# User journeys

A viewer joins, selects interests, opens Home, sees relevant content from both familiar and unfamiliar sources, saves content, follows accounts, joins communities, and gradually improves the feed through behavior.

A creator joins, sets up a profile, publishes content, receives an initial test, sees distribution feedback, and decides what to create next.

A project owner creates a project, defines its purpose, adds roles, publishes updates, receives interest, reviews applications, and starts conversations with relevant participants.

A community organizer creates or manages a space, establishes rules, publishes or curates activity, and uses discovery surfaces to attract relevant members.

These journeys should feel connected. The product should avoid dead ends where a user discovers something but cannot act on it.

---

# MVP scope

The first version should prove that structured discovery is useful.

The required product includes accounts, profiles, interest onboarding, posting, media upload, Home feed, basic ranking, first-test tracking, likes, comments, saves, shares, follows, search, projects, applications, basic conversations, notifications, creator analytics, account controls, and administrative tools.

Features that can wait include advanced advertising, advanced monetization, paid communities, complex group communication, live formats, public APIs, marketplace transactions, advanced automation, and enterprise workflows.

The product should be ambitious enough to prove the thesis and constrained enough to build reliably.

---

# Operating requirements

The product must be measurable. Every important action should produce structured events that support analytics, recommendations, operations, and future product decisions.

The product must be understandable. Creators should know what happened after they publish. Viewers should have controls over relevance. Project owners should understand whether projects are receiving interest.

The product must be maintainable. Features should be built with clear ownership, clean data models, and obvious upgrade paths.

The product must be trustworthy. Distribution, monetization, account controls, and administrative actions should not feel arbitrary.

---

# Product risks

The main risk is building too broadly before the discovery loop works. A large set of weak features is less valuable than a focused system that proves the central promise.

The second risk is feed quality. If viewers do not find the feed relevant, they will not remain long enough for the discovery system to matter.

The third risk is unclear creator feedback. If creators cannot tell whether their content was tested, the platform will not earn trust.

The fourth risk is project separation. Projects must connect naturally to profiles, posts, search, recommendations, and messaging.

The fifth risk is operational weakness. A social product requires administrative tools, review flows, account controls, and reliable data from the beginning.

---

# Chapter conclusion

Discovr should be a familiar social product with a stronger discovery architecture.

The product is not defined by a single feature. It is defined by how posts, profiles, projects, communities, messaging, search, and analytics work together to create meaningful discovery.

The first version should prove that eligible content can receive relevant first tests, viewers can discover useful unfamiliar content, and users can act on what they find.
