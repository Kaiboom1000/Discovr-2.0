# 06 — Feed and Discovery Engine

The feed and discovery engine are the heart of Discovr.

Everything else supports this system. Posts, profiles, projects, communities, topics, analytics, messaging, moderation, and monetization all become more valuable when the platform can reliably introduce the right content to the right people.

Discovr’s core promise depends on this chapter:

> Every eligible post receives a real opportunity to be discovered by a relevant audience.

That promise requires a system, not a vibe. The platform needs rules for eligibility, classification, audience selection, feed inventory, ranking, testing, expansion, analytics, spam prevention, and creator feedback.

The discovery engine should not be framed as mysterious algorithm magic. It should be designed as a measurable product system.

---

# The central problem

Most feeds are good at distributing content that already has evidence.

A creator with followers creates early engagement. A post with early engagement becomes easier to recommend. A creator with a history of successful posts receives more confidence. A trend with known performance becomes safer to distribute.

This is efficient, but it creates cold-start unfairness.

New creators and niche posts often fail before they are properly tested. The platform does not always know who should see the post, so it shows it to too few people or the wrong people. The post produces weak signals, and weak signals reduce future reach.

Discovr should solve this by explicitly separating first opportunity from final reach.

The system should guarantee a meaningful initial test for eligible content, then let measured response determine expansion.

---

# Core discovery model

The discovery engine should operate in stages.

A simplified lifecycle:

1. Post is created.
2. Post passes basic eligibility checks.
3. Post is classified by content, topic, format, language, and safety risk.
4. System selects an initial relevant audience.
5. Post receives a first discovery test.
6. System measures meaningful signals.
7. Post either stops, holds, or expands.
8. Strong posts receive additional distribution waves.
9. Creator receives analytics and status feedback.
10. Post remains discoverable through profile, search, communities, and long-tail recommendation.

This model makes the promise concrete.

A post does not need followers before being tested.

A post does need eligibility and relevance before being distributed.

A post does not receive infinite reach.

A post does receive a real first chance.

---

# Eligibility

Not every post should receive the same initial distribution.

Eligibility protects the platform from spam, abuse, unsafe content, and low-quality manipulation.

Eligibility checks may include:

- Account exists and is active
- Email or account verification where required
- Account is not restricted
- User has not exceeded rate limits
- Media processed successfully
- Content is not already removed
- Content passes basic safety checks
- Content is not obvious duplicate spam
- Links are not obviously malicious
- Post has enough content to classify
- User is not blocked from the target audience

Eligibility is not the same as quality ranking. A post can be eligible and still perform poorly. Eligibility only decides whether the post deserves a real first test.

The platform should avoid using eligibility as a hidden excuse to suppress normal content. If a post is ineligible, creators should receive a clear reason where possible.

---

# Content classification

Before the platform can choose an audience, it must understand the post.

Classification should identify:

- Format: text, image, video, carousel, project update, community post
- Topics: music, robotics, design, coding, photography, comedy, etc.
- Subtopics: drums, VEX IQ, UI design, street photography, indie film, etc.
- Language
- Media type
- Creator intent where inferable
- Project attachment
- Community attachment
- Safety risk
- Spam risk
- Originality or duplication risk later

Classification can use multiple inputs:

- Caption text
- User-selected topics
- System-inferred topics
- Media metadata
- Visual analysis later
- Audio/video analysis later
- Creator history
- Community context
- Project context

User-entered topics are useful, but they should not be trusted blindly. The system should compare tags against actual user response and content signals.

If a creator tags a drum cover as “startup” to chase reach, the audience will likely respond poorly. The system should learn that the tag was weak or manipulative.

---

# Audience selection

A fair test requires a relevant audience.

Random reach is not fair reach. Showing a robotics post to random comedy viewers does not produce useful signal. Showing a niche music post to users who never engage with music does not test the post properly.

The initial audience should be selected from users who have demonstrated interest in related areas.

Audience signals include:

- Onboarding interests
- Followed creators
- Joined communities
- Saved posts
- Watched posts
- Commented posts
- Shared posts
- Search history where appropriate
- Project follows
- Project applications
- Skills and profile interests
- Negative feedback history
- Language preference
- Location where appropriate

The audience should be large enough to produce useful signal but small enough to protect feed quality.

The exact size should be configurable and tested.

A possible early model:

- Small test: 25-100 impressions
- Medium test: 100-500 impressions
- Strong expansion: 500-5,000 impressions
- Larger expansion: based on performance and audience size

These numbers are placeholders, not final rules. The important idea is staged testing.

---

# Feed inventory

The feed has limited space.

Every feed impression used for a new post is an impression not used for followed content, proven content, ads, project updates, or community posts. The feed engine must reserve discovery inventory intentionally.

Possible feed inventory categories:

- Followed content
- Recommended proven content
- New discovery tests
- Project updates
- Community content
- Search/trend influenced content
- Sponsored content later

A healthy feed might allocate a percentage of impressions to discovery tests.

Example:

- 40% personalized recommended content
- 25% followed/community content
- 20% discovery test content
- 10% project/community modules
- 5% experiments or sponsored content later

These are not final numbers. The allocation should change based on user behavior, feed maturity, and product goals.

If discovery inventory is too low, Discovr becomes a normal platform.

If discovery inventory is too high, feed quality may drop.

---

# Ranking signals

The feed should rank content using multiple signals.

Positive signals:

- Watch time
- Read time
- Completion rate
- Rewatch or reread behavior
- Likes
- Saves
- Shares
- Comments
- Meaningful replies
- Profile visits
- Follows after impression
- Project follows
- Project applications
- Community joins
- Search clicks
- Return visits

Negative signals:

- Fast skips
- Hides
- Not interested actions
- Reports
- Blocks
- Low completion
- Repeated ignores
- Comment toxicity
- Spam indicators
- Duplicate content indicators

Context signals:

- User interests
- Time since posting
- Topic match
- Creator trust
- Account age
- Relationship to creator
- Community membership
- Project relationship
- Language
- Location where appropriate
- Device/network constraints for media-heavy posts

Ranking should not use one metric blindly. A post with many comments may be valuable or controversial. A post with many likes may be shallow. A post with fewer likes but high saves and profile visits may be strong.

Discovr should treat meaningful follow-through as especially important.

---

# Meaningful discovery signals

Discovr should distinguish attention from discovery.

Attention means the user saw or reacted to something.

Discovery means the user found something worth acting on or remembering.

Strong discovery signals include:

- Save after viewing
- Follow after viewing
- Profile visit after viewing
- Message request after viewing
- Project application after viewing
- Community join after viewing
- Share after viewing
- Return to creator later
- Explore related posts

These signals should carry more weight than raw impressions.

A post that generates 200 impressions and 20 saves may be more valuable than a post that generates 2,000 impressions and 5 likes.

The system should be designed to notice that difference.

---

# Expansion waves

Posts should expand in waves.

Wave-based distribution allows the platform to test, measure, and scale reach without dumping unproven content into the entire feed.

Possible stages:

## Stage 0 — Created

The post exists but has not been distributed.

## Stage 1 — Eligibility and classification

The system checks whether the post is safe and classifiable.

## Stage 2 — Initial audience test

The post is shown to a small relevant audience.

## Stage 3 — Signal evaluation

The system measures response quality.

## Stage 4 — Second wave

If signals are strong, the post expands to a larger related audience.

## Stage 5 — Adjacent audience testing

If the post has broader potential, it is tested with adjacent interests.

## Stage 6 — Broad recommendation

High-performing posts can enter broader recommendation pools.

## Stage 7 — Long-tail discovery

The post remains discoverable through search, profile, communities, and future recommendations.

Not every post needs every stage.

Niche posts may perform well within a narrow audience and not need broad expansion. That should not be considered failure.

---

# Creator feedback

The discovery engine must communicate enough to build trust.

Creators should be able to see:

- Whether the post was eligible
- Whether the post received an initial test
- Approximate initial reach
- Strong signals
- Weak signals
- Expansion status
- Long-tail status

Possible status language:

- “Your post is being prepared for discovery.”
- “Your post is being tested with a relevant audience.”
- “Your post completed its first discovery test.”
- “Your post is expanding to a wider audience.”
- “Your post performed best with music and live performance audiences.”
- “Your post did not expand further, but it remains available on your profile and in search.”

The product should not expose exact ranking formulas. Too much transparency creates gaming. But the creator should understand the process.

Silence is the enemy. A creator should not be left wondering whether the post failed or was never tested.

---

# Cold-start creators

Cold-start creators are the users Discovr most needs to help.

A creator with no followers should still be able to receive a relevant first audience.

The system can use:

- Post content
- Topics
- Onboarding interests
- Profile interests
- Early account behavior
- Community selection
- Project attachment
- Similar content patterns

The creator’s lack of history should reduce confidence, not eliminate opportunity.

New creators may receive smaller initial tests until trust grows, but the test should still be real.

This is the difference between caution and invisibility.

---

# Feed quality protection

The discovery promise cannot destroy the viewer experience.

Viewers are not test subjects for irrelevant content. If the feed becomes noisy, the product fails.

Protection mechanisms:

- Relevance filtering
- Small initial test sizes
- Negative feedback controls
- Spam scoring
- Account trust scoring
- Topic confidence scoring
- Distribution caps
- Quality thresholds
- Duplicate detection
- Report-triggered pauses

The feed should be generous to creators but respectful of viewers.

A good system creates opportunity without making users feel like they are doing unpaid moderation work.

---

# Spam and abuse prevention

Guaranteed initial reach creates incentives for abuse.

Bad actors may try to create many accounts, upload duplicate content, tag unrelated topics, use clickbait, send spam links, manipulate engagement, or exploit message requests.

Anti-abuse signals:

- New account velocity
- Posting frequency
- Duplicate media
- Duplicate captions
- Link patterns
- Report rate
- Block rate
- Follow/unfollow patterns
- Engagement from suspicious accounts
- Topic mismatch
- Device/IP risk where appropriate
- Message request volume

The system should not permanently punish users for one weak signal, but repeated abuse patterns should reduce distribution.

Spam prevention is not separate from the discovery engine. It protects the promise from being exploited.

---

# Projects in discovery

Projects should be discoverable objects, not just profile attachments.

A project can appear in:

- Discover modules
- Feed cards
- Search results
- Profile sections
- Community pages
- Suggested collaboration modules

Project ranking signals include:

- Project follows
- Applications
- Update engagement
- Role relevance
- Member credibility
- Community relevance
- Completion of project profile
- Recent activity
- Report rate

A project looking for a drummer should be shown to people with music, drums, band, live performance, and collaboration signals.

A robotics project looking for programmers should be shown to users with robotics, coding, engineering, or VEX interests.

Project discovery is one of the clearest ways Discovr can turn attention into action.

---

# Communities in discovery

Communities create context and retention.

Community ranking signals include:

- Member growth
- Active members
- Post quality
- Report rate
- Topic match
- Moderator activity
- Project connections
- User interest overlap

Communities should be recommended to users who are likely to participate, not only lurk.

A community with fewer members but strong relevance may be better for a user than a massive generic community.

This follows the same philosophy as posts: existing size should not be the only path to visibility.

---

# Personalization

Personalization should improve relevance without trapping users in narrow bubbles.

The system should learn from:

- Explicit interests
- Follows
- Saves
- Shares
- Comments
- Watch/read time
- Searches
- Communities
- Projects
- Negative feedback

But it should also include exploration.

Users should sometimes see adjacent topics, rising creators, new projects, and fresh communities. Discovery requires some controlled surprise.

The system should avoid extreme repetition. If a user engages with one drum post, the feed should not become only drums forever.

---

# Metrics

The discovery engine should be evaluated using mission-specific metrics.

Important metrics:

- Eligible posts tested
- Median first-test reach
- Time to first test
- Expansion rate
- Save rate during first test
- Follow rate after discovery impression
- Project application rate
- Community join rate
- Hide/report rate
- New creator return rate
- Feed retention
- Viewer satisfaction
- Creator trust score

Standard metrics like DAU, MAU, session length, and engagement still matter, but they are not enough.

If session length rises while creator trust collapses, the system is failing the mission.

---

# Chapter conclusion

The feed and discovery engine define Discovr more than any single screen.

The product promise depends on building a system where eligible posts are classified, matched with relevant first audiences, tested in controlled waves, evaluated through meaningful signals, and expanded when they earn it.

The system must protect both sides of the marketplace: creators need opportunity, and viewers need relevance.

A discovery engine that is too conservative becomes a normal feed.

A discovery engine that is too generous becomes spam.

The correct system sits between those extremes: intentional, measurable, transparent enough to trust, and strict enough to protect quality.
