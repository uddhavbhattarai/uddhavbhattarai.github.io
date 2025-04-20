---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 2
---

<div class="publications">

<h3 style="font-size: 1.8em;">Ph.D. Dissertation</h3>
{% bibliography --query @*[category=dissertation] %}

<h3 style="font-size: 1.8em;">Recent Preprints</h3>
{% bibliography --query @*[category=preprint] %}

<h3 style="font-size: 1.8em;">Published Journal Manuscripts</h3>
{% bibliography --query @*[category=journal] %}

<h3 style="font-size: 1.8em;">Published Book Chapters</h3>
{% bibliography --query @*[category=chapter] %}

<h3 style="font-size: 1.8em;">Published Conference Proceedings</h3>
{% bibliography --query @*[category=conference] %}



</div>
