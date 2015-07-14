---
title: Drupal Multisite Workaround
description: Best practices for having two Drupal sites on one domain.
category:
  - developing
  - drupal
keywords: drupal, multisite, domains
---
Pantheon only supports one Drupal core and one database per site. We do not support database prefixes or multisite. Our workflow, backup, and deployment tools only perform as expected given the standard Pantheon setup. If you try to install a second site inside your site container, there are no warranties and you'll probably break it.

While we can't make specific recommendations, we can give general best practices for having two sites under one domain. This is what is known as a “Drupal” problem, as it is a very common issue for which many strategies and workarounds exist. A great summary of the issue is published at the following:
http://www.palantir.net/blog/multi-headed-drupal

What will work on Pantheon is:

Separate Installs with redirection to a subdomain
Features based installs with Pantheon One custom upstreams and redirection to a subdomain
Domain Access on a single site install ** Try https://www.drupal.org/project/subfolders_domain but no guarantee it would work.
Organic Groups
