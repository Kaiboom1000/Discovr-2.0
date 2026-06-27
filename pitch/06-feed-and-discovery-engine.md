# 06 — Feed and Discovery Engine

The feed and discovery engine are the core systems of Discovr.

The product promise depends on this system being real, measurable, and trustworthy. Discovr should not describe discovery as vague algorithmic magic. The platform needs defined rules for eligibility, classification, audience selection, feed inventory, ranking, staged testing, expansion, analytics, quality controls, and creator feedback.

This chapter defines the first version of that system in formal product and engineering terms. It avoids founder-specific examples and should be treated as the foundation for later ranking, data, and infrastructure specifications.

---

# Core promise

Every eligible post should receive a meaningful opportunity to be discovered by a relevant audience.

This does not mean every post receives equal distribution. It does not mean every post receives broad reach. It means the system creates a first test before final reach is determined.

The platform should separate first opportunity from final reach. First opportunity is the initial test. Final reach is the result of performance, relevance, viewer response, and system confidence.

This distinction protects creators and viewers at the same time.

---

# Discovery lifecycle

A post should move through a defined lifecycle.

The content is created. The system verifies basic eligibility. The content is classified by format, topic, language, project or community context, and quality indicators. The system selects a relevant initial audience. The post receives a controlled first test. The system evaluates response quality. The post either stops expanding, remains in a narrow audience, or expands into additional distribution waves. The creator receives understandable feedback. The post remains available through profile, search, communities, projects, and long-tail recommendation where appropriate.

This lifecycle makes discovery operational. It prevents the platform from claiming fairness without defining how fairness is produced.

---

# Eligibility

Eligibility determines whether content enters the first-test system.

Eligibility is not the same as quality. A post can be eligible and still perform poorly. Eligibility only confirms that the post can receive an initial test.

Eligibility checks should include account state, upload validity, content availability, processing state, rate limits, duplicate patterns, link risk, and whether the post contains enough information to classify.

If content is not eligible, the user should receive a clear reason where possible.

---

# Classification

Audience selection requires understanding the content.

Classification should identify format, topics, language, media type, project context, community context, creator history, and quality indicators. It can use captions, user-selected topics, inferred topics, media metadata, profile context, community context, and project context.

User-entered metadata should help the system but should not be trusted blindly. If declared topics repeatedly fail to match audience response, confidence in that metadata should decline.

Classification should improve over time, but the first version should remain explainable.

---

# Audience selection

A fair first test requires a relevant audience.

Random exposure is not fair exposure. It creates poor viewer experience and misleading creator feedback. The initial audience should be selected from users with demonstrated or declared interest in related categories.

Relevant signals may include onboarding interests, follows, saves, shares, comments, viewing behavior, search behavior, community membership, project participation, profile interests, language preference, location where appropriate, and negative preference signals.

The audience should be large enough to produce useful data and small enough to protect feed quality. Exact numbers should be configurable and tested.

---

# Feed inventory

The feed has limited space.

Every impression assigned to a discovery test is an impression not assigned to followed content, proven recommendations, community content, project updates, or sponsored content. Feed inventory must therefore be allocated deliberately.

The feed should contain a controlled mix of followed content, personalized recommendations, first-test content, project updates, community content, and later sponsored content. The exact proportions should be configurable.

If first-test inventory is too low, Discovr becomes a standard feed. If first-test inventory is too high, viewer relevance may decline.

---

# Ranking signals

Ranking should use multiple signal types.

Positive signals include saves, shares, comments, profile visits, follows after exposure, project applications, community joins, completion behavior, return visits, and repeated interest.

Negative signals include fast skips, hides, disinterest actions, low completion, repeated ignores, and quality indicators.

Context signals include topic match, user interest, account history, creator trust, relationship to creator, community membership, project relationship, language, freshness, media type, and device or network constraints where relevant.

No single metric should dominate the system.

---

# Meaningful discovery

Discovr should distinguish attention from discovery.

Attention means a user saw or reacted to something. Discovery means the user found something worth acting on or remembering.

Strong discovery signals include saving, sharing, following after exposure, visiting a profile, joining a community, applying to a project, starting an approved conversation, returning to related content, or searching for related topics later.

These signals should matter because they indicate durable value. The platform should avoid treating raw impressions as the main measure of success.

---

# Expansion waves

Distribution should happen in stages.

A basic wave model includes creation, eligibility, classification, first test, signal evaluation, second wave, adjacent audience test, broader recommendation, and long-tail discovery.

The first test validates audience fit. The second wave validates whether the signal remains strong at a larger scale. Adjacent audience tests determine whether the post can travel beyond its initial category. Broad recommendation should be reserved for content with strong evidence. Long-tail discovery keeps useful content available through search, profiles, projects, communities, and future recommendation.

Not every post should become broad. A narrow post that performs well within a narrow audience can still be successful.

---

# Creator feedback

Creator feedback is part of the discovery engine.

The system should show whether content was eligible, whether a first test occurred, approximate reach, strong signal categories, weak signal categories, expansion state, and long-tail availability.

The product should not expose exact ranking formulas. The correct approach is principled transparency: enough information to build trust, not enough detail to compromise the system.

The creator should understand the difference between a post that failed after a test and a post that was not eligible for testing.

---

# Cold-start handling

Cold-start users should receive opportunity with appropriate caution.

A new account has less trust history, but lack of history should not mean lack of opportunity. The system can use content classification, declared interests, profile context, community context, project context, and early account behavior to form an initial test.

New accounts may receive smaller tests, stricter rate limits, and more conservative expansion thresholds until trust grows. That is different from making them invisible.

The system should protect feed quality while still allowing new creators to generate evidence.

---

# Project and community discovery

Projects should be discoverable objects. A project can appear in Discover, search, feed modules, profile sections, community pages, and suggested participation surfaces. Project ranking should consider topic relevance, role relevance, project completeness, update activity, application activity, member trust, community context, and user interest.

Communities should be recommended based on relevance and activity, not only size. Community ranking should consider topic match, active participation, member growth, post quality, moderator activity, project connections, and user interest overlap.

Existing scale should matter, but it should not be the only path to visibility.

---

# Personalization and exploration

Personalization should improve relevance without trapping users into repetitive loops.

The system should learn from explicit interests, follows, saves, shares, comments, search, communities, projects, negative preferences, and return behavior. It should also include controlled exploration so users encounter adjacent topics, new creators, rising projects, and relevant communities outside their immediate history.

The feed should avoid becoming too narrow. Discovery requires some surprise, but surprise must be controlled by relevance.

---

# Measurement

The discovery engine should be measured through mission-specific metrics.

Important metrics include eligible posts tested, time to first test, median first-test reach, expansion rate, save rate during first test, follow rate after discovery exposure, project application rate, community join rate, negative feedback rate, new creator return rate, viewer retention, and creator trust.

General growth metrics still matter, but they are not enough. If session length improves while creator trust declines, the product is drifting away from its mission.

---

# Chapter conclusion

The feed and discovery engine define Discovr more than any single screen.

The system must give eligible content a relevant first test, measure meaningful response, expand in stages, protect feed quality, provide creator feedback, and support discovery for projects and communities.

A system that is too conservative becomes a standard feed. A system that is too broad becomes noisy. Discovr must operate between those extremes with discipline, measurement, and trust.
