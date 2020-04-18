---
title: Algorithmic and Neural Basis of Naturalistic Decision Making
name: electrosense
---

### Algorithmic and Neural Basis of Naturalistic Decision Making

<p style="text-align:justify" width="100%">When a situation affords a long latency between stimulus and response, 
deliberative behavioral control can be used to generate behavior that is strategic, variable, and hard to predict by an 
adversary. As this latency decreases, reactive control takes over and generates responses that are fast, less variable, and
easier to predict by an adversary. We can characterize deliberative behavioral control or planning as action choices that 
occur after internally simulating more than one action sequence and its respective consequences. Conversely, reactive control 
is a rapid stimulus-evoked response. A large amount of research suggests that these two decision making systems have different 
neural substrates. Interestingly, the similarities between the lamprey (jawless fish that preceded mammals by 560 million 
years) and mammalian neural system that is implicated in reflexive behavior suggests that reactive control evolved very early
on in the vertebrate evolution. In contrast, behavioral and neural evidence for planing and higher level cognition seems to 
only exist for mammals and birds. Evidence for planning is less clear for reptiles and amphibians, and similarly ambiguous or 
absent in fish.</p>
<br>
<p style="text-align:justify" width="100%">Assuming the apparent absence of plan-based decision making in fish and other 
early vertebrates is correct (and not simply due 
to a lack of study relative to terrestrial vertebrates), we can use the uneven distribution of higher level cognition to gain 
insight into why we only see this in (certain) animals.</p> 

<figure><center>
  <img width="800" src="{{site.baseurl}}/images/posts/decision-making.png" data-action="zoom">
</center></figure>

<p style="text-align:justify" width="100%">Conventionally, we think of nervous systems as the means by which an animal organizes its world, but a deep time perspective suggests that it is rather the world of an animal that organizes its brain. Our work shows that prior to the vertebrate invasion of land 385 million years ago, eyes tripled in size and shifted from the sides to the top of the head. Simulations of these animal's visual ecology suggests that these morphological changes would only be advantageous if animals were viewing through air, just above the water line, while still primarily inhabiting water. Therefore, before permanent life on land these animals probably hunted like crocodiles, where the vastly higher transparency of air enabled a more than 100-fold increase in visual range when compared to vision through water. The increase in visual range allowed these early vertebrates to see distant potential drivers of behavior, such as predator or prey, and afforded long delays between stimulus and response.  A possible reason for the greatly increased size and complexity of terrestrial vertebrate brains over those of fish is that this environment provides selective advantage to long sequences of actions toward distant goals, reaching its most complex form in varieties of prospective cognition in certain mammals and birds.</p> 

<figure><center>
  <img width="800" src="{{site.baseurl}}/images/posts/skull_visualrange.png" data-action="zoom">
</center></figure>

<hr>

Rooted in  evolution, we study both the algorithmic formalization and neural substrates of naturalistic decision making, which encompasses decision making in temporally extended naturalistic environments. Our theoretical and algorithmic work aims to elucidate the effects of environment topology and complexity on state-space representations, and choice of arbitration between habit and planning. Our empirical work, conducted in collaboration with Daniel Dombeck (Department of Neurobiology), involves both behavioral and in-vivo imaging of mammalian brains in highly uncertain environments that mimic idealized predator-prey interactions to understand the biological mechanisms involved in decision making in more naturalistic tasks.  

<table class="media">
  <tr>
    <td valign="top" width="70%">
      <figure><center>
          <img width="721" height="300" src="{{site.baseurl}}/images/posts/vr-system.png" data-action="zoom">
        </center></figure></td>
     <td valign="top" width="30%">
      <figure><center>
          <img width="355" height="300" src="{{site.baseurl}}/images/posts/maze.png" data-action="zoom">
        </center></figure></td>
  </tr>
</table>

#### People<br>

{% assign people_sorted = site.people | sort: 'joined' %}

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
    {% for profile in people_sorted %}
      {% if profile.project contains "planning" %}
          {% if profile.position contains "gradstudent" %} 
              {% assign profile_full = profile.name | append: ',  PhD student' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% elsif profile.position contains "postdoc" %}
              {% assign profile_full = profile.name | append: ' ,  Postdoc' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% elsif profile.position contains "research" %}
              {% assign profile_full = profile.name | append: ' ,  Research Staff' %}
              <li> <a class="research" href="{{ site.baseurl }}{{ profile.url }}">{{ profile_full }}</a></li>
          {% endif %}
      {% endif %}
    {% endfor %}
</ul>

#### Collaborators<br>

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
  <li><a class="research" href="https://www.neurobiology.northwestern.edu/people/core-faculty/daniel-dombeck.html"?>Daniel Dombeck, Dept. of Neurobiology, Northwestern Universtiy</a></li>
  <li><a class="research" href="http://www.dombecklab.org/lab-members/"?>Heydar Davoudi, Postdoc in the Dombeck Lab</a></li>
</ul>

#### Related Publications<br>

_Spatial planning with long visual range benefits escape from visual predators in complex naturalistic environments_<br>
Ugurcan Mugan, Malcolm A. MacIver<br>
Under revision, Nature Communications, 2020 ([Preprint](https://www.biorxiv.org/content/10.1101/585760v2))

_Arbitrating between planning and habit in naturalistic environments_<br>
Ugurcan Mugan, Malcolm A. MacIver<br>
Conference on Cognitive Computational Neuroscience, Berlin GR, 2019 ([Article](https://robotics.northwestern.edu/documents/publications/mugan.pdf))

_How sensory ecology affects the utility of planning_<br>
Ugurcan Mugan, Malcolm A. MacIver<br>
Conference on Cognitive Computational Neuroscience, Philadelphia PA, 2018 ([Article](https://robotics.northwestern.edu/documents/publications/Muga18a_ecology_planning.pdf), [Presentation](https://www.youtube.com/watch?v=yKILeeI_9n0&feature=emb_title))

_Massive increase in visual range preceded the origin of terrestrial vertebrates_<br>
Malcolm A. MacIver, Lars Schmitz, Ugurcan Mugan, Todd D. Murphey, Curtis D. Mobley<br>
Proceedings of the National Academy of Sciences, 2017 ([Article](https://www.pnas.org/content/114/12/E2375.short), [Video Explainer](https://youtu.be/I19usgWHJLc))

_Neuroscience Needs Behavior: Correcting a Reductionist Bias_<br>
John W. Krakauer, Asif A. Ghazanfar, Alex Gomez-Martin, Malcolm A. MacIver, David Poeppel<br>
Neuron, 2017 ([Article](https://www.sciencedirect.com/science/article/pii/S0896627316310406))

