# 04 — User Experience and Interface

Discovr should feel easy before it feels powerful.

The product has a large long-term vision: discovery, posts, profiles, projects, communities, messaging, analytics, creator tools, monetization, search, recommendations, and moderation. If all of that complexity is visible at once, the product will feel heavy. The interface must make the platform feel simple even when the system underneath is sophisticated.

The user experience should follow one rule:

> Make the first action obvious, then reveal depth when the user needs it.

A casual viewer should be able to open the app and scroll without thinking. A new creator should be able to post without reading documentation. A project owner should be able to create a project without feeling like they are filling out enterprise software. A serious creator should be able to access analytics and deeper tools when they want them.

The interface should not try to prove that Discovr is different by making basic actions weird. The product should feel familiar where familiarity reduces friction and distinctive where distinction supports the core promise.

The visual direction is clean, white, minimal, rounded, and content-first, with a fully considered dark mode. It should feel closer to the clarity of Instagram, Notion, Linear, and modern Apple-style interfaces than to a loud neon creator app. The product can have personality, but the base interface should feel polished, calm, and premium.

---

# UX principles

## 1. Familiar patterns, Discovr outcomes

Users already understand feeds, profiles, likes, comments, saves, shares, follows, search, and messages. Discovr should use these patterns where they work.

The product should feel different because users discover different people, receive clearer creator feedback, find projects, join communities, and form connections. The interface does not need to reinvent scrolling to prove innovation.

## 2. Discovery should feel intentional, not random

Unknown creators will appear in the feed. That is part of the product. The interface should make this feel like discovery, not noise.

Possible signals:

- Topic labels
- Community context
- “Rising in robotics” style explanations
- “Because you follow drummers” style hints later
- Project tags
- Creator status such as “new creator” or “rising” where appropriate

These explanations should be light. The feed should not become cluttered with algorithm notes.

## 3. Creation should be fast but structured

The create flow should capture enough information to support discovery without making users feel interrogated.

A post needs content, caption, media, and context. The system can infer some context automatically and ask the user to confirm or adjust it.

## 4. Depth should be progressive

Discovr has serious features, but not everyone needs them immediately.

A post card should be simple. Advanced analytics can live deeper.

A profile should be readable at a glance. Portfolio sections can expand.

A project should show title, purpose, roles, and activity first. Detailed milestones and member permissions can live below.

## 5. Safety controls should be visible but not scary

Report, block, hide, and message-request controls should be easy to find. They should not make the product feel hostile by default.

## 6. The product should feel alive

A discovery platform should not feel static. The interface should communicate that posts are being tested, projects are active, communities are growing, and creators are being found.

This can happen through subtle status labels, notification wording, activity modules, and analytics states.

## 7. Minimal does not mean empty

The interface should be minimal in noise, not minimal in usefulness. Important actions must remain visible. Cards should have breathing room. Labels should be clear. Empty states should guide action. Minimalism should make the product easier to use, not harder to understand.

---

# Platform priorities

Discovr should be mobile-first.

Most social consumption happens on phones, and the core feed experience is naturally mobile. The desktop web app still matters, especially for serious creators, project owners, analytics, and content management, but the first impression should be designed for mobile.

## Mobile priorities

- Fast feed loading
- Thumb-friendly navigation
- Low-friction posting
- Clear post cards
- Easy saving and sharing
- Simple profile viewing
- Fast message access
- Project browsing that does not feel like a spreadsheet
- Safe message requests

## Desktop priorities

- Better project management
- Better analytics layouts
- Easier typing and editing
- Better media management
- Multi-column discovery where useful
- Admin and moderation tooling later
- Creator dashboards later

The same product should feel coherent across devices, but not identical. Mobile is for browsing and quick creation. Desktop is better for deeper work.

---

# Visual direction

Discovr should use a clean, white, minimalist visual system with rounded corners, soft borders, restrained shadows, and a polished dark mode.

The base interface should feel calm and premium. It should not look like a noisy gamer dashboard, a crypto landing page, or an over-designed neon app. Content should be the hero. The interface should make posts, profiles, projects, communities, and messages feel easy to scan.

The visual reference point is closer to:

- Instagram’s familiar social clarity
- Notion’s calm surfaces
- Linear’s sharp hierarchy
- Apple’s restraint and spacing
- Modern rounded card interfaces

The product should not copy any of these directly. The goal is to capture the same feeling of clarity: white space, legible typography, rounded surfaces, clean icons, and a sense that every element has a reason to exist.

## Light mode

Light mode is the default visual identity.

Expected qualities:

- White or near-white app background
- Slightly off-white page surfaces where needed
- Dark neutral text
- Subtle gray borders
- Rounded cards
- Soft shadows used sparingly
- Clear iconography
- Accent color used only for meaningful actions
- Minimal gradients, if any

Light mode should not feel sterile. It can use warmth through spacing, rounded corners, subtle elevation, and friendly typography.

## Dark mode

Dark mode should be first-class, not a simple color inversion.

Expected qualities:

- Deep neutral background, not pure black everywhere
- Slightly lighter card surfaces
- Clear separation between cards and background
- High readability
- Reduced harsh contrast where possible
- Accent color adjusted for dark surfaces
- Media still feels dominant
- Borders and dividers remain subtle

Dark mode should feel premium and comfortable for long browsing sessions.

## Rounded corners

Rounded corners are a core part of the interface language.

Cards, buttons, inputs, media containers, modals, chips, message bubbles, project cards, community cards, and profile modules should use consistent radius values.

The product should avoid sharp, harsh rectangles unless there is a strong reason. Rounded surfaces make the interface feel approachable and modern.

## Cards and surfaces

Discovr should use card-based surfaces for:

- Posts
- Project previews
- Community previews
- Creator suggestions
- Analytics summaries
- Message requests
- Notification groups
- Search results

Cards should feel lightweight. They should not have heavy shadows or thick borders. The design should use spacing, background contrast, and subtle borders more than dramatic elevation.

## Accent color

The accent color should be used carefully for:

- Primary buttons
- Active navigation states
- Links or highlighted actions
- Progress/status indicators
- Selected chips

The app should not be flooded with accent color. If everything is highlighted, nothing is highlighted.

---

# Layout and spacing

Spacing should make the product feel calm and easy to scan.

General spacing principles:

- Feed cards should have enough separation to avoid visual fatigue.
- Text blocks should avoid long dense paragraphs inside UI.
- Primary actions should be close to the content they affect.
- Secondary actions should be accessible but not visually dominant.
- Mobile tap targets should be comfortable.
- Desktop layouts can use wider grids, but should not stretch content lines too far.

Whitespace is useful when it improves scanning. It becomes wasteful when it hides important actions or makes the interface feel empty.

---

# Typography

Typography should be simple and highly readable.

The product should use a modern sans-serif font with strong readability across mobile and desktop. Font sizes should support quick scanning in the feed and longer reading in posts, project descriptions, comments, and settings.

Text hierarchy should be clear:

- Page title
- Section title
- Card title
- Body text
- Metadata
- Labels
- Captions
- Helper text

The UI should avoid excessive font weights. Too many weights make the interface look messy.

---

# Home feed UX

The Home feed is the most important screen.

The default feed card should include:

- Creator avatar
- Display name
- Username or secondary identifier
- Follow button where appropriate
- Post media or text
- Caption
- Topic/context labels where useful
- Like
- Comment
- Save
- Share
- More menu
- Link to project or community if attached

The feed should support quick actions without overwhelming the card.

Feed cards should use rounded surfaces and clean spacing. Media should respect the rounded shape where appropriate. Text posts should feel designed, not like raw database entries. Image and video posts should keep content dominant while preserving consistent action placement.

## Post context

Discovr should show context when it helps discovery.

Examples:

- Posted in VEX Robotics
- Project update from Amplify EP
- Rising in Music
- New creator in UI Design
- Looking for collaborators

These labels should help users understand why the post is in the feed.

## Feed controls

Users should have controls such as:

- Not interested
- Show more like this
- Hide this post
- Report
- Block creator
- Save
- Follow

These controls train the system and protect the user experience.

## Feed refresh

The feed should avoid jarring resets. If a user returns to the app, the product can show new content availability without instantly destroying their place.

---

# Discover UX

Discover should feel like a structured exploration page.

It should include a prominent search bar and curated modules.

Possible layout:

1. Search bar
2. Interest chips
3. Rising creators
4. Projects looking for people
5. Communities for you
6. New posts gaining traction
7. Topics grid
8. Local or school-related discovery where appropriate

Discover should be visually different from Home. Home is an endless stream. Discover is a set of doors.

The page should help users steer the algorithm. Users should be able to add, remove, or tune interests from Discover.

Discover cards should use the same rounded minimalist system as the feed while supporting more variety: horizontal creator cards, compact community cards, project cards with roles, and topic tiles.

---

# Create UX

The create flow should be one of the fastest parts of the product.

A basic create flow:

1. Tap Create.
2. Choose post type or default to the most common type.
3. Add text or media.
4. Add caption.
5. Confirm topics or let the system infer them.
6. Attach to a project or community if relevant.
7. Publish.

The system should avoid asking too much before the user has created anything. Optional fields should stay optional.

## Topic confirmation

Topic selection helps discovery. It should feel lightweight.

For example:

“Looks like this is about: Drums, Music, Performance. Edit?”

The user can accept, remove, or add topics.

## Project attachment

If a user belongs to projects, the create flow can ask whether the post is a normal post or project update.

Project updates should feed into both the project page and relevant discovery surfaces.

## Drafts

Drafts should be saved automatically where possible. Losing a post is one of the fastest ways to make users hate a product.

---

# Profile UX

A profile should be readable in seconds.

The top section should answer:

- Who is this?
- What do they create or care about?
- Should I follow them?
- Are they open to connection or collaboration?

Core profile layout:

- Header image or simple banner later
- Avatar
- Display name
- Username
- Bio
- Follow/message buttons
- Collaboration status where enabled
- Interests or skills
- Featured posts/projects
- Content tabs

Possible tabs:

- Posts
- Projects
- Saves if public or private owner view
- Communities
- About

For the profile owner, the page should include shortcuts to analytics, edit profile, drafts, settings, and creator tools.

For visitors, the page should prioritize identity and action.

The profile should stay clean and social. It should not become a cluttered resume. Portfolio depth should be available, but the first view should feel like a modern social profile.

---

# Project UX

Projects must not feel like boring forms.

A project page should feel like a living public workspace.

Top section:

- Banner
- Title
- Short description
- Category
- Owner
- Members
- Follow button
- Apply/join button
- Status such as planning, active, recruiting, paused, launched

Important modules:

- Roles needed
- Recent updates
- Milestones
- Media
- Links
- Members
- Discussion or project chat access
- Related posts

The most important action should be obvious. If the project is recruiting, “Apply” should be prominent. If it is not recruiting, “Follow” should be prominent.

Project creation should begin simple:

1. Project name
2. Description
3. Category
4. Recruiting status
5. Roles needed
6. Banner or media later

More advanced sections can be added after creation.

Project pages should use rounded cards for roles, milestones, updates, and members. They should feel modern and social, not like a database table.

---

# Community UX

Communities should feel active and approachable.

A community page should include:

- Name
- Description
- Member count
- Join button
- Rules
- Moderators
- Feed or discussion list
- Featured posts
- Related projects
- Events later

The first view should help a user decide whether to join.

Community posting should clearly show when a post is going to the community. Users should not accidentally post into a community when they meant to post publicly.

Moderators need basic controls:

- Remove posts
- Pin posts
- Review reports
- Manage rules
- Approve or restrict members later

---

# Messaging UX

Messaging should be fast, safe, and connected to discovery.

Inbox sections:

- Primary messages
- Message requests
- Project conversations
- Group chats later

Message requests are important because open DMs can become spammy. A user should be able to accept, ignore, block, or report a request.

Project applications should create structured messaging contexts. The receiver should see what project the applicant is referring to and what role they applied for.

Messaging should include:

- Text
- Media later
- Links
- Reactions later
- Report
- Block
- Mute

Read receipts and typing indicators should be considered carefully. They can improve conversation but also create pressure. They can be optional or delayed until later.

Message bubbles should follow the rounded visual system. The inbox should stay clean and organized so project conversations, requests, and normal DMs do not collapse into chaos.

---

# Notifications UX

Notifications should be useful, not desperate.

Discovr should avoid manipulative notification language. Notifications should tell users what happened and why it matters.

Good notification examples:

- “Your post completed its first discovery test.”
- “Your project received a new application.”
- “A creator you follow posted an update.”
- “Your post is now reaching a wider audience.”
- “Someone replied to your comment.”

Weak notification examples:

- “You’re missing out!”
- “Everyone is talking about you!”
- “Open now before it disappears!”

The notification center should group related events. A creator with an expanding post should not receive a separate notification for every minor interaction.

---

# Analytics UX

Analytics should be clear enough to build trust.

Creator analytics should show:

- Reach
- Engagement
- Saves
- Shares
- Comments
- Profile visits
- Follows gained
- Initial test status
- Expansion status

The language should be plain.

Instead of only showing numbers, the interface can include short explanations:

“Your post completed its first discovery test. It performed strongly in saves and profile visits, so it is being shown to a wider audience.”

Or:

“Your post completed its first discovery test. Engagement was below the expansion threshold, so it will remain available on your profile and in search.”

The product should not over-explain the algorithm, but it should reduce confusion.

Analytics cards should be simple and rounded. Use clear numbers, short labels, and concise explanations. Avoid dashboard clutter in the basic creator view.

---

# Empty states

Empty states are important in early products.

Examples:

## Empty feed

“You have not followed anyone yet. Choose interests or explore creators to start building your feed.”

## Empty project page

“This project has not posted updates yet.”

## Empty inbox

“No messages yet. When people reply, apply, or collaborate, conversations will appear here.”

## Empty analytics

“Analytics appear after your post receives enough activity.”

Empty states should teach the next action. They should not feel like dead ends.

---

# Loading states

Loading states should make the app feel responsive.

Use skeletons for feeds, profiles, projects, and comments. Avoid blank white screens.

For uploads, progress should be clear. Users should know whether media is uploading, processing, posted, or failed.

For feed refresh, avoid sudden jumps. If new posts are available, the product can show a small prompt instead of moving the user unexpectedly.

---

# Error states

Errors should be specific and recoverable.

Bad error:

“Something went wrong.”

Better error:

“Your video could not upload because the connection dropped. Try again.”

Common error cases:

- Upload failed
- Media too large
- Unsupported file type
- Post removed or unavailable
- Message failed to send
- Project application failed
- Network offline
- Permission denied
- Rate limit reached
- Account restricted

The user should know what happened and what to do next.

---

# Accessibility

Accessibility is product quality.

Requirements:

- Strong contrast
- Readable type sizes
- Keyboard navigation for web
- Focus states
- Screen-reader labels
- Captions for video where possible
- Alt text for images
- Reduced-motion support
- Tap targets large enough for mobile
- Avoid relying only on color to communicate state

Accessibility should not be postponed until the product is mature. Retrofitting accessibility later is harder and usually worse.

---

# Motion and interaction

Motion should make the product feel smooth, not slow.

Good uses of motion:

- Opening post detail
- Saving a post
- Following a creator
- Switching tabs
- Expanding project sections
- Sending messages
- Upload progress
- Toast confirmations

Bad uses of motion:

- Long transitions before content appears
- Excessive bouncing
- Animations that delay posting
- Decorative movement that competes with media
- Motion that cannot be reduced for accessibility

Discovr should use motion to explain state changes.

---

# Tone and microcopy

The writing inside the product should be human and clear.

Avoid corporate filler and fake hype.

Good:

- “Post published.”
- “Your post is being tested with a relevant audience.”
- “This project is looking for a designer.”
- “Message request sent.”
- “You can apply after completing your profile.”

Bad:

- “Unlock the next generation of discovery engagement.”
- “Revolutionize your creator journey.”
- “Oopsie, the internet goblin ate your upload.”

The product can have personality, but important states should stay clear.

---

# Design system direction

The design system should define:

- Colors
- Typography
- Spacing
- Buttons
- Cards
- Inputs
- Modals
- Toasts
- Navigation
- Post cards
- Project cards
- Community cards
- Profile modules
- Message bubbles
- Skeleton loaders
- Empty states
- Error states
- Icons

The system should support light mode and dark mode from the beginning. Light mode should be the primary clean white identity. Dark mode should be equally polished, not a quick inverted theme.

Components should be reusable. A project card, community card, creator card, and post card should share design logic while preserving their distinct purpose.

Core component direction:

- Rounded corners across the system
- Minimal borders
- Subtle shadows only where useful
- Clean white surfaces in light mode
- Deep neutral surfaces in dark mode
- Clear primary actions
- Soft secondary actions
- Consistent spacing scale
- Consistent icon sizing

---

# Interface risks

## Too much explanation

If every feed item includes long algorithm explanations, the product becomes noisy. Context should be light.

## Too much hidden complexity

If deeper tools are buried too far, serious creators will not find them. Progressive disclosure must still make advanced features discoverable.

## Projects feel too formal

If Projects feel like work software, casual users may avoid them. They should feel social and alive.

## Chat becomes chaotic

If message requests and project chats are not separated clearly, the inbox becomes confusing.

## Analytics feel fake

If analytics use vague or inflated language, creators will lose trust.

## Minimalism hides function

A clean UI can accidentally hide important actions. Discovr should avoid mystery-meat icons and overly subtle controls.

---

# Chapter conclusion

Discovr’s interface should make a complex product feel simple.

The app should be familiar enough for users to understand instantly and distinctive enough to support the discovery promise. Home should feel relevant. Discover should feel intentional. Create should feel fast. Profiles should communicate identity. Projects should make collaboration obvious. Communities should create context. Chat should make follow-up safe. Analytics should make distribution understandable.

The visual system should be clean, white, minimal, rounded, and content-first, with a first-class dark mode. The product should feel premium and calm, not loud or gimmicky.

The product should not rely on hype, clutter, or novelty for its identity. The interface should quietly support the deeper system: helping people, posts, projects, and communities get discovered by the right audience.
