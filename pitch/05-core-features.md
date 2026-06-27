# 05 — Core Features

Discovr needs reliable core social mechanics before its discovery system can matter.

The platform can have a differentiated distribution model, but users will still expect the basic product to work clearly: accounts, profiles, posting, uploads, likes, comments, saves, shares, follows, search, messaging, notifications, projects, communities, analytics, and account controls.

This chapter defines the baseline feature set in neutral product language. It avoids founder-specific examples and should be treated as an implementation-oriented roadmap document.

---

# Feature philosophy

Core features should be predictable.

A like should feel like a like. A save should save. A follow should follow. A message should send. A report should create an operational record. The product should not make basic actions unusual without a strong reason.

The distinctive behavior should appear in how Discovr interprets these actions. A save is a convenience feature and a quality signal. A follow is a relationship and proof that discovery created interest. A project application is a workflow action and a strong indicator of intent. A hide action is a user control and a ranking signal.

The feature system must serve the user interface, the discovery engine, analytics, and operational reliability at the same time.

---

# Accounts and identity

Users need accounts to publish, follow, save, message, join communities, create projects, and receive personalized recommendations.

The account system should support signup, login, logout, verification, session management, recovery, profile creation, account settings, account deletion, and account state management.

Account and profile should be separate concepts. The account represents authentication and ownership. The profile represents public identity.

Account states should include active, unverified, restricted, suspended, and pending deletion. These states matter because the platform should not treat every account as equally trusted for posting, messaging, upload limits, and distribution eligibility.

Usernames should be unique, stable, readable, and protected from reserved terms. Display names can be more flexible but still need operational rules against misleading use.

---

# Profiles

Profiles convert attention into identity.

A basic profile should include avatar, display name, username, bio, links, posts, follow action, message action where allowed, and basic account context. Later versions can add featured posts, featured projects, skills, availability, communities, badges, and creator analytics.

The profile should answer who the person or entity is, what they publish, what they are associated with, and what action a visitor can take next.

Profiles should remain social and readable. They should not become dense professional resumes unless the user chooses to expose more structured information.

---

# Posting and uploads

Posting is the core creator action.

The first version should support text posts, image posts, project updates, and community-attached posts. Short video can be included if media infrastructure is ready. More complex formats can come later.

Every post should support caption or body text, media where relevant, topic metadata, visibility state, edit rules, deletion, review state, and distribution state.

Media uploads require validation, file limits, processing status, thumbnails, metadata, storage paths, deletion rules, and clear user feedback. Upload failures should be recoverable. Drafts should preserve work where possible.

A post should have lifecycle states such as draft, uploading, processing, published, under review, limited, removed, and deleted. The interface does not need to expose every internal state, but the system needs them for reliability.

---

# Captions, topics, and metadata

Captions help users understand content and help the system classify it. They should be searchable and usable for recommendation context.

Topics help the discovery engine match content to audiences. Topics can be user-entered, system-inferred, or both. The system should treat user-entered topics as useful but not automatically correct.

A topic system should improve classification, search, recommendations, community routing, and analytics. It should not become a shortcut for unrelated reach. Repeated mismatch between declared topics and actual response should reduce confidence in that metadata.

---

# Engagement features

Likes are simple positive feedback. They are useful but shallow.

Comments create conversation and context. Comment volume should be interpreted carefully because quantity does not always equal quality.

Replies can support conversation but should avoid deep nesting in the first version. A single reply level is likely enough for the early product.

Saves are a strong positive signal because they indicate that a user wants to return to content later. Saves should be private by default.

Shares help content travel outside the feed. Public posts, profiles, projects, and communities should eventually have clean shareable URLs with polished previews.

Follows create relationships between users and accounts. Follower count is useful but should not become the only visible status indicator in the product.

---

# Negative preference and account controls

Users need ways to control relevance and unwanted interaction.

The product should support hiding content, indicating disinterest, muting later, blocking, and reporting. These controls protect the user experience and provide important ranking and operations signals.

Reports should be available for posts, comments, profiles, messages, projects, communities, and applications. The reporting flow should be quick enough for users and specific enough for review.

Administrative tools should exist early. Operating a social product through database edits is not acceptable. The team needs interfaces for reviewing records, resolving reports, restricting accounts, and auditing administrative actions.

---

# Messaging

Messaging is a core feature because discovery needs follow-up.

The first version should support direct conversations, message requests, project-related context, basic notifications, and user controls. More advanced group and team messaging can come later.

Message requests are important because they allow discovery-driven contact without placing every new interaction directly into the main inbox.

Messaging should be reliable, organized, and connected to projects and profiles. It should not attempt to replace every communication tool in the first version.

---

# Projects and applications

Project applications are core because Projects are a differentiating product surface.

An application should include applicant, project, role or participation type, short message, relevant profile context, status, and conversation context where appropriate.

Applications should be lightweight enough for social collaboration and structured enough that project owners can manage them.

Application activity is one of the strongest indicators that discovery produced intent.

---

# Search

Search is intentional discovery.

The first version should support search across users, posts, projects, and communities. Results should be grouped by object type so the user understands what has been found.

Later versions can add semantic search, role search, skill search, topic search, and richer filters. Search should eventually connect strongly with projects, profiles, communities, and discovery analytics.

All search examples in this specification should remain generic and should not reference founder-specific interests, locations, organizations, or prior private projects.

---

# Drafts, edits, and deletion

Drafts reduce lost work and posting anxiety. The product should support basic draft preservation for text and project updates, with media draft handling added as infrastructure allows.

Editing rules should be clear. Caption editing can be allowed. Media replacement after publication should be delayed until the implications for integrity, analytics, and review are understood.

Deletion should remove public access quickly. Backend retention may exist temporarily for operational reasons, but user-facing behavior should be clear and consistent.

---

# Notifications

Notifications should communicate relevant events without creating unnecessary noise.

Core notification types include comments, replies, follows, messages, project applications, project responses, community activity, distribution milestones, and account notices.

Notifications should be grouped where possible and written in a factual tone. The product should avoid manipulative notification language.

---

# Feature priority

The first version should prioritize the features that prove the discovery loop: accounts, profiles, posting, media upload, feed, basic ranking, likes, comments, saves, shares, follows, search, projects, applications, message requests or basic conversations, notifications, creator analytics, user controls, and administrative tools.

Secondary features include replies, drafts, topic suggestions, community basics, caption editing, disinterest controls, and stronger internal tools.

Later features include collections, mentions, advanced group messaging, scheduling, polls, advanced monetization, deep analytics, live formats, public APIs, and marketplace mechanics.

---

# Chapter conclusion

Core features are not the differentiator by themselves, but they are the foundation that allows the differentiator to work.

Discovr must feel like a reliable social product before users will trust its discovery system. The early product should include enough functionality to publish, browse, interact, follow up, manage identity, organize projects, join communities, understand outcomes, and operate the platform responsibly.

The system should remain familiar at the action level and distinctive at the distribution level.
