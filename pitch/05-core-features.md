# 05 — Core Features

Discovr needs to feel like a complete social platform before its discovery system can matter.

A user should not join and feel like basic features are missing. The platform can have a unique discovery philosophy, but the everyday mechanics still need to work: posting, liking, commenting, saving, sharing, following, messaging, searching, reporting, and receiving notifications.

This chapter defines the core feature set that makes Discovr usable as a social product.

The goal is not to list every future idea. The goal is to define the baseline mechanics clearly enough that the product can be built without guessing what “normal platform features” means.

---

# Feature philosophy

Core features should be simple, predictable, and reliable.

Discovr’s differentiation is discovery. Basic social actions should not become strange unless there is a strong reason. A like should feel like a like. A comment should feel like a comment. A save should save. A follow should follow. A report should report.

The unique behavior should appear in what the system does with these signals.

A save is not only a user convenience. It is a quality signal.

A follow is not only a relationship. It is evidence that discovery produced interest.

A comment is not only engagement. It may indicate conversation quality.

A project application is not only a form submission. It is one of the strongest signs of meaningful connection.

Core features must therefore be designed for both user experience and signal quality.

---

# Accounts

Users need accounts to post, follow, save, message, join projects, join communities, and receive personalized recommendations.

The account system should support:

- Sign up
- Log in
- Log out
- Password reset or magic link flow
- Email verification
- Username selection
- Basic profile creation
- Session management
- Account deletion later
- Account recovery

Authentication should be simple. If signup is too slow, users leave before experiencing the product.

The first version can support email-based signup and OAuth providers later. Google and Apple sign-in are likely useful because they reduce friction.

Accounts should be separate from profiles in the data model. The account represents authentication and ownership. The profile represents public identity.

---

# Usernames and display names

Every user should have a unique username and a display name.

The username is the stable public handle.

The display name is the human-readable name shown in the interface.

Rules:

- Usernames must be unique.
- Usernames should be limited to safe characters.
- Usernames should be case-insensitive for uniqueness.
- Reserved words should be blocked.
- Impersonation should be handled through reporting and verification later.
- Display names can be more flexible.

Usernames matter because they appear in profiles, mentions, URLs, search, messaging, and project ownership.

---

# Profiles

Profiles are covered deeply in a later chapter, but the core feature set requires a baseline.

Users should be able to edit:

- Avatar
- Display name
- Username where allowed
- Bio
- Links
- Interests
- Skills later
- Collaboration status later

Profiles should show:

- Posts
- Projects
- Communities where appropriate
- Follow button
- Message button where allowed
- Basic stats

The profile should not feel empty even for new users. Empty states should guide users to post, add interests, create a project, or follow others.

---

# Posting

Posting is the core creator action.

The MVP should support:

- Text posts
- Image posts
- Carousel posts if practical
- Short video posts if infrastructure supports it
- Project updates
- Community posts

Every post should support:

- Caption or body text
- Media attachment where relevant
- Topics or inferred topics
- Visibility
- Edit caption where appropriate
- Delete
- Report by others
- Moderation status
- Distribution status

Posting should be fast and reliable. Failed uploads should be recoverable. Drafts should be saved where possible.

The create flow should not ask the user for too much metadata, but it should capture enough context for discovery.

---

# Media uploads

Media is expensive and technically important.

The upload system should support:

- Images
- Short videos later
- Thumbnails
- File validation
- File size limits
- File type limits
- Upload progress
- Processing status
- Failed upload recovery
- Deletion

Media should be stored through a system designed for scale, such as Cloudflare R2 or an equivalent object storage layer.

Each media asset should have metadata:

- Owner
- Original filename where appropriate
- MIME type
- Size
- Dimensions
- Duration for video
- Storage path
- Thumbnail path
- Processing status
- Moderation status
- Created time

Media upload limits should be tied to product and business decisions. The free plan should allow meaningful use, while paid plans can support higher storage, larger uploads, and better tools.

---

# Captions and text

Captions help users understand content and help the system classify it.

Caption features:

- Plain text
- Mentions later
- Hashtags or topics
- Links where allowed
- Basic formatting later if needed
- Edit window or edit history decision

Captions should be searchable and used for recommendation context.

The platform should avoid overcomplicated formatting in the MVP. Social posts should remain fast.

---

# Topics and tags

Topics help the discovery system match content with audiences.

Tags can be user-entered, system-inferred, or both.

A good topic system should:

- Help classify posts
- Improve search
- Improve recommendations
- Support communities
- Avoid hashtag spam
- Allow correction by users

The interface can suggest topics after upload.

Example:

“Looks like this post is about Music, Drums, and Live Performance.”

The user can accept, remove, or add topics.

Topics should not become a hack where users add unrelated popular tags to chase reach. The ranking system should detect mismatch between topics and user response.

---

# Likes

Likes are the simplest positive feedback signal.

A like should indicate that the user appreciated the post, but likes are shallow compared to saves, shares, follows, and project actions.

Feature requirements:

- Like a post
- Unlike a post
- Show like count where appropriate
- Store timestamp
- Prevent duplicate likes
- Respect blocked/deleted content

Likes should influence ranking, but they should not dominate it.

A platform that overvalues likes will reward content optimized for quick approval instead of meaningful discovery.

---

# Comments

Comments create conversation and context.

The MVP should support:

- Add comment
- Delete own comment
- Report comment
- Like comment later
- Reply to comment later or in MVP if practical
- Comment count

Comments need moderation controls from the beginning. Comment sections can become hostile quickly.

Users should be able to report comments. Creators should eventually have tools to restrict or manage comments on their own posts.

The ranking system should treat comments carefully. A high comment count can indicate value, but it can also indicate controversy, arguments, or spam.

---

# Replies

Replies allow threaded conversation.

The MVP can either support one level of replies or delay replies until comments are stable.

If replies exist, they should be limited and readable. Deep nested threads are difficult on mobile and can make the interface messy.

Recommended approach:

- Support one level of replies.
- Collapse long reply chains.
- Allow reporting and deletion.
- Avoid infinite nesting.

---

# Saves

Saves are one of the strongest positive signals.

A save means the user wants to return to the content later. That usually indicates more value than a like.

Feature requirements:

- Save post
- Unsave post
- View saved posts privately
- Organize saves into collections later
- Use saves as ranking signal

Saves should be private by default. Public saved collections can be considered later, but private saving is safer and simpler.

Saves are especially important for educational content, project posts, inspiration, tutorials, music discoveries, and creator portfolios.

---

# Shares

Sharing helps content leave its original surface.

Share options:

- Copy link
- Native device share sheet
- Share to another Discovr user later
- Share to message later
- Share to project/community later

Share count can be a strong signal, but not every share is visible to the platform once content leaves Discovr.

The platform should generate clean public URLs for posts, profiles, projects, and communities.

Shared previews should look polished. If someone sends a Discovr link, the preview should include useful title, image, and description metadata.

---

# Follows

Following creates a relationship between a viewer and a creator.

Feature requirements:

- Follow user
- Unfollow user
- See followers/following where appropriate
- Show follower count or hide/soften it as a design decision
- Use follows in feed ranking
- Notify users about new followers where appropriate

Follower count is useful but can also recreate popularity pressure. Discovr should consider how strongly follower counts are displayed.

Possible approaches:

- Show exact counts like normal platforms.
- Show rounded counts after a threshold.
- Emphasize reach and discovery analytics over follower count.

The first version can show follower counts normally, but the product should avoid making follower count the only visible status marker.

---

# Blocks

Blocking is a required safety feature.

When a user blocks another user:

- The blocked user should not be able to message them.
- The blocked user should have limited access to their profile/content depending on privacy rules.
- The blocker should stop seeing the blocked user’s content.
- Existing conversations may be hidden or restricted.
- The block should affect recommendations.

Blocking should be easy to access from profiles, posts, comments, and messages.

---

# Mutes and hides

Not every negative preference requires a block.

Hide and mute features allow softer control.

Potential controls:

- Hide this post
- Not interested
- Show fewer posts like this
- Mute user later
- Mute topic later
- Mute community later

These controls improve feed relevance and reduce user frustration.

They also generate negative signals for recommendation quality.

---

# Reports

Reporting is required for safety and moderation.

Users should be able to report:

- Posts
- Comments
- Profiles
- Messages
- Projects
- Communities
- Project applications

Report categories may include:

- Spam
- Harassment
- Impersonation
- Scam
- Hate or abuse
- Unsafe content
- Stolen content
- Inappropriate media
- Misinformation category later if policy requires it
- Other

Reports should create moderation records with enough context for review.

A report flow should be quick but specific. Users should not need to write an essay, but moderators need usable information.

---

# Notifications

Notifications are the feedback system of the product.

Core notifications:

- Like
- Comment
- Reply
- Follow
- Mention later
- Message request
- Direct message
- Project application
- Project response
- Community invite later
- Post test completed
- Post expanded
- Moderation action

Notifications should be grouped where possible.

A creator should not receive fifty separate notifications if one post gets a burst of likes. Grouping makes the product calmer and more professional.

---

# Messaging

Messaging is a core feature because discovery needs follow-up.

MVP messaging should support:

- One-to-one conversations
- Message requests
- Blocking
- Reporting
- Basic notifications
- Project application context

Later messaging can support:

- Group chats
- Project team chats
- Media sharing
- Reactions
- Pinned messages
- Search within messages
- Voice notes
- Calls only if strongly justified later

The initial messaging system should be safe before it is powerful. Open DMs without controls will create spam and abuse.

---

# Project applications

Project applications are a core feature because Projects are a major differentiator.

An application should include:

- Applicant
- Project
- Role applied for
- Short message
- Relevant links or profile sections
- Status: pending, accepted, rejected, withdrawn
- Conversation link where appropriate

Project owners should be able to review applications and respond.

Applications should not feel like job applications unless the project requires that level of seriousness. The UX should be lightweight enough for creative collaboration.

---

# Search

Search is a core discovery tool.

MVP search should support:

- Users
- Posts
- Projects
- Communities

Search should handle:

- Exact usernames
- Display names
- Keywords
- Topics
- Project titles
- Community names

Later search should become semantic and support queries like:

- “drummer in Mumbai”
- “robotics team looking for programmer”
- “designer for app project”
- “short film editor”

Search should eventually connect strongly with skills, roles, interests, and project needs.

---

# Drafts

Drafts reduce posting anxiety and prevent lost work.

Draft support should include:

- Auto-save text drafts
- Save media draft references where possible
- Resume unfinished post
- Delete draft
- Drafts for project updates later

Drafts are especially important for longer captions, project updates, and posts with multiple media items.

The MVP can start with simple local or server-side drafts depending on architecture.

---

# Editing and deletion

Users should be able to delete their own content.

Editing rules need careful decisions.

Posts may allow caption edits. Media edits are more complex because changing media after engagement can confuse context and moderation.

Recommended approach:

- Allow caption edits.
- Show edited indicator later if needed.
- Do not allow media replacement after publishing in MVP.
- Allow deletion.
- Soft-delete first, then purge according to policy.

Comments should allow deletion. Editing comments can be added later.

---

# Mentions

Mentions allow users to reference other users.

Mentions can be added after core posting is stable.

Feature requirements:

- Type @username
- Autocomplete
- Notify mentioned user
- Respect blocks
- Prevent mention spam

Mention spam can become a problem. Rate limits and notification controls are important.

---

# Links

Links are useful but risky.

Users may want to link to portfolios, GitHub, YouTube, Instagram, websites, ticket pages, project docs, and resources.

Risks include scams, phishing, spam, malware, and low-quality link farming.

The MVP should support links carefully:

- Profile links
- Post links if allowed
- Project links
- Link previews later
- Safety scanning later
- Rate limits for new accounts

Links should not become a loophole for spam distribution.

---

# Bookmarks and collections

Saves are the MVP version.

Collections can come later.

Collections could allow users to organize saved posts into groups:

- Music inspiration
- Robotics ideas
- Design references
- People to message
- Project ideas
- Tutorials

Collections can become powerful, but they should not delay the MVP.

---

# Sharing outside Discovr

External sharing matters for growth.

Every public post, profile, project, and community should eventually have a clean URL.

Shared pages should include:

- Open graph metadata
- Preview image
- Title
- Description
- Call to open Discovr

External sharing helps new users discover the platform without paid acquisition.

---

# Admin basics

Even early versions need admin tools.

Minimum admin abilities:

- View users
- View reported posts
- View reported comments
- View reported profiles
- Remove content
- Restrict accounts
- Resolve reports
- View basic media metadata
- View project reports
- View message reports where policy allows

Without admin tools, moderation becomes manual database work, which is fragile and unsafe.

---

# Feature priority

The first version should prioritize features that prove the core loop.

## Must-have

- Accounts
- Profiles
- Posting
- Media upload
- Feed
- Like
- Comment
- Save
- Share link
- Follow
- Search basics
- Projects basics
- Project applications
- Message requests or basic DMs
- Notifications basics
- Report
- Block
- Creator analytics basics

## Should-have

- Replies
- Drafts
- Topic suggestions
- Community basics
- Post edit captions
- Hide/not interested
- Admin moderation tools

## Could-have later

- Collections
- Mentions
- Advanced group chats
- Scheduling
- Polls
- Paid memberships
- Creator storefronts
- Advanced analytics
- Live streaming
- Calls
- Public API

This priority list should stay flexible, but the product should not delay launch for features that do not prove discovery.

---

# Chapter conclusion

Discovr needs strong basic social mechanics before its discovery system can matter.

The core features are not glamorous, but they are the foundation: accounts, profiles, posts, uploads, likes, comments, saves, shares, follows, blocks, reports, notifications, messaging, search, projects, applications, drafts, editing, and admin basics.

These features should feel familiar and reliable. The unique value comes from how Discovr uses them to create meaningful discovery, safer connection, and better creator feedback.

The first version should not attempt to include every possible feature. It should include enough to make Discovr feel like a real social platform and enough to prove that fairer discovery can work.
