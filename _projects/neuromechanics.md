---
title: Neuromechanics of Prey Capture
name: neuromechanics
---

### Neuromechanics of Prey Capture

<p style="text-align:justify" width="100%">Sensing, tracking, and then attacking other animals to
consume is one of the most highly evolved and complex behaviors animals perform. We study the
mechanical and neural principles underlying this behavior in two model systems: the larval
zebrafish, Danio rerio, and the black ghost electric knifefish, Apteronotus albifrons.
Larval zebrafish are a leading vertebrate genetic model system. While only 4 mm long, their
brains contain all the key vertebrate brain modules packaged within a completely transparent body.
This enables visualization of the function of the nervous system at level beyond what is possible
in any other vertebrate. In collaboration with Prof. David McLean at Northwestern, we are analyzing
prey capture behavior and key midbrain circuits to understand how brains process complex stimuli in
the generation of motor programs. Black ghost knifefish are an ideal system for detailed analysis of
how the brain performs signal processing on sensory signals, and provide an exquisite system for the
analysis of the mechanics of agility.
<br><br>
    The video below is of a 4 millimeter long larval zebrafish
hunting a 0.1 millimeter long Paramecium. Shot at 250 frames per second, movie exported at
30 FPS. Total actual time: just under one second.</p>

<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55642867" width="640" height="640" frameborder="0" allowfullscreen></iframe></p><br>

<p style="text-align:justify" width="100%">The same prey capture event after automated
tracking combined with some postprocessing to extract curvature (heat map), and body
velocity (blue line) and body angle (green line). </p>

<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55642806" width="640" height="480" frameborder="0" allowfullscreen></iframe></p><br>


#### People<br>

{% assign people_sorted = site.people | sort: 'joined' %}

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
    {% for profile in people_sorted %}
      {% if profile.project contains "preycapture" %}
          {% if profile.position contains "gradstudent" %} 
              {% assign profile_full = profile.name | append: ',  PhD student' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% elsif profile.position contains "postdoc" %}
              {% assign profile_full = profile.name | append: ' ,  Postdoc' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% elsif profile.position contains "research" %}
              {% assign profile_full = profile.name | append: ' ,  Research Staff' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% elsif profile.position contains "alumni" %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a></li>
          {% endif %}
      {% endif %}
    {% endfor %}
  <li>Matt Green</li> 
</ul>

#### Collaborators<br>

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
  <li><a class="research" href="https://www.neurobiology.northwestern.edu/people/core-faculty/david-mclean.html">Prof. David McLean, Dept. of Neurobiology, Northwestern Universtiy</a></li>
</ul>

### Related Publications<br>

_Intersection of motor volumes predicts the outcome of predator-prey interactions_<br>
Kiran D. Bhattacharyya, David L. McLean, Malcolm A. MacIver<br>
bioRxiv, 2019 ([Preprint](https://www.biorxiv.org/content/10.1101/626549v1.abstract))

_Visual threat assessment and reticulospinal encoding of calibrated responses in larval zebrafish_<br>
Kiran D. Bhattacharyya, David L. McLean, Malcolm A. MacIver<br>
Current Biology, 2017 ([Article](https://www.sciencedirect.com/science/article/pii/S0960982217310217))

_Visually guided gradation of prey capture movements in larval zebrafish_<br>
Bradely W. Patterson, Aliza O. Abraham, Malcolm A. MacIver, David L. McLean<br>
Journal of Experimental Biology, 2013 ([Article](https://jeb.biologists.org/content/jexbio/216/16/3071.full.pdf?download=true))

_Optimal movement in the prey strikes of weakly electric fish: a case study of the interplay of body plan and movement capability_<br>
Claire M. Postlethwaite, Tiffany M. Psemeneki, Jangir Selimkhanov, Mary Silber, Malcolm A. MacIver<br>
Journal of The Royal Society Interface, 2009 ([Article](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2659693/))

_Neuroethology: From Morphological Computation to Planning_ Malcolm A. MacIver<br>
The Cambridge Handbook of Situated Cognition (2009), Robbins P. & Aydede M. (eds). Cambridge University Press: Capter 26, 48-504

_Omnidirectional sensory and motor volumes in electric fish_<br>
James B. Snyder, Mark E. Nelson, Joel W. Burdick, Malcolm A. MacIver<br>
PLoS Biology, 2007 ([Article](https://journals.plos.org/plosbiology/article/file?type=printable&id=10.1371/journal.pbio.0050301))

_Modeling electrosensory and mechanosensory images during the predatory behavior of weakly electric fish_<br>
Mark E. Nelson, Malcolm A MacIver, Sheryl Coombs<br>
Brain, Behavior and Evolution, 2002 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.537.5035&rep=rep1&type=pdf))

_Prey-capture behavior in gymnotid electric fish: motion analysis and effects of water conductivity_<br>
Malcolm A. Maciver, Noura M. Sharabash, Mark E. Nelson<br>
Journal of Experimental Biology, 2001 ([Article](https://jeb.biologists.org/content/jexbio/204/3/543.full.pdf))

_Prey capture in the weakly electric fish Apteronotus albifrons: sensory acquisition strategies and electrosensory consequences_<br>
Mark E. Nelson, Malcolm A. MacIver<br>
Journal of Experimental Biology, 1999 ([Article](https://jeb.biologists.org/content/jexbio/202/10/1195.full.pdf))
