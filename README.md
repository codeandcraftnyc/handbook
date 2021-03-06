# Handbook

This is a living document of common, company-wide practices for
[_smooth operation_](https://www.youtube.com/watch?v=4TYv2PhG89A) day-to-day.
I think we should encourage conversation around this document -- what works,
what doesn't, and how we can change for the better. The items below will be
written in a pseudo-RFC format, utilizing the keywords listed in the IETF's
[RFC 2119](http://tools.ietf.org/html/rfc2119).



## Tools

The services below provide really solid baseline support for operating a
business. They also provide really wonderful APIs, so if there's a feature
that's missing or that could improve our workflow **we can totally build it**.

- [**Harvest**](https://www.getharvest.com/), time tracking and cost analysis
- [**Tracker**](https://www.pivotaltracker.com/), project management and
  planning (review the philosophy behind this tool
  [here](https://www.pivotaltracker.com/help/gettingstarted))
- [**Google Apps**](https://apps.google.com/), email, calendar, file store
- [**GitHub**](https://www.github.com/), codebases and other versioned
  resources
- [**Slack**](https://www.slack.com/), team chat



## Clients, Projects, and Tasks

- organization
- how they relate to services listed above

#### Defining Stories

...

#### Supporting Assets

...

#### Tracking Time

...



## Communication

- when to use what
- best practices

#### Email

...

#### Chat (Slack)

...

#### Meetings

These can get unweildy quickly, and we've all got limited space in our heads,
so let's keep them as simple and understandable as possible. When you need to
add a calendar event you SHOULD follow these steps:

- prefix the event with the client code e.g. `[JAKO]` or `[COG]` -- this makes
  it easy to see what the meeting is about at a glance. Use `[CC]` for Code &
  Craft internal meetings.
- include the purpose of the meeting in the description.
- include links to relevant items in our PM tool.
- add the event to _Code & Craft_ Google calendar so it's visible to everyone.
  [screenshot](resources/meetings-calendar.png)
- invite everyone (including yourself) that needs to be involved.
- allow guests to modify the meeting so anyone can keep it updated.
  [screenshot](resources/meetings-modify.png)

> **Note:** many suggest keeping meetings to [15 minutes or less](https://open.bufferapp.com/how-to-hold-a-better-meeting-research/),
> so unless it's a whiteboarding session (or something similar) try to stick
> to a timeline.



## Onboarding

- add accounts for tools listed above
- ???



## Design

...



## Development

#### Stack

...

#### Styleguides & Linting

We keep common styleguides accessible here so we can maintain consistency
across projects, prototypes, etc. You SHOULD include the linter files in
any new project and maintain coding style.

- **JavaScript**, [styleguide](docs/styleguide-javascript.md) and
  [JSCS config](resources/.jscsrc)
- **SCSS**, [styleguide](docs/styleguide-scss.md) and
  [Sass Lint config](resources/.sass-lint.yml)

#### Build Tools

...

#### Source Control

We use [Git](https://git-scm.com/) and employ a fairly basic branching model.
The `master` branch is the source-of-truth and SHOULD be "staging-ready" and
presentable -- if it's a user-facing app, clients will be looking at it.

When working on a feature or fix you SHOULD create a separate branch with a
description name e.g. `account-management` or `fix-broken-images`. We do
utilize [pull requests](https://help.github.com/articles/using-pull-requests/)
and you SHOULD open one up onto the `master` branch as soon as you've branched
away with the intention of eventually merging. It's meant to be a discussion
and will evolve with the feature or fix.

#### Testing

...

#### Hosting

#### Continuous Integration (CI) / Continuous Deployment (CD)

Some type of continuous integration SHOULD be employed for each code base.
Implementing these tools up front eliminates a lot of opportunities for
mistakes down the road, especially if your test suite is kept up-to-date (as
it should be). Here are some options:

- [TravisCI](https://travis-ci.org/), for anything publicly available
- [Wercker](http://wercker.com/), for private repositories

Continuous deployment can be accomplished by our hosting platform,
[Heroku](https://www.heroku.com/). Set up the app to monitor the related
Github repository and run an automated deploy to staging _after the CI has
completed_.

#### Checklist

- [ ] test

