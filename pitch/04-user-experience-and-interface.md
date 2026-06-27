# 04 — User Experience and Interface

Discovr should feel simple before it feels powerful.

The product has several major systems: feed, discovery, profiles, posts, projects, communities, messaging, analytics, search, recommendations, monetization, and platform operations. The interface must make that complexity feel approachable. Users should not feel that they are operating a management console when they only want to browse, publish, or respond.

The experience principle is direct:

> Make the primary action obvious and reveal depth only when it is useful.

A casual viewer should browse without effort. A creator should publish without reading instructions. A project owner should create a project without feeling trapped in an administrative form. A serious user should still be able to access deeper tools when needed.

This chapter defines the user experience and interface direction in neutral product language. It contains no founder-specific examples or references to prior private projects.

---

# Visual standard

The interface direction is clean, white, minimal, rounded, and content-first, with a fully considered dark mode.

The product should feel familiar to users of modern social applications, but it should not copy any specific product. The goal is a calm and premium interface: strong spacing, readable typography, rounded cards, subtle borders, restrained shadows, clear icons, and predictable actions.

The interface should avoid loud visual effects, unnecessary gradients, exaggerated motion, and cluttered dashboard patterns. Discovr’s difference should come from product behavior and trust, not from visual noise.

Light mode should be the primary identity. It should use white or near-white surfaces, dark neutral text, subtle dividers, rounded components, and limited accent color.

Dark mode should be first-class. It should use deep neutral backgrounds, slightly elevated surfaces, readable contrast, and adjusted accent colors. It should not be a quick inversion of light mode.

Rounded corners should be part of the system. Cards, inputs, buttons, modals, message surfaces, project modules, community modules, and analytics summaries should use consistent radius values.

---

# UX principles

The interface should use familiar patterns where they reduce friction. Feed browsing, posting, liking, commenting, saving, sharing, following, search, messages, and profiles should not be made strange for the sake of novelty.

Discovery should feel intentional, not random. When unfamiliar content appears, the interface can provide light context, such as topic labels, community context, project context, or broad relevance indicators. These explanations should remain subtle. The feed should not become crowded with algorithm commentary.

Creation should be fast but structured. The create flow should capture enough context to support audience matching without slowing down casual posting.

Depth should be progressive. Basic cards should remain clean. Analytics, project settings, community tools, and advanced account controls can live deeper in the interface.

Safety and account controls should be available without making the product feel hostile. Users should be able to manage unwanted content, contact, and visibility with clear controls.

Minimalism should not hide functionality. A clean interface still needs visible actions, clear labels, and understandable states.

---

# Layout and spacing

Spacing should make the product easy to scan.

Feed cards should breathe. Project and community cards should be compact enough for browsing but detailed enough to communicate purpose. Profile pages should prioritize identity and action. Search results should clearly distinguish users, posts, projects, and communities.

Mobile tap targets should be comfortable. Desktop layouts can use wider surfaces and multi-column structures, especially for project management and analytics, but text should not stretch across excessive line lengths.

Whitespace should improve comprehension. It should not bury important controls.

---

# Core surfaces

Home is the main feed. Cards should be rounded, readable, and content-first. Actions should remain consistent across post types. Context labels should be used when they help the user understand why something appears.

Discover is the exploration surface. It should feel more structured than Home. It should support search, interest controls, recommended creators, projects, communities, topics, and rising content.

Create is the publishing surface. It should move from content to context to publish. The user should be able to publish quickly, while optional fields support better discovery.

Profile is the identity surface. It should answer who the user is, what they publish, what they are associated with, and what action a visitor can take.

Projects should feel like living social objects, not static forms. Roles, updates, members, media, and application actions should be visible without making the page feel like enterprise software.

Communities should feel active and approachable. A user should quickly understand what the community is, whether it is relevant, and what joining means.

Messaging should be clean, safe, and organized. Requests, regular conversations, project-related conversations, and future group contexts should not collapse into a confusing inbox.

Notifications should be useful and calm. They should communicate what happened without manipulative wording.

Analytics should be explanatory. A creator should understand the broad state of a post without needing to interpret a dense dashboard.

---

# States

Empty states should teach the next action. An empty feed should guide interest selection or discovery. An empty project should encourage updates or role creation. An empty inbox should explain when conversations appear. Empty analytics should explain when data becomes available.

Loading states should preserve perceived speed. Feeds, profiles, projects, comments, and search results should use skeletons or structured placeholders rather than blank screens.

Error states should be specific. A failed upload, unavailable post, permission issue, network failure, or processing delay should explain what happened and how the user can proceed.

Success states should be quiet and clear. Publishing, saving, following, sending, applying, and updating should produce confirmation without excessive animation.

---

# Accessibility

Accessibility is part of product quality.

The interface should support readable text sizes, strong contrast, keyboard navigation on web, visible focus states, screen-reader labels, captions where applicable, alt text where applicable, reduced-motion settings, and large enough mobile tap targets.

The product should not rely on color alone to communicate state. Icons should have labels where ambiguity is likely.

Accessibility should be included from the beginning. It is more difficult and less effective when treated as a late-stage correction.

---

# Motion and interaction

Motion should explain state changes. It should not delay the user.

Useful motion includes opening detail views, saving content, following accounts, switching tabs, expanding project sections, sending messages, showing upload progress, and confirming actions.

Avoid excessive motion, long transitions, decorative animation that competes with media, and animations that cannot be reduced.

---

# Microcopy

Product writing should be direct and professional.

The interface should avoid generic startup hype and overly casual jokes in important states. Clear wording builds trust.

Good product language explains what happened, what is happening, or what the user can do next. Distribution-related language should be especially careful. It should not overpromise reach or imply certainty where the system is still learning.

---

# Design system direction

The design system should define colors, typography, spacing, buttons, cards, inputs, modals, navigation, post cards, project cards, community cards, profile modules, message surfaces, skeleton loaders, empty states, error states, icons, and analytics cards.

The system should support light and dark mode from the start. Components should be reusable across product surfaces while preserving object-specific differences.

The baseline component language is rounded, minimal, readable, and restrained. Primary actions should be visually clear. Secondary actions should remain accessible without competing for attention.

---

# Interface risks

A clean interface can accidentally hide important functionality. Discovr should avoid overly subtle controls and unexplained icons.

A discovery product can also over-explain itself. Too much algorithm text in the feed will create clutter. Context should be useful and restrained.

Projects may become too formal if designed like administrative software. They should remain social and approachable.

Messaging can become difficult to manage if requests, project conversations, and regular conversations are not separated clearly.

Analytics can damage trust if the language appears vague or inflated. The product should be factual and careful.

---

# Chapter conclusion

Discovr’s interface should make a complex product feel simple.

The visual system should be clean, white, minimal, rounded, and content-first, with a polished dark mode. The experience should feel familiar enough to use immediately and clear enough to support serious creator, project, and community workflows.

The interface should not rely on novelty. It should quietly support the deeper system: helping content, people, projects, and communities reach relevant audiences and turn discovery into action.
