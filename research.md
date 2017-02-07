---
title: Research
permalink: /research/
---


Our research is centered around fish. Part of the lab is focused on  weakly electric fish *Apertonus albifrons* looking at active sensing, motion and agility for a detailed analysis of how the brain performs signal processing on sensory signals. The other part of the lab analyzes prey capture behavior and key midbrain circuits in larval zebra fish in collaboration with Prof. David McLean at Northwestern University to understand how brains process complex stimuli in the generation of motor programs. 

## Current Research

  {% for post in site.posts %}
    {% if post.categories contains ‘research’ %}
    <div class="list-item">
    <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%m/%d/%y" }}</small>)
        </p>
    </div>
    {% endif %}
  {% endfor %}
