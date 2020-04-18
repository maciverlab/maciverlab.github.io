---
title: Active Electrosense
name: active_electrosense
---

### Active Electrosense

<p style="text-align:justify" width="100%">Few effective technologies exist for sensing in dark or murky underwater
situations. For this reason, we have been exploring the use of a novel biologically-inspired approach to non-visual
sensing based on the detection of perturbations to a self generated electric field. This is used by many species
of neotropical nocturnal freshwater fish. This approach, termed active electrosense, provides unique capabilities
for sensing of nearby objects.
<br>
Northwestern University has pioneered developing electronic equivalents to active electrosense. Together with Fred Boyer's group, we organized the First International Workshop on Robotic Electrosense in 2012.</p>


<figure><center>
  <img width="640" src="{{site.baseurl}}/images/posts/decision-making.png" data-action="zoom">
</center></figure>

<p style="text-align:justify" width="100%">The image above provides an example of how this sensory mechanism works.
In A, two electrodes (red) are set to emit a bi-phasic oscillating signal. Another two electrodes (green) are
positioned orthogonal to the original pair and all electrodes are equidistant from a center point.
When the green electrodes are measured differentially in an open space with no objects present, a voltage
perturbation of 0 is measured.  In B, when we add an object whose conductivity differs from the surrounding
fluid, the field is perturbed so that we are able to measure a change in voltage. This system creates the
basic unit we use for active electrosense where changes in the conductivity of the environment can be sensed.
<br>
The video below demonstrates what happens to the field and electrode measurements as an object flies
by an insulating pod.</p> 

<p style="text-align:center;"><iframe title="vimeo-player" src="https://player.vimeo.com/video/95799899" width="640" height="450" frameborder="0" allowfullscreen></iframe></p><br>

##### Exploration<br>

<p style="text-align:justify" width="100%">An intutive use for our active electrosensing robot is to explore
unknown underwater environments. There are plenty of techniques developed for vision and sonar,
however our induced voltage pertubations does not fit either of these categories. Rather than
abstracting and correlating the voltage pertubation with specific objects (see Statistical Object
Identification) we stay exclusively in the voltage domain. The assumption is that every object will
have a particular voltage profile; and thus searching for the areas that are unqiue in each profile
will help us localize objects more easily. The question that we ask is how do we optimally maximize
our time in the regions that will yield more salient information given that we don't know where our
objects are ahead of time. We use Bayesian filters, Fisher information as well as ergodicity to try
to answer our question. </p>

##### Exploration<br>

<p style="text-align:justify" width="100%">An intutive use for our active electrosensing robot is to explore
unknown underwater environments. There are plenty of techniques developed for vision and sonar,
however our induced voltage pertubations does not fit either of these categories. Rather than
abstracting and correlating the voltage pertubation with specific objects (see Statistical Object
Identification) we stay exclusively in the voltage domain. The assumption is that every object will
have a particular voltage profile; and thus searching for the areas that are unqiue in each profile
will help us localize objects more easily. The question that we ask is how do we optimally maximize
our time in the regions that will yield more salient information given that we don't know where our
objects are ahead of time. We use Bayesian filters, Fisher information as well as ergodicity to try
to answer our question. </p>

#### Obstacle Avoidance<br>

<p style="text-align:justify" width="100%">Simple reactive control algorithms can be applied to the
sensorPod to navigate through cluttered underwater environment. Shown below is a point of vision
(POV) shot of the sensorPod navigating through a simulated cluttered environment using electrosense.
The sensorPod moves autonomously with a single goal to traverse the tank from one end to the other.
The VU meter on the side shows the electric signals on the left and right-hand sides of the sensorPod.
The sensorPod tries to balance the electric signals on two sides to avoid obstacles.</p>

<p style="text-align:center;"><iframe title="vimeo-player" src="https://player.vimeo.com/video/88114546" width="640" height="480" frameborder="0" allowfullscreen></iframe></p>

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
  <li>Yang Bai</li>
  <li>Yonatan Silverman</li>
  <li>James Snyder</li>
  <li>James Solberg</li>
  <li>Sandra Fang</li>  
</ul>

#### Collaborators<br>

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
  <li><a class="research" href="https://robotics.northwestern.edu/people/profiles/faculty/peshkin-michael.html">Michael Peshkin, Dept. of Mechanical Engineering, Northwestern Universtiy</a></li>
  <li><a class="research" href="https://robotics.northwestern.edu/people/profiles/faculty/lynch-kevin.html">Kevin M. Lynch, Dept. of Mechanical Engineering, Northwestern Universtiy</a></li>
  <li><a class="research" href="https://sensor.cs.washington.edu/jrs.html">Joshua R. Smith, Dept. of Electrical &amp; Engineering, University of Washington</a></li>
  <li><a class="research" href="http://www.hdtglobal.com">HDT Global</a></li>
</ul>

### Related Publications<br>

_Human-in-the-loop active electrosense_<br>
Sandra Fang, Michael Peshkin, Malcolm A. MacIver<br>
Bioinspiration & Biomimetics, 2016 ([Article](https://iopscience.iop.org/article/10.1088/1748-3190/12/1/014001/pdf))

_Enhanced detection performance in electrosense through capacitive sensing_<br>
Yang Bai, Izaak D. Neveln, Michael Peshkin, Malcolm A. MacIver<br>
Bioinspiration & Biomimetics, 2016 ([Article](https://iopscience.iop.org/article/10.1088/1748-3190/11/5/055001/meta))

_Finding and identifying simple objects underwater with active electrosense_<br>
Yang Bai, James B. Snyder, Michael Peshkin, Malcolm A. MacIver<br>
The International Journal of Robotics Research, 2015 ([Article](https://journals.sagepub.com/doi/abs/10.1177/0278364915569813))

_Improving Object Tracking through Distributed Exploration of an Information Map_<br>
Izaak D. Neveln, Lauren M. Miller, Malcolm A. MacIver, Todd D. Murphey<br>
IEEE International Conference on Intelligent Robots and Systems (IROS), 2014 ([Article](https://robotics.northwestern.edu/documents/publications/Neve14b.pdf))

_Biomimetic and bio-inspired robotics in electric fish research_<br>
Izaak D. Neveln, Yang Bai, ... , Malcolm A. MacIver<br>
Journal of Experimental Biology, 2013 ([Article](https://jeb.biologists.org/content/jexbio/216/13/2501.full.pdf))

_Optimal Planning for Information Acquisition_<br>
Yonatan Silverman, Lauren M. Miller, Malcolm A. MacIver, Todd D. Murphey<br>
Intelligent Robots and Systems (IROS), Tokyo JP, 2013 ([Article](https://robotics.northwestern.edu/documents/publications/IRS13.pdf))

_Sensing Capacitance of Underwater Objects in Bio-inspired Electrosense_<br>
Yang Bai, James B. Snyder, Yonatan Silverman, Michael Peshkin, Malcolm A. MacIver<br>
IEEE/RSJ International Conference on Intelligent Robots and Systems, 2012 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.720.8311&rep=rep1&type=pdf))

_Underwater object tracking using electrical impedance tomography_<br>
James B. Snyder, Yonatan Silverman, Yang Bai, Malcolm A. MacIver<br>
IEEE/RSJ International Conference on Intelligent Robots and Systems, 2012 ([Article](https://ieeexplore.ieee.org/document/6386251))

_Location and Orientation Estimation with an Electrosensing Robot_<br>
Yonatan Silverman, Yang Bai, James B. Snyder, Malcolm A. MacIver<br>
IEEE Int. Conf. on Intelligent Robots and Systems (IROS), 2012 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.713.7064&rep=rep1&type=pdf))

_Active electrolocation for underwater target localization_<br>
James R. Solberg, Kevin M. Lynch, Malcolm A. MacIver<br>
The International Journal of Robotics Research, 2008 ([Article](http://groups.csail.mit.edu/drl/wiki/images/c/c6/SolbergLynchMacIverIJRR08ActiveElectrolocationForUnderwaterTargetLocalization.pdf))

_Robotic electrolocation: Active underwater target localization with electric fields_<br>
James R. Solberg, Kevin M. Lynch, Malcolm A. MacIver<br>
IEEE International Conference on Robotics and Automation, 2007 ([Article](https://ieeexplore.ieee.org/abstract/document/4209849/))

_Sensory acquisition in active sensing systems_<br>
Mark E. Nelson, Malcolm A. MacIver<br>
Journal of Comparative Physiology A, 2006 ([Article](http://nelson.beckman.illinois.edu/pubs/Nelson_MacIver06.pdf))

_Towards a biorobotic electrosensory system_<br>
Malcolm A. MacIver, Mark E. Nelson<br>
Autonomous Robots, 2001 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.23.5363&rep=rep1&type=pdf))
