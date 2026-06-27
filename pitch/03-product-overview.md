# 03 — Product Overview

Discovr is a social discovery platform.

The product should feel familiar immediately: a user opens the app, scrolls a feed, posts content, interacts with people, follows creators, joins communities, sends messages, and creates or discovers projects. The platform should not require a complicated explanation before it becomes usable.

The deeper product difference is what happens behind those familiar actions. Discovr gives eligible posts a relevant first audience, measures meaningful response, and expands distribution when the content earns it. The same philosophy extends beyond posts. Projects, communities, profiles, and creators should also be discoverable based on relevance rather than only existing size.

This chapter defines the overall product model: the main surfaces, user flows, content objects, interaction systems, and early feature boundaries.

It does not define every technical detail. Later chapters cover feed ranking, database architecture, infrastructure, AI systems, security, moderation, monetization, and interface behavior in greater depth.

---

# Product model

Discovr is built around five major product objects:

1. Users
2. Posts
3. Profiles
4. Projects
5. Communities

Messaging, search, notifications, analytics, and monetization support those objects.

The feed is the primary discovery surface, but it is not the only product. Discovr should avoid becoming a feed-only platform where everything begins and ends with scrolling. The feed introduces people, posts, projects, and communities. The rest of the product gives users a reason to act on what they discover.

The simplest model is:

- Posts create attention.
- Profiles create identity.
- Projects create collaboration.
- Communities create context.
- Messaging creates follow-up.
- Analytics create trust.
- Search creates intentional discovery.
- Monetization creates sustainability.

A user can experience Discovr casually as a normal social app. A serious creator can use it as a growth tool. A project owner can use it to find collaborators. A community organizer can use it to grow a space. A business can eventually use it to find creators or sponsor relevant opportunities.

The product should support all of these paths without forcing every user into every feature.

---

# Primary navigation

The first usable product should have simple navigation.

A likely mobile tab structure:

1. Home
2. Discover
3. Create
4. Projects or Communities
5. Inbox
6. Profile

Because mobile tab bars usually cannot comfortably hold six items, the first version may need to choose between a five-tab model and a hybrid model.

A practical five-tab model:

1. Home
2. Discover
3. Create
4. Inbox
5. Profile

Projects and Communities can live inside Discover at first, then become separate tabs once usage proves they deserve first-class placement.

A more ambitious five-tab model:

1. Home
2. Discover
3. Create
4. Projects
5. Profile

Inbox can be placed in the top-right corner, similar to many social apps.

The best early decision is likely:

- Home as the default feed
- Discover as the exploration hub
- Create as the central creation action
- Projects as a major product section accessible from navigation
- Inbox as a top-level icon
- Profile as a persistent user destination

The exact layout can be tested, but the information architecture should keep these ideas clear.

---

# Home

Home is the main feed.

It is the first surface most users will open and the surface most responsible for proving the product promise.

The Home feed includes:

- Posts from followed creators
- Recommended posts from non-followed creators
- Initial discovery tests for eligible posts
- Community posts
- Project updates
- Trending posts where relevant
- Local or interest-based posts where appropriate
- Eventually, clearly labeled sponsored content

Home should not feel random. Users should understand why the feed feels relevant even when it includes unknown creators.

The feed should balance several categories:

## Familiar content

Content from followed creators and communities provides continuity. Users need some predictability.

## Discovery content

New or unknown creators receive controlled feed inventory. This is where Discovr proves its mission.

## Interest-based content

Posts related to selected interests, joined communities, saved posts, watched content, project involvement, and search behavior.

## Project content

Updates from followed projects, recommended projects, and project posts relevant to the user’s interests.

## Fresh content

Recently posted content that needs early testing.

## Proven content

Content that has already performed well and is likely to be valuable to a broader audience.

The feed should not become a pure popularity machine. It also should not become an obligation feed where users are forced to see weak content just because it is new. Feed quality and discovery fairness must be balanced.

---

# Discover

Discover is the intentional exploration surface.

Home answers: “What should I see now?”

Discover answers: “What can I find?”

Discover should include:

- Search
- Trending topics
- Recommended creators
- Recommended communities
- Recommended projects
- Interest categories
- Local discovery where appropriate
- New creators
- Rising posts
- Featured projects
- Suggested collaborations
- Popular tags or topics

The search bar should be prominent. Search should eventually support posts, users, projects, communities, topics, and media captions.

Discover should also help users adjust their interests. If the feed is becoming repetitive or irrelevant, Discover gives users a way to steer the system intentionally.

Potential Discover sections:

## Rising creators

Creators who are gaining traction through discovery but are not already massive.

## New and notable posts

Posts that performed strongly in early tests.

## Projects looking for people

Projects with open roles that match the user’s interests or skills.

## Communities to join

Interest spaces that match user behavior and onboarding preferences.

## Topics

Broad categories such as music, robotics, film, design, startups, gaming, photography, coding, education, fashion, art, sports, and local scenes.

Discover should feel more organized than Home. Home is a stream. Discover is a map.

---

# Create

Creation must be fast.

If posting feels heavy, users will not post casually. If posting is too loose, the discovery system may not have enough context to match the post well. The create flow must balance speed with structured metadata.

Supported post formats should eventually include:

- Text
- Images
- Carousels
- Short videos
- Longer videos later
- Links with previews
- Polls later
- Project updates
- Community posts

The first version does not need every format. It should prioritize the formats that prove discovery:

- Text posts
- Image posts
- Short video posts if media infrastructure is ready
- Project updates

Every post should support:

- Caption or body text
- Media where relevant
- Topic selection or inferred topics
- Visibility setting
- Community selection where relevant
- Project attachment where relevant
- Draft state
- Delete option

The creation flow should encourage users to add enough context for matching without making posting annoying.

For example, after a user uploads a drum cover, the system may infer topics like music, drums, live performance, cover, rock, or practice. The user can confirm or edit them. This helps the initial discovery test.

Creation should support both casual posts and serious work.

A casual user should be able to post in seconds.

A serious creator should be able to refine caption, topics, project attachment, thumbnail, alt text, and scheduling once those features exist.

---

# Posts

Posts are the primary content unit.

A post can be created by a user, attached to a project, submitted to a community, or recommended through the feed.

Core post fields include:

- Author
- Caption or body
- Media assets
- Post type
- Topics
- Visibility
- Created time
- Engagement counts
- Moderation status
- Distribution status
- Project attachment where relevant
- Community attachment where relevant

Post interactions include:

- Like
- Comment
- Reply
- Save
- Share
- Follow author
- Visit profile
- Report
- Hide
- Block author
- Open project
- Open community
- Message where allowed

The platform should treat posts as both user-facing objects and ranking objects. A post has content, but it also has signals, distribution state, audience history, safety state, and analytics.

The user-facing post should remain clean. The system-facing post can be complex.

---

# Profiles

Profiles are the identity layer of Discovr.

A profile should work for both casual users and serious creators.

At minimum, a profile includes:

- Avatar
- Display name
- Username
- Bio
- Posts
- Followers/following or a simplified relationship model
- Links
- Interests

A stronger Discovr profile also includes:

- Featured posts
- Featured projects
- Skills
- Collaboration status
- Communities
- Achievements or badges
- Location where appropriate
- Portfolio sections
- Creator analytics visible only to the owner

Profiles should answer what a person creates, what they care about, and whether there is a reason to connect.

This matters because Discovr is not only about consuming posts. If a user discovers someone interesting, the profile should help the user decide what to do next: follow, message, invite, apply, support, or explore more work.

Profiles also support trust. Project owners, collaborators, community moderators, and businesses need signals that help them evaluate people without turning the platform into a rigid professional network.

The tone should remain social-first, not corporate-first.

---

# Projects

Projects are persistent collaboration pages.

They are one of Discovr’s most important differentiators.

A project represents something being built, organized, produced, performed, launched, or explored.

Examples:

- A band creating an EP
- A robotics team building a competition robot
- A developer building an app
- A filmmaker assembling a crew
- A photographer planning a shoot
- A school club organizing an event
- A designer launching a clothing brand
- A game developer recruiting artists
- A startup looking for early teammates
- An open-source tool seeking contributors

A project page includes:

- Title
- Description
- Banner
- Category
- Owner
- Members
- Roles needed
- Application flow
- Updates
- Milestones
- Media
- Links
- Location or remote status
- Follow button
- Join/apply button

Projects create a structured path from discovery to collaboration.

Without Projects, users can still DM each other, but collaboration remains messy. Projects make intent visible. They show what is being built, who is involved, what is needed, and how someone can join.

Projects should be discoverable through:

- Project tab or section
- Discover page
- Search
- Feed updates
- Profile attachments
- Community links
- Recommended collaboration modules

Projects should not replace posts. They organize work that posts can update.

---

# Communities

Communities are interest-based spaces.

They provide context for users, content, and recommendations.

A community can be based on:

- Topic
- Skill
- Location
- School
- Creator
- Project
- Industry
- Genre
- Event
- Hobby

Examples:

- Drummers
- VEX Robotics
- Mumbai Creators
- Indie Game Dev
- UI Design
- Photography
- Student Startups
- Short Films
- Music Producers
- Fashion Design

Communities include:

- Name
- Description
- Rules
- Members
- Moderators
- Posts
- Discussions
- Projects
- Events later
- Challenges later

The first version can keep communities simple. Public communities with posts, members, rules, and moderators may be enough. Private communities, roles, channels, events, and advanced moderation can come later.

Communities are important because they help solve the wrong-audience problem. A post submitted to a relevant community can be tested among people who already care about the topic.

Communities also improve retention. Users return not only for the feed but for spaces they belong to.

---

# Messaging and chat

Chat is a core feature because discovery needs follow-up.

If Discovr helps users find creators, collaborators, project owners, and communities, the product must give them safe ways to communicate. Otherwise, the most important actions move to Instagram, WhatsApp, Discord, email, or other tools.

The messaging system should eventually include:

- One-to-one DMs
- Message requests
- Group chats
- Project chats
- Community-related chats or threads
- Creator-business conversations
- Media sharing
- Link sharing
- Reactions
- Read receipts as an optional design decision
- Blocking and reporting
- Spam protection

The MVP does not need a full Discord replacement. It needs the basics:

- Users can message mutuals or approved contacts.
- Non-followed users can send message requests.
- Project applications can create structured conversation.
- Users can block and report message abuse.

Chat must be designed with safety. Open messaging can quickly become spammy or unsafe. Message requests, rate limits, media restrictions from unknown users, and stronger defaults for younger users are important.

Messaging should support the core sentence:

> I discovered you. Can we talk?

That is central to meaningful connection.

---

# Notifications

Notifications bring users back and help them understand what happened.

Notification types include:

- Likes
- Comments
- Replies
- Follows
- Saves milestones where appropriate
- Shares where visible
- Message requests
- DMs
- Project applications
- Project acceptance/rejection
- Project updates
- Community activity
- Post distribution milestones
- Safety or moderation notices
- Subscription or billing events later

Notifications should not become spam. A discovery platform can generate many events, especially if posts receive initial tests. The product must decide which notifications are useful enough to interrupt the user.

Creator-facing notifications about distribution should be especially thoughtful.

Examples:

- “Your post completed its first discovery test.”
- “Your post is expanding to a wider audience.”
- “Your project received a new application.”
- “A community is discussing your post.”

The tone should be factual, not manipulative.

---

# Search

Search is intentional discovery.

The feed helps users find things they did not know to ask for. Search helps users find things they already know they want.

Search should eventually cover:

- Users
- Posts
- Projects
- Communities
- Topics
- Tags
- Captions
- Skills
- Locations where appropriate
- Roles needed in projects

Search should support exact matching and semantic discovery over time.

A user should be able to search:

- “drummer Mumbai”
- “VEX robotics”
- “looking for designer”
- “indie rock vocalist”
- “app developer”
- “photography project”
- “school startup”

Search connects strongly to Projects and Profiles. If profiles include skills and projects include roles, search becomes more valuable than normal social search.

The first version can use simpler text search, but the data model should leave room for richer search later.

---

# Creator analytics

Analytics are not an advanced extra. They are part of the discovery promise.

Creators need to know what happened after posting.

Basic analytics should include:

- Views or impressions
- Likes
- Comments
- Saves
- Shares
- Profile visits
- Follows gained
- Initial test status
- Expansion status
- Audience interests in broad categories
- Negative feedback where appropriate

Project analytics should include:

- Project views
- Followers
- Applications
- Role interest
- Update reach
- Member activity later

Community analytics should include:

- Member growth
- Active members
- Post activity
- Report volume
- Trending posts

Analytics should be understandable, not overwhelming.

The first version can show simple numbers and plain-language status. Later versions can add deeper dashboards for serious creators, project owners, communities, and businesses.

---

# Onboarding

Onboarding must teach the system enough to make early recommendations useful without becoming boring.

The user should provide:

- Username
- Display name
- Basic profile setup
- Interest selection
- Optional skills
- Optional creator intent
- Optional project/collaboration intent

Interest selection is important because Discovr needs relevance from the start. A new user’s first feed should not be random.

Possible onboarding questions:

- What do you want to see?
- What do you create?
- What are you building?
- Are you open to collaboration?
- Which communities interest you?

The onboarding should be skippable in parts, but the product should strongly encourage interest selection.

For users who only want to browse, onboarding should be light.

For creators and builders, onboarding can unlock profile and project suggestions.

---

# Account types

The first version should avoid overly complex account types.

Everyone can begin with a normal user account.

Additional modes can be layered on:

## Creator mode

Enables deeper analytics, creator profile modules, monetization eligibility later, and post management tools.

## Project owner mode

For users who create and manage projects.

## Community moderator mode

For users who manage communities.

## Business profile

For brands, organizations, schools, agencies, event organizers, and companies later.

The product should not require users to choose a rigid identity at signup. A user can become a creator, project owner, moderator, or business user over time.

This reduces friction and keeps the platform flexible.

---

# Visibility and privacy

Discovr needs clear visibility rules.

Content may be:

- Public
- Followers-only later
- Community-only
- Project-only
- Private draft
- Unlisted later

Profiles may have controls for:

- Public visibility
- Message permissions
- Collaboration availability
- Location visibility
- Social links
- Project visibility
- Minor safety defaults

The first version should keep privacy understandable. Too many visibility states can confuse users and complicate ranking. Public posting, drafts, community posts, and project updates may be enough at first.

Messaging privacy is especially important. Users should control who can DM them, who can send requests, and who can include them in groups or projects.

---

# Moderation and reporting surface

Every major object needs reporting and safety controls.

Users should be able to report:

- Posts
- Comments
- Profiles
- Messages
- Projects
- Communities
- Project applications

Users should be able to:

- Block accounts
- Hide posts
- Delete own posts
- Leave communities
- Leave projects
- Reject message requests
- Report spam

Admins should eventually have internal tools to review reports and take actions. The product cannot depend only on database access or manual hacks.

Moderation is part of the product surface because users need visible safety tools.

---

# MVP boundary

The MVP must prove the core loop without trying to build the entire long-term platform.

A reasonable MVP includes:

- Sign up and login
- Profile setup
- Interest onboarding
- Create posts
- Upload images and text, with short video if infrastructure supports it
- Home feed
- Basic recommendation logic
- Initial discovery test tracking
- Like, comment, save, share
- Follow
- Basic search
- Basic projects
- Project applications
- Message requests or basic DMs
- Notifications
- Creator analytics
- Report and block
- Admin moderation basics

Features that can wait:

- Advanced ads
- Complex creator monetization
- Paid communities
- Live streaming
- Advanced video editing
- Full group voice/video calls
- Enterprise tools
- Deep AI assistants
- Complex community roles
- Marketplace transactions
- Public API

The MVP should be ambitious enough to prove Discovr’s reason to exist, but not so broad that the product collapses before the core loop works.

---

# Product risks

## Too many features too early

Discovr includes feed, projects, communities, messaging, analytics, search, monetization, and moderation. That can become too much. The first version must prioritize the loop of posting, discovery testing, engagement, feedback, and follow-up.

## Feed fails to feel good

If the feed is boring or irrelevant, users will not care about fairness. Feed quality is non-negotiable.

## Projects feel separate from the social product

Projects must connect to posts, profiles, search, chat, and discovery. If they feel like a random extra tab, users may ignore them.

## Chat becomes unsafe or spammy

Messaging is necessary, but it must have request controls, reporting, blocking, and rate limits.

## Analytics overpromise precision

The product should explain distribution clearly without pretending to know more than it does.

## Monetization damages trust

Paid features must not make the basic discovery promise feel fake.

---

# Product direction

Discovr should start as a social platform that proves fairer discovery through a familiar feed.

The first product goal is not to build every possible tool. The first goal is to make users feel a specific difference:

- Creators feel their posts are actually tested.
- Viewers feel they are finding fresh, relevant people.
- Projects feel discoverable.
- Communities feel easier to find.
- Messaging lets discovery continue into conversation.

Once that core experience works, the platform can expand into deeper creator tools, monetization, advertising, advanced recommendations, richer communities, and professional project workflows.

The product should grow from the discovery loop outward.

---

# Chapter conclusion

Discovr is a familiar social platform with a discovery-first structure.

The main product surfaces are Home, Discover, Create, Projects, Communities, Inbox, and Profile. The main objects are users, posts, profiles, projects, and communities. The support systems are messaging, search, notifications, analytics, moderation, and monetization.

The first version should prove that eligible posts can receive meaningful initial tests, that users enjoy discovering unknown but relevant creators, and that discovery can lead to follow-up through profiles, projects, communities, and chat.

The product should remain simple enough to use casually and deep enough to support serious creators and builders over time.

This chapter defines the product shape. Later chapters define the details of each system.
