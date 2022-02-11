---
title: "Support Policy"
slug: "support-policy"
description: "60 days after a version is released, all previous releases will be considered deprecated"
---

* toc
{:toc}

When a new version of a software package is released, users are expected to upgrade as soon as possible.

**60 days after a version is released, all previous releases will be considered deprecated.** Devices running deprecated software may experience breaking changes that result in a loss of access to FarmBot servers. Bug reports for deprecated releases will not be investigated unless the issue is reproducible on non-deprecated releases.

For example, if FarmBot OS v1.2.3 is released on January 1st, and a user does not upgrade by March 2nd, the device may experience breaking changes.

# Best practices

 * Enable [auto-update](../../app/settings/farmbot-settings.md#auto-update) on your device. (All new accounts have auto-update enabled by default)
 * If you decide against automatic updates, consider subscribing to the [FarmBot newsletter](http://newsletter.farm.bot) to receive alerts about new versions of FarmBot OS.
 * Avoid service disruptions by ensuring your device still falls within the software support timeframe described above.

# Problems with old software versions

Supporting old versions of FarmBot OS presents a number of problems, both for users and software developers. Old software is less secure and has fewer features than newly released versions. Old software also creates support issues that take software developers away from new feature development.

To focus as much of our resources on moving forward, FarmBot Inc does not provide long term support for versions of old software. Supporting old software versions:

 * Increases QA effort, leading to a slower release cycle and fewer new features.
 * Takes support staff away from more serious issues due to a high number of bug reports that were resolved in more current releases.
 * Causes slowdowns and compromises on new feature development due to backward compatibility requirements.
 * Hurts the legitimacy of FarmBot when security breaches occur due to unpatched vulnerabilities by end-users that refuse to upgrade.

{%
include callout.html
type="info"
title="No LTS"
content="Due to resource constraints and the issues noted above, **FarmBot Inc does not provide [long term support (LTS)](https://en.wikipedia.org/wiki/Long-term_support) for any of its software packages** and reserves the right to deny server access to devices that fail to update in a timely manner."
%}

