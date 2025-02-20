---
title: MISP 2.4.56 released
date: 2016-12-07
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP [2.4.56](https://github.com/MISP/MISP/tree/v2.4.56) has been released, including bug fixes and improvements.

This is the first version introducing the [misp-galaxy](https://github.com/MISP/misp-galaxy). MISP galaxy is a simple method to express
large objects called cluster that can be attached to MISP events or (in the near future) attributes. A cluster can be composed of one or more elements, 
which are expressed as key-value pairs. You can now directly benefit from the shared galaxy with threat actors and tools used by attackers in MISP.

![MISP galaxy](/img/blog/galaxy.png "{class='img-responsive'}")
![MISP galaxy](/img/blog/cluster.png "{class='img-responsive'}")

The release includes various improvements such as:

- [API] Added the published flag to restsearch.
- [modules] Added the possibility to specify a "type" instead of a list of "types" in the enrichment modules.
- Significant improvements in the Bro export format and process.
- Improvements of the discussion/posts.
- Many bug fixes in the API and UI.

We thank all contributors.

The full change log is available [here](http://www.misp-project.org/Changelog.txt).

Don't hesitate to [open an issue](https://github.com/MISP/MISP/issues) if you have any feedback, found a bug or want to propose new features.
