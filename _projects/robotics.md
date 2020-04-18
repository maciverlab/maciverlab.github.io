---
title: Mechanics and Bio-Inspired Robotics of Fish Locomotion
name: robotics
---

### Mechanics and Bio-Inspired Robotics of Fish Locomotion

<p style="text-align:justify" width="100%">Knifefish are highly maneuverable swimmers capable of navigating
complex environments. The fish generate thrust by undulating an elongated ventral fin. We study the fin
mechanics using motion capture of live fish, computational fluid dynamics, and bio-inspired robotics.
Using these tools, we are uncovering the underlying principles of knifefish locomotion which can then
be implemented into underwater robotics to enhance maneuverability.<br>
<br>
Below is a video that demonstrates the forward and backward traveling waves
along the ribbon fin of the black ghost electric knifefish.
</p>

<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55545968" width="640" height="480" frameborder="0" allowfullscreen></iframe></p><br>



##### The knifefish Inspired GhostBot
<p style="text-align:justify" width="100%">We've built one
of the most advanced fish robots in the world, with 34 degrees of freedom (the humanoid robot ASIMO has 26;
the Roomba floor vacuum robot has 2), in order to better understand knifefish mechanics and sensorimotor
coupling. This video is the first where we discovered that inward counter-propagating waves generate a
strong downward jet, producing vertical thrust. This is a key element of knifefish maneuverability.
The water is seeded with reflective particles for subsequent particle imaging velocimetry. </p>

<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55543716" width="640" height="640" frameborder="0" allowfullscreen></iframe></p><br>


<p style="text-align:justify" width="100%">In this video, Ghostbot demonstrates 'nodal point control' in 
which a closed-loop positioning algorithm shifts the point at which inward counter-propagating waves
meet in order to control position. </p> 
<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55488639" width="640" height="360" frameborder="0" allowfullscreen></iframe></p><br>


<p style="text-align:justify" width="100%">We perform 3D Navier-Stokes simulations of 
fish and robot locomotion. Shown here is forward swimming followed by a rapid reversal, 
similar to what we discovered the real fish uses for hunting prey.</p> 

<p style="text-align:center;">
<iframe title="vimeo-player" src="https://player.vimeo.com/video/55488639" width="640" height="360" frameborder="0" allowfullscreen></iframe></p><br>


#### People<br>

{% assign people_sorted = site.people | sort: 'joined' %}

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
    {% for profile in people_sorted %}
      {% if profile.project contains "robotics" %}
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
  <li>Izaak Neveln</li>
  <li>Rahul Bale</li>
  <li>Oscar M. Curet</li>
  <li>Anup Shirgaonkar</li>
</ul>

#### Collaborators<br>

<ul style="list-style-position:outside;padding:0px;list-style-type:none;">
  <li><a class="research" href="https://www.mccormick.northwestern.edu/research-faculty/directory/profiles/patankar-neelesh.html">Prof. Neelesh Patankar,
  Computational and Theoretical Fluid Dynamics, Northestern University</a></li>
  <li><a class="research" href="https://oeb.harvard.edu/people/george-v-lauder">Prof. George V. Lauder,
  Dept. of Organismic &amp; Developmental Biology, Harvard University</a></li>
  <li><a class="research" href="https://limbs.lcsr.jhu.edu/people/cowan/">Prof. Noah J. Cowan,
  Dept. of Mechanical Engineering, Johns Hopkins University</a></li>
</ul>

### Related Publications<br>

_Sense organ control in moths to moles is a gamble on information through motion_<br>
Chen Chen, Todd. D. Murphey, Malcolm A. MacIver<br>
Under revision, eLife, 2020 ([Preprint](https://www.biorxiv.org/content/10.1101/826305v1), 
[Video Explainer](https://youtu.be/vOAzSa6Pna4))

_Feedback Synthesis For Underactuated Systems Using Sequential Second-Order Needle Variations_<br>
Giorgos Mamakoukas, Malcolm A. MacIver, Todd D. Murphey<br>
The International Journal of Robotics Research, 2018 ([Article](https://robotics.northwestern.edu/documents/publications/IJRR_published.pdf))

_Superlinear Convergence Using Controls Based on Second-Order Needle Variations_<br>
Giorgos Mamakoukas, Malcolm A. MacIver, Todd D. Murphey<br>
IEEE Conference on Decision and Control, Miami Beach FL, 2018 ([Article](https://robotics.northwestern.edu/documents/publications/CDC.pdf))

_Feedback Synthesis for Controllable Underactuated Systems using Sequential Second Order Actions_<br>
Giorgos Mamakoukas, Malcolm A. MacIver, Todd D. Murphey<br>
Robotics Science and Systems, 2017 ([Article](https://robotics.northwestern.edu/documents/publications/RSS_Jan17.pdf), [Video](https://robotics.northwestern.edu/documents/publications/videos/MamakoukasMacIverMurphey_RSS_2017.mp4))

_Ergodic Exploration of Distributed Information_<br>
Lauren M. Miller, Yonatan Silverman, Malcolm A. MacIver, Todd D. Murphey<br>
IEEE Transactions on Robotics, 2016 ([Article](https://arxiv.org/pdf/1708.09352.pdf),
[Video Explainer](https://robotics.northwestern.edu/documents/publications/videos/EEDI.mp4))

_Sequential Action Control for Models of Underactuated Underwater Vehicles in a Planar Ideal Fluid_<br>
Giorgos Mamakoukas, Malcolm A. MacIver, Todd D. Murphey<br>
American Control Conference (ACC), Boston MA, 2016 ([Article](https://robotics.northwestern.edu/documents/publications/Mama16a_ACC2016_0.pdf))

_Convergent evolution of mechanically optimal locomotion in aquatic invertebrates and vertebrates_<br>
Rahul Bale, Izaak D. Neveln, Amneet Pal Singh Bhalla, Malcolm A. MacIver, Neelesh A. Patankar<br>
PLoS Biology, 2015 ([Article](https://journals.plos.org/plosbiology/article/file?type=printable&id=10.1371/journal.pbio.1002123))

_Separability of drag and thrust in undulatory animals and machines_<br>
Rahul Bale, Anup A. Shirgaonkar, Izaak D. Neveln, Amneet Pal Singh Bhalla, Malcolm A. MacIver, Neelesh A. Patankar<br>
Scientific Reports, 2014 ([Article](https://www.nature.com/articles/srep07329))

_Separability of drag and thrust in undulatory animals and machines_<br>
Izaak D. Neveln, Rahul Bale, Amneet Pal Singh Bhalla, Oscar M. Curet, Neelesh A. Patankar, Malcolm A. MacIver<br>
Journal of Experimental Biology, 2014 ([Article](https://jeb.biologists.org/content/jexbio/217/2/201.full.pdf))

_Mutually opposing forces during locomotion can eliminate the tradeoff between maneuverability and stability_<br>
Shahin Sefat, Izaak D. Neveln, ... , Malcolm A. MacIver, Eric S. Fortune, Noah J. Cowan<br>
Proceedings of the National Academy of Sciences, 2013 ([Article](https://www.pnas.org/content/pnas/110/47/18798.full.pdf))

_Biomimetic and bio-inspired robotics in electric fish research_<br>
Izaak D. Neveln, Yang Bai, ... , Malcolm A. MacIver<br>
Journal of Experimental Biology, 2013 ([Article](https://jeb.biologists.org/content/jexbio/216/13/2501.full.pdf))

_Kinematics of the ribbon fin in hovering and swimming of the electric ghost knifefish_<br>
Ricardo Ruiz-Torres, Oscar M. Curet, George V. Lauder, Malcolm A. MacIver<br>
Journal of Experimental Biology, 2012 ([Article](https://jeb.biologists.org/content/jexbio/216/5/823.full.pdf))

_Counter-Propagating Waves Enhance Maneuverability and Stability: A Bio-Inspired Strategy for Robotic Ribbon-Fin Propulsion_<br>
Shahin Sefati, Izaak D. Neveln, Malcolm A. MacIver, Eric Fortune, Noah J. Cowan<br>
4th IEEE RAS & EMBS International Conference on Biomedical Robotics and Biomechatronics (BioRob), 2012 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.714.7296&rep=rep1&type=pdf))

_Optimal number of waves for ribbon fin propulsion_<br>
Rahul Bale, Amneet Pal Singh Bhalla, Malcolm A. MacIver, Neelesh A. Patankar<br>
Bulletin of the American Physical Society, 2012 ([Article](http://adsabs.harvard.edu/abs/2012APS..DFDG15008B))

_Mechanical properties of a bio-inspired robotic knifefish with an undulatory propulsor_<br>
Oscar M. Curet, Neelesh A. Patankar, George V. Lauder, Malcolm A. MacIver<br>
Bioinspiration & Biomimetics, 2011 ([Article](https://jeb.biologists.org/content/jexbio/216/5/823.full.pdf))

_Aquatic maneuvering with counter-propagating waves: a novel locomotive strategy_<br>
Oscar M. Curet, Neelesh A. Patankar, George V. Lauder, Malcolm A. MacIver<br>
Journal of the Royal Society Interface, 2011 ([Article](https://royalsocietypublishing.org/doi/pdf/10.1098/rsif.2010.0493))

_Hydrodynamic optimality of ribbon fin shapes_<br>
Rahul Bale, Malcolm A. MacIver, Neelesh A. Patankar<br>
Bulletin of the American Physical Society, 2011 ([Article](http://meetings.aps.org/link/BAPS.2011.DFD.H28.7))

_Can drag and thrust be separated in undulatory swimming_<br>
Neelesh A. Patankar, Anup A. Shirgaonkar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2009 ([Article](http://adsabs.harvard.edu/abs/2009APS..DFD.GV003P))

_Multi-directional thrusting using oppositely traveling waves in knifefish swimming_<br>
Oscar M. Curet, Malcolm A. MacIver, Neelesh A. Patankar<br>
Bulletin of the American Physical Society, 2009 ([Article](http://adsabs.harvard.edu/abs/2009APS..DFD.EV004C))

_The hydrodynamics of ribbon-fin propulsion during impulsive motion_<br>
Anup A. Shirgaonkar, Oscar M. Curet, Neelesh A. Patankar, Malcolm A. MacIver<br>
Journal of Experimental Biology, 2008 ([Article](https://jeb.biologists.org/content/jexbio/211/21/3490.full.pdf))

_Hydrodynamic aspects of thrust generation in gymnotiform swimming_<br>
Anup A. Shirgaonkar, Oscar M. Curet, Neelesh A. Patankar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2008 ([Article](http://adsabs.harvard.edu/abs/2008APS..DFD.BM001S))

_An efficient algorithm for fully resolved simulation of freely swimming bodies_<br>
Anup A. Shirgaonkar, Neelesh A. Patankar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2007 ([Article](http://adsabs.harvard.edu/abs/2007APS..DFD.GF005S))

_Infomechanical specializations for prey capture in knifefish_<br>
Malcolm A. MacIver, Neelesh A. Patankar, Oscar M. Curet, Anup A. Shirgaonkar<br>
Bulletin of the American Physical Society, 2007 ([Article](http://adsabs.harvard.edu/abs/2007APS..DFD.GD009M))

_Simulation of bio-locomotion by a momentum redistribution technique for self-propulsion_<br>
Oscar M. Curet, Anup A. Shirgaonkar, Neelesh A. Patankar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2007 ([Article](http://adsabs.harvard.edu/abs/2007APS..DFD.JU035C))

_An algorithm for low to moderate Reynolds number swimming_<br>
Oscar M. Curet, Neelesh A. Patankar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2007 ([Article](http://adsabs.harvard.edu/abs/2007APS..DFD.NH007C))

_Hydrodynamics of ribbon fin-based swimming with application to highly maneuverable underwater vehicles_<br>
Neelesh A. Patankar, Oscar M. Curet, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2006 ([Article](http://meetings.aps.org/Meeting/DFD06/Session/AA.12))

_Generating thrust with a biologically-inspired robotic ribbon fin_<br>
Michael Epstein, J. Edward Colgate, Malcolm A. MacIver<br>
IEEE/RSJ International Conference on Intelligent Robots and Systems, 2006 ([Article](https://ieeexplore.ieee.org/abstract/document/4058749/))

_Towards direct numerical simulation of freely swimming fish_<br>
Oscar M. Curet, Neelesh A. Patankar, Malcolm A. MacIver<br>
Bulletin of the American Physical Society, 2006 ([Article](http://meetings.aps.org/link/BAPS.2006.DFD.AA.8))

_A biologically inspired robotic ribbon fin_<br>
Michael Epstein, J. Edward Colgate, Malcolm A. MacIver<br>
IEEE/RSJ International Conference on Intelligent Robots and Systems, workshop on Morphology, Control, and Passive Dynamics, 2006 ([Article](https://pdfs.semanticscholar.org/f15b/e3613cc1da74a719d4c3330d17c124b8725a.pdf))

_Designing future underwater vehicles: principles and mechanisms of the weakly electric fish_<br>
Malcolm A. MacIver, Ebraheem Fontaine, Joel W. Burdick<br>
IEEE Journal of Oceanic Engineering, 2004 ([Article](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.116.1197&rep=rep1&type=pdf))
