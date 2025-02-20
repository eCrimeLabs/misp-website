---
title: MISP 2.4.96 released (aka API everywhere release)
date: 2018-10-09
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP ([2.4.96](https://github.com/MISP/MISP/tree/v2.4.96)) has been released with a complete rework, refactoring and simplification of the restSearch API, allowing for more flexibility, improved search capabilities, performance and extendability.

All of the MISP export APIs have now been unified into the restSearch APIs with a vastly improved query format. The complete documentation of the restSearch is included in the automation page.

A pagination system has been added allowing users to easily paginate over search result sets and limit the output. The two new parameters are limit and page, both directly accessible in the MISP query format.

The search results in the MISP UI now allows for the direct download of the search results in any of the supported formats available in MISP in a convenient and quick way.

The CSV export has been refined to remove inconsistencies in the requested field parameters and the header field names among other fixes.

The internal fetcher has been rewritten to use an internal pagination and caching mechanism that scales with the amount of memory given to the PHP process, increasing performance and reducing the chance of ever running into memory limit issues. Various other changes (such as resolving some bottlenecks in regards to object references, potential query length issues in certain situations, etc) improve both the stability and performance of all functions relying on fetching event / attribute data.

The freetext import is now delegated to a background process for large imports. It has also received additional tweaks such as support for ASN detection and additional indicator refanging rules.

The API for warning-lists has been improved and can now be updated by using a substring contained within a warninglist's name. A simple toggle function mechanism to disable and enable warning-lists via the API has also been added.

The [cortex integration is now back](https://blog.thehive-project.org/2018/09/27/cortex-2-1-0-the-response-edition/) to nominal and fully functional with this latest version.

A host of additional improvements and bugs fixed were introduced including improvements to the user-interface, API,  STIX 1/2 import and export, etc.

A huge thanks to all the [contributors](/contributors) who have tirelessly helped us improve the software and also all the participants in the MISP trainings giving us a bunch of interesting feedback for ideas for improvements.

MISP [galaxy](/galaxy.pdf), [objects](/objects.pdf) and [taxonomies](/taxonomies.pdf) were notably extended by many contributors. These are also included by default in MISP. Don't forget to do a `git submodule update` and update galaxies, objects and taxonomies via the UI.

Don't forget that the MISP Threat Intelligence Summit 0x4 will take place the Monday 15th October 2018 before hack.lu 2018. Don't hesitate to have a look at our [events page](http://www.misp-project.org/events/) to see our next activities to improve threat intelligence, analytics and automation. We have also two MISP trainings foreseen in Luxembourg Monday 17th December [MISP Training - Threat Intelligence Analyst and Administrators](https://en.xing-events.com/MURFIIQ) and Tuesday 18th December [MISP Training - Developers session - API and Extensions ](https://en.xing-events.com/QDBMTBT.html).
