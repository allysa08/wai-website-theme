---
title: "[in-progress] Updating WAI Website Resources"
permalink: /workflow/
ref: /workflow/
lang: en
github:
  repository: w3c/wai-website-theme
  path: content/workflow.md
---

{::nomarkdown}
{% include box.html type="start" title="Summary" class="" %}
{:/}

This page describes the process for editors to submit updates to the WAI website.

{::nomarkdown}
{% include box.html type="end" %}
{:/}

{% include toc.html %}

## Overview

This process enables parts of the WAI website to be developed independently through the lightweight [GitHub Flow](https://docs.github.com/en/get-started/quickstart/github-flow), and enables all publication on the WAI website to be coordinated by the website manager.

* One branch in each repository is designated as the publication branch. Publication branches are lightly [protected](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches) so that all changes to the WAI website are merged only by the site manager, technical lead, or maintainers &mdash; currently Shawn and Steve.
* Editors provide a single pull request to the publication branch when updates are ready for publication.
* Scheduled updates are usually published/deployed on Tuesdays.

## Workflow

* Each Working Group and editorial team defines their own workflow for drafting, reviewing, approving, and submitting updates.
  * All update work is carried out on feature branches. Several may be in progress at any time.
  * If pull request are used during development they are made to a staging/ready-to-publish branch, NOT the publication branch
  * Netlify previews are available for all pull requests.
  * Editors and/or project managers ensure [early coordination on user interface, shared component, and content updates](#coop), per below.
* When an update is ready for publication, the editor merges it into the designated staging/ready-to-publish branch. (Or if there is a single simple update, they can just create a single pull request to the publication branch as in the next step)
* When the editor wants the updates published, they:
  * Create a single pull request to the publication branch.
    * Include a brief summary of the changes. Explain everything that the website manager and/or technical lead needs to particularly be aware of.
    * Include details on any shared components or other things that need updating outside this resource repo. For example,  Liquid variables provided in the resource's `_config.yml` file that need to be copied across to the wai-website repo.
    * Assigned it to @shawna_slh.
    * If there are updates that the technical lead needs to be involved in, also assign it to @SteveALee.
  * Add a link to the pull request in the Publication Schedule _{@@ maybe a wiki page in a new GitHub repo that anyone can edit? or a page in https://www.w3.org/wiki/ except only Members can edit that...}_
    * Indicate if the technical lead needs to be involved in this publication or not.
* When the updates are published, the publisher does an initial check that things worked, and comments on the pull request so the editors can do additional checks.

## Coordinating User Interface, Shared Component, and Content Updates {#coop}

**Editors are responsible for ensuring that everything submitted for publication is indeed ready to publish** &mdash; that it is approved, tested, and carefully quality checked. Website publishers are not able to do thorough reviews before publication.

* All user interface ideas must be coordinated with the WAI website manager (currently Shawn) &mdash; ideally from the start of the idea, before people get attached to a particular option.

* All updates to shared components or other beyond the individual repo &mdash; to the website theme, config files, navigation.yml, etc. &mdash; must be coordinated with the WAI website technical lead before a pull request is submitted to the publication branch.

* All content updates must be approved by the Working Group that owns the repo content. In some cases, the Working Group has provided blanket approval for some types of updates, such as for some aspects of ACT Rules.

## Details

Publication branches are protected, and editable only by W3C staff. In most repos, the publication branch is main or master. All updates to appear in the WAI website are on this branch and will be merged by the site manager, technical lead, or maintainers &mdash; currently Shawn and Steve. As backup, any W3C staff (as W3C organization administrators) can edit or merge into the publication branch. To enable this, resource editors and other non-W3C-team have maximum repository access privileges "write".

Resource editors provide updates in a single pull request to the publication branch. If there are multiple updates, they can be provided in a staging/ready-to-publish branch, with a single pull request for that branch to be merged into the publication branch. Only highly-trusted individuals should have write access to the staging/ready-to-publish branch. Before updates are made in the staging/ready-to-publish branch, content updates have been approved by the Working Group, user interface updates approved by the website manager, and shared component updates approved by the technical lead.

WAI website updates are usually published/deployed on Tuesdays about 13:00UTC. Deploys on other days can be arranged ahead of time. Note that the site manager or maintainers will also likely deploy the site at other times, without prior notice.

After a pull request has been merged it is deleted in GitHub and the associated branch should also be deleted. GitHub keeps deleted pull requests and branches, and they can be restored.

Editors work with the WAI site manager and technical lead to coordinating considerations for:
* fit with existing content
* editorial style
* user experience
* accessibility
* internationalization
* theme and coding
* information architecture
* technical integration