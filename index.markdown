---
layout: home
title: ''
---

## Background
[background]: #background

An open software project — that is, a software project conducted in the open, without attaching it
to either of the two dominant ideologies, “free software” and “open source” — might be started for
many reasons, but the most basic of these is that someone, a developer or designer or someone with
another skillset entirely but willing to experiment and muddle their way through… had an idea, and
brought it into the world, and was willing and able to share it. To open it up.

A vast majority of open software works thereafter see no use beyond their creator’s. A small
portion see some occasional use, and an even smaller percentage see more than that. That last
category has a tendency to grow. People will find the project, and some will use it. Through social
propagation, be that word of mouth, github stars, blog posts, bone fide social media, or stumbling
upon it via a google search, more and more people find and use it. And eventually, it happens:

Contribution.

That comes in many forms. I want to distinguish four families: reporting, helping, submitting,
and supporting.

- **Reporting** is filing bugs. Asking questions. Requesting features. Giving feedback. It is
	conceptually one step above _using_ the work, though in practical terms one may be asking
	questions before really using the software, or in order to, and one may be filing issues only
	after having given up on making it work by oneself.

- **Helping** only really starts occuring naturally after some growth: initially, it’s people
	familiar with the project answering questions, giving tips, writing blogs, doing some light
	triage. Then, it might graduate into something more involved, or more formal. In large projects,
	each of triage, answering questions, organising work, and administering the project… can be a
	full-time occupation.

- **Submitting** is generally what is meant by “contributing.” However, I argue that all four forms
	described are _work_, and therefore all are contributions. Submitting often involves code: a
	pull-request fixing a bug, implementing a feature, improving the software. But it may also touch
	a wide variety of other aspects: writing documentation, making art, proposing new designs and
	arguing for, against, or alongside existing ones. Reviewing other submissions.

- **Supporting** is indirect contribution, not directly to the project, but to the people behind the
	project. Monetary contributions to maintainers, employers letting staff work on open-source,
	partners taking care of children and housework while one's working, family, friends, and close
	colleagues providing companionship, wisdom, and safety.

In small to medium open software projects, the traditional way work is organised is stratified
between three main roles: Maintainers or Owners, Contributors, and Everyone Else.

I want to emphasise that there are no codified rules, no formal document laying out the “traditional”
way open projects function. What I describe as such is informal etiquette and culture, and by very
nature, is subjective to how I see and have experienced it. That said, _some_ of that way _is_
codified, through the tools we use: GitHub and GitLab both more or less tacitly encode many aspects,
as two prominent examples.

With this caveat out of the way, in the traditional way:

- **Owners** or **Maintainers** drive the project. They are responsible for the project itself,
	for making releases, for keeping the code up to standard, for fixing urgent bugs, for
	administering, for keeping to semver, for answering most questions, doing triage, reviewing
	contributions, merging them, cleaning up behind them as needed, all while also developing the
	software: new features, improvements, the fun stuff, the not so fun.

- **Contributors** submit work. Sometimes, but that is pretty rare, some contributors do take on
	triage, helping, etc. without becoming maintainers themselves. Most of the time, contributors
	_pass by_: they make one or two changes, submit their work, stick around just long enough to
	see it merged, and move on.

- **Everyone else** is the users, the visitors, the invisible mass that’s only really a statistic
	on a traffic chart, or the "stargazers" in GitHub parlance. It’s also most of the reporters,
	and some of the feature-requesters. This is by far the largest group.

The balance of responsibility and effort is heavily skewed up, onto maintainers. In a way, this is
organic: projects grow from one idea by one person (or a handful of people), and at that point they
_do_ do everything. But when others start using and then contributing to the project, all the
overhead also gets added on to that one person.

At the same time, the responsibility grows, as more people use the software. There can be a real
feeling of _duty_ that builds. As the creator and now maintainer of the work, you become responsible
if or when it breaks. It is very easy for boundaries to blur: users of your software become “your”
users, and it can feel like mistakes are a personal failing. As the user base grows, so do their
expectations, especially as they start using your work in their production environments. Having that
happen is not awful: indeed, it’s a great feeling, of pride, of achievement. But the pressure mounts.

It is completely unsurprising that people burn out. That they have meltdowns. That they feel
overwhelmed by what seems like simple, enthusiastic feedback. That some quit open work, or even tech
or the internet entirely.

**The Caretaker Model** is a limited re-organisation of responsibilities and expectations in an open
software project, specifically imagined to reduce burnout of maintainers as well as frustration of
contributors and users.


## Introduction
[introduction]: #introduction

The model is built around the concept of _releases_.

This comes from what the motivation of each external person interested in the work boils down to:

- Users want the software to be usable and have the features they want.
- Reporters want the features they ask for implemented, the bugs they file fixed, etc.
- Submitters want to have their work merged and used (and useful).

The way the software is consumed is via releases. In between releases, the software may be unstable
or incomplete. This is true regardless of the development methodology: even if you have a policy
that "the main branch always builds", what that means is that commits on that main branch may be
releases, albeit informally so. And even if the build passes, other aspects may not be ready.

Internally to the project, there is a lot of work left beyond contributions to get to a releasable
state. Tidying up, checking work, updating documentation, packaging, recording changes, and more.
As seen above, in the traditional way this work is mostly done by maintainers.

In Caretaker, **release work is done by “releasers”**.

A **releaser** is a _transient_ role, which only exists for the purpose and for the duration of
preparing, making, and publishing _one_ release.

The role of releaser can be assumed freely by a “more permanent” member of the project, or can be
assigned, after a proposal, and for a single release, to an external contributor, who then becomes a
**_temporary_ releaser**.

The releaser then _owns_ the release process, and drives it to completion. The project will define a
particular process and have its requirements, but in general this may involve any, all, or more of:

- Picking which features or fixes go in the release
- Reviewing and merging submissions to that effect
- Wholesale coding up features, fixes, improvements
- Writing glue or polish code to make things coherent
- Running lints and cleaning up style, fixing CI failures
- Updating documentation as needed
- Building and packaging, if not automated
- Recording and editing the changelog
- Publishing and announcing the release

Once all that work is done, and the release is out in the world, the releaser's role is over, and
the project returns to a dormant or idle state, awaiting the next releaser to step up, if and when
needed.

The “more permanent” members who can assign releasership mentioned above are **caretakers**.

Caretaking responsibilities are to:

- Provide feedback on release proposals as needed.
- Approve or deny these proposals when ready, and assign release rights in consequence.
- Keep an eye on temporary releasers while they have those rights, and intervene if needed.

That’s it.

Of course, people who are caretakers may also do many other things, or indeed all other things.
Coding, documenting, fixing bugs, answering queries, arbitrating disputes, making decisions, triage,
promotion, making art, investigating bugs, thinking about design… being a caretaker is a _role_,
not an identity.

But the _core, mandatory responsibilities_ of the caretaker role are those three things, and only
those. As long as a caretaker fulfills those three duties, the project can survive, develop, evolve,
grow. Thus, a caretaker's mandatory duties are kept light, such that even someone who has very
little time can achieve them.

The rest of this document delves deeper into how release proposals work, the lifecycle of a release
from the perspective of the model, the duties and expectations placed upon both caretakers and
releasers, how to become a caretaker, discussions about audience (who should _not_ use the model),
scope (what the model _doesn't_ cover), scaling up, normal and failure scenarios, and automation.

--------------------------------------------------


## Scope
[scope]: #scope

The Caretaker model's scope only extends to codifying two new roles in the management of an open
software project, and the processes these two roles support and require. It is intentionally limited
thus, to allow for the wide variety of project strategies and cultures that exist to use the model
without compromising on their existing practices beyond what is needed for the model to work.

The model can be applied fully, such that all release work is done along the caretaker-releaser
interaction, or it can be applied partially, with maintainers exempt, or conditionally, as in the
caretaker role only being useful when maintainers are not active on the project. All of these are
valid uses, and the model attempts to be generic enough to support them.

To avoid any confusion (not an exhaustive list):

- It is not an all-encompassing developer management methodology like Agile or Shape Up.
- It is not about issue management or triage.
- It is not about community management; it certainly does not replace the need for codes of conduct.
- It is not about funding, remuneration, or the pursuit of sustainability in a financial regard.
- It does not concern itself with copyright, licensing, patents, or other such legal concerns.
- It is not itself a tool or product.

Additionally, anything written in this document can be overriden, added on to, or discarded by a
project's own rules. (If sufficient differences occur, it is encouraged that the project instead
codifies their own model and doesn't use the “Caretaker” name, to avoid confusion. See also the
[meta] section.)

## Audience
[audience]: #audience

From the onset, the Caretaker model positions itself as being for "small to medium" projects.

There is no defined upper bound on "how large" a project can be before it stops being appropriate to
use the model: besides the difficulty of measuring "largeness" of a project in discrete terms, the
decision to leave Caretaker behind or adapt it for large-scale use must be made by the project
itself, for its own well-being, and to achieve its own goals.

There is however a lower bound, which is "one": a project _must_ have at least _one_ **caretaker**
who responds to requests for the model to work. If the project is abandoned, or if none of the
established caretakers respond to and act on requests (within reasonable time), then the model by
definition cannot work.

Beyond size, there are other reasons why the model may be unsuitable for a project:

- If a large degree of control over the project, its direction, implementation, copyright and legal
	status, or some other such is required. Caretaker requires trusting potentially any random
	stranger to _release live software to the world_. If that is antithetical to your project or
	philosophies there's no adaptation that will make it work: do no use it.

- If the project is security-critical, or used by a large amount of people, devices, companies...
	then, for the same reasons of trust, the model is inappropriate and should not be used.

- If the project is backed by or directly developed by a company, the model is likely untenable.

There may be other reasons not stated here: the model makes no claim of universality. Use it if, and
only as long as, it fits.


## The caretaker role
[caretaker role]: #the-caretaker-role

At the core of the Caretaker model is the eponymous **caretaker** _role_.

The role's sole responsibility is to facilitate the model's release process. In practice, caretakers
will likely also be maintainers, leaders, triagers, or any of the various other roles that projects
have, but critically, _they don't have to_ for the project to function.

The point of the Caretaker model is to enable a way for the project to function when maintainers are
mostly away. There is little need for external contributors to go through a release proposal and the
entire process when the project's maintainer or team is active enough to pick up features and cut
releases on their own (though the model _can_ be used then too, as a formal process). But when
they're busy elsewhere, be that on other projects, life, or hard at work on tougher features such
that they let the release-making fall by the wayside, the Caretaker model offers a low-cost (to the
maintainers) way for the project to keep evolving.

Additionally, if a user wants a feature _right now_ or a fix to be backported to an old version but
the team doesn't have the time for that, the model allows for the user to get involved directly to
achieve their goal.

A caretaker acts as a guide for prospective releasers submitting a proposal, a gatekeeper in only
allowing proposals that correspond to the project's goals, as well as keeping out known bad actors,
and an observer-slash-monitor for activity by releasers to catch and mitigate malicious activity.

A caretaker still needs to be available to answer queries and proposals within reasonable time, as
defined either by the project or by the default timings in the [release proposals] section. This is
to maintain clear expectations and thus reduce everyone's frustration.

The caretaker role is a good choice when looking for backup or additional maintainers: instead of
taking on a large role upfront, people can take on the much smaller role of being a caretaker, and
ease into other roles, while still always providing the assurance of someone else being there for
the project in case you turn away from active duty on the project for whatever reason.

It's important that people _consent_ to becoming caretakers, though, and it _should not_ be made a
compulsory step in becoming a titled contributor or maintainer. Besides that this scales poorly,
the requirements of being a caretaker may be taxing for some people, or in some situations. This
is open software and open development: most likely, you're all doing this for free. Let roles be
voluntary, especially this one.

Detail on the actual duties of the role are in the [release proposals] and [release lifecycle]
sections, alongside the corresponding responsibilities by releasers.

Becoming a caretaker is a process left to the discretion of the project. A [template](/becoming-a-caretaker)
for prospective caretakers is provided on this site, and if that works for the project no further
action is required beyond considering these requests. Otherwise, add a section to your contributing
guide (the website's action header as well as the template itself do instruct people to look there
as a first step).


## The releaser role
[releaser role]: #the-releaser-role

While the caretaker role is the core of the model, **releasers** do the bulk of the work (in regard
to what the model deals with).

Releasers... _release_. But before they get to the releasing, they also have to become a releaser.

The **releaser _role_** is special in that it is _transient_: it only exists for the purpose of
releasing a single release. When that one release is done, the role dismisses itself.

The other way in which it is special is _who_ can wear the role. Most roles get assigned to or taken
by members of the project. The releaser role can be like that, but it also can be obtained by a
non-member, someone just passing through, an "external contributor," via a formal process.

The project temporarily gains a temporary member, there to do one thing and one thing only, until
that one thing is done, at which time they automatically leave the project again. Even while they're
acting a releaser, they're not responsible for, not expected to do, and indeed expected _not to do_,
any other task or role covered by the rest of the project's members.

This process is based in affording trust to fellow developers. There is one obvious security hole
here: that someone malicious becomes releaser, adds malicious code, and pushes it out. The Caretaker
model is a _bet_ that our trust is warranted and that this failure scenario will not happen _enough_
to warrant not giving strangers that trust in the first place.

This is not a radical step: most projects routinely grant prolific or even just willing contributors
more rights (fancy "member" hats, commit bits, release permissions), so a dedicated person can quite
easily obtain rights on many projects simply by being helpful, and then turn around and wreak havoc.
It happens. It just does not happen _enough_ to put everyone off.

The Caretaker model formalises that process (to establish expectations and reduce frustration) and
limits it to a very specific interaction with a clear, well-defined goal (to encourage participation)
which has an evident and effective result benefitting both the releaser and the project (to make it
appealing for everyone).

To become a releaser under the Caretaker model, a person needs to file a [release proposal], which
is described in the next section. Then, the project's **caretakers**, after reviewing and discussing
and possibly asking for more or pushing back on the proposal, either deny or **approve** it, after
which the person becomes a **releaser**, tasked with accomplishing what their proposal was about.
They're given all the rights necessary for them to achieve that. When they're done, they relinquish
those rights and walk away.


## Release proposals
[release proposals]: #release-proposals
[release proposal]: #release-proposals

A release proposal is a document put forward by someone who, by doing so, applies to the project to
become a temporary releaser. It has several sections:

1. The scope of the release.

   This is the _exhaustive_ list of everything that will make it in the release. This may be as
   simple as mentioning a single pull request, or as complex as putting forward an implementation
   plan for an as-of-yet hypothetical feature. It is not limited to one item: merging all pending
   pull requests is expected to be the most common proposal.

   It is required that the proposal be _exhaustive_. A releaser _must not_ do more than what was
   agreed on without the explicit, written, clearly amended onto the original proposal, approval of
   a caretaker. A releaser _may_ do less than what the proposal stated, but that must also be
   clearly indicated, to avoid assumptions being made and be clear about what remains to be done.

2. The proposed version number of the release.

3. The reasoning behind that version number.

   This can be one sentence, such as "PR #123 is a new feature and contains no breaking changes."

   This section serves to ensure both the applicant and the caretakers are on the same page, to
   avoid assumptions or misunderstandings, and as an insight in the applicant’s thought process,
   which might provide the opportunity for correction.

   For example, a project may have deliberately excluded one part of its API from semver
   consideration, and so when a release application for a pull request touching on that part comes
   in with only a version bumping the major number, it could be rejected or commented against on
   that basis. Yet the applicant may have considered this: "while {API} is not under semver, the PR
   also makes a behaviour change to {other part of the project}, so the major needs breaking."

   Reasoning about this also helps formulate the idea and goals of the release, and to work through
   its contents. It is very well to say "I will merge #12 and #34" but adding "therefore a minor
   version bump is required, as #12 is a feature and #34 a minor bugfix" requires having reviewed
   and understood the implications of the merges.

4. The timeline the applicant expects.

   This is important to set expectations on both sides, and may include any or all of:

   - How long the release work is expected to take. Both so other work can be organised, and so the
	 process can be reasonably cancelled if the releaser vanishes for a longer period of time.

   - How long the applicant will wait for a reply or approval, or after how much time they may
	 consider their proposal stale and the project likely abandoned.

   - Days on and off. For example, that the applicant will only work on this on Saturdays, or that
	 they will be completely unavailable for two weeks starting three days from now (actual dates
	 are recommended).

   None of these are required, and the section may be skipped entirely. In the absence of specified
   timings, defaults from the project or from the model (in this order) will be assumed to apply.

5. Any agreements or statements needed to contribute work on the project, such as agreeing to
   license work, relinquish or retain rights, etc, as required.

Proposals should fit whatever template the project provides, if any, but otherwise there is no
expectation on form nor style except that it must be comprehensible.

Here is a casual sample release proposal for a fictitious project:

```
## Release proposal: 4.3.17

Hi! I really need #123 to be released for my project [rotten
elephants], and I have time this week (13 to 17 July) or the
next (20 to 25 July) to get that done. The new version
number would be 4.3.17 as #123 is only a bugfix.
```

Here is the same release proposal, but a little more impersonal:

```
## Release proposal: 4.3.17

- Scope: merge #123.
- New version number: 4.3.17
- Reasoning for the version: #123 fixes a bug, adds no new
  functionality, contains no breaking change besides the
  fixing of the bug.
- Timeline: available until 25 July, weekdays only.
```


[release lifecycle]: #release-lifecycle
[walkthrough]: #walkthrough
[automation]: #automation
[failure and recovery]: #failure-and-recovery
[scaling up]: #scaling-up
[meta]: #meta
