---
layout: home
---

## Background

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

**The Caretaker Model** is a re-organisation of the responsibilities and expectations in an open
software project, specifically imagined to reduce burnout of maintainers as well as frustration of
contributors and users.


## Introduction

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

In Caretaker, **release work is done by release managers**.

A **release manager** is a _transient_ role, which only exists for the purpose and for the duration
of preparing, making, and publishing _one_ release.

The role of release manager can be assumed freely by a permanent member of the project, or can be
assigned, after request, and for a single release, to an external contributor, who then becomes a
**temporary release manager**.

The release manager then _owns_ the release process, and drives it to completion. The project may
define a particular process, but in general this may involve:

- Picking which features or fixes go in the release
- Reviewing and merging submissions to that effect
- Wholesale coding up features, fixes, improvements
- Writing glue or polish code to make things coherent
- Running lints and cleaning up style, fixing CI failures
- Updating documentation as needed
- Building and packaging, if not automated
- Recording and editing the changelog
- Publishing and announcing the release

Once all that work is done, and the release is out in the world, the release manager's role is over,
and the project returns to a dormant or idle state, awaiting the next release manager to step up,
if and when needed.

The permanent members of the project mentioned above are **Caretakers**.

Caretaking responsibilities are:

- Guiding the project
- Arbitrating (disputes, decisions, etc)
- Answering and processing release and caretaking requests

That’s it.

Of course, people who are Caretakers may also do many other things, or indeed all other things.
Coding, documenting, fixing bugs, answering queries, triage, promotion, making art, investigating
bugs, thinking about design, making releases, all that.

But the _core, mandatory responsibilities_ of a Caretaker are those three things, and only those.
As long as a Caretaker fulfills those three duties, the project can survive, develop, evolve, grow.
Thus, a Caretaker's mandatory duties are kept light, such that even someone who has very little time
can achieve them.

The rest of this document delves deeper into how exactly the temporary release manager process goes,
what the caretaking request process is, discussions about audience (who should _not_ use the model),
scope (what the model _doesn't_ cover), normal and failure scenarios, and automation.

--------------------------------------------------


## Scope

The Caretaker model's scope only extends to codifying two new roles in the management of an open
software project, and the processes these two roles support and require. It is intentionally limited
thus, to allow for the wide variety of project strategies and cultures that exist to use the model
without compromising on their existing practices beyond what is needed for the model to work.

To avoid any confusion (not an exhaustive list):

- It is not an all-encompassing management and development methodology like Agile or Shape Up.
- It is not about issue management or triage.
- It is not about community management: it certainly does not replace the need for codes of conduct.
- It is not about funding, remuneration, or the pursuit of sustainability in a financial regard.
- It does not concern itself with copyright, licensing, patents, or other such legal concerns.


## Audience

From the onset, the Caretaker model positions itself as being for "small to medium" projects.

There is no defined upper bound on "how large" a project can be before it stops being appropriate to
use the model: besides the difficulty of measuring "largeness" of a project in specific terms, the
decision to leave Caretaker behind or adapt it for large-scale use must be made by the project
itself, for its own well-being, and to achieve its own goals.

There is however a lower bound, which is "one": a project _must_ have at least _one_ **caretaker**
who responds to requests for the model to work. If the project is abandoned, or if none of the
established caretakers respond to and act on requests (within reasonable time), then the model by
definition cannot work.

Beyond size, there are other reasons why the model may be unsuitable for a project:

- If a large degree of control over the project, its direction, implementation, copyright and legal
	status, or some such... is required. Caretaker requires trusting potentially any random stranger
	to _release live software to the world_. If that is antithetical to your project or philosophies
	there's no adaptation that will make it work: do no use it.

- If the project is security-critical, or used by a large amount of people, devices, companies...
	then, for the same reasons of trust, the model is inappropriate and should not be used.

- If the project is backed by or directly developed by a company, the model is likely untenable.

There may be other reasons not stated here: the model makes no claim of universality. Use it if, and
only as long as, it fits.

**One important note**: this section only applies to _projects_ deciding on whether to adopt the
model as their own, or to keep using it. Contributors, or even individual caretakers if in a larger
team, _cannot_ decide to ignore the model if the project they're contributing to uses it: unless
you're in a position to make or change them, you must follow the rules of the project, and if the
project uses this model, then the model's rules apply. No (unsanctioned) wiggling out.

