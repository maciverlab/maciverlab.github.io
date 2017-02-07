---
title: Research
permalink: /research/
---


Our research is centered around fish. Part of the lab is focused on  weakly electric fish *Apertonus albifrons* looking at active sensing, motion and agility for a detailed analysis of how the brain performs signal processing on sensory signals. The other part of the lab analyzes prey capture behavior and key midbrain circuits in larval zebra fish in collaboration with Prof. David McLean at Northwestern University to understand how brains process complex stimuli in the generation of motor programs. 

## Current Research

  {% for post in site.posts %}
    {% if post.categories contains ‘research’ %}
  	<h3><strong>{{ page.title }}</strong><br/>
  	<small>posted on {{ page.date | date: '%B %-d, %Y'}}</small></h3>
  	{{ content }}
    {% endif %}
  {% endfor %}
