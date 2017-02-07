---
layout: post
title: Active Electrosense
categories: research
---

Few effective technologies exist for sensing in dark or murky underwater situations. For this reason, we have been exploring the use of a novel biologically-inspired approach to non-visual sensing based on the detection of perturbations to a self generated electric field. This is used by many species of neotropical nocturnal freshwater fish. This approach, termed active electrosense, provides unique capabilities for sensing of nearby objects.

Northwestern University has pioneered developing electronic equivalents to active electrosense. Together with Fred Boyer's group, we organized the First International Workshop on Robotic Electrosense in 2012.

### Fundamentals of Electrosense

Electrosense is fundamentally different from systems based on propagating wave phenomenon which include ultrasound imaging and optical vision. Projective imaging of the 3D space and point-to-point geometrical mapping of an image are not possible with electrosensory data. The generated field structure (magnitude and orientation) is highly dependent on geometry and impedance of the system. When objects whose conductivities differ from the surrounding fluid are introduced, they cause spatial distortions measurable in voltage and phase. These perturbations contain information that is characteristic of object geometry and conductivity.

![Electrosense with a conducting object]({{site.url}}/assets/Fig01_electrosense.png)

The image above provides an example of how this sensory mechanism works.  In A, two electrodes (red) are set to emit a bi-phasic oscillating signal. Another two electrodes (green) are positioned orthogonal to the original pair and all electrodes are equidistant from a center point.  When the green electrodes are measured differentially in an open space with no objects present, a voltage perturbation of 0 is measured.  In B, when we add an object whose conductivity differs from the surrounding fluid (in this case a conductive object), the field is perturbed so that we are able to measure a change in voltage. This system creates the basic unit we use for active electrosense where changes in the conductivity of the environment can be sensed.

However, due to electrical current diffusion into the body of water and complex environment-object interactions at the object boundary, the inverse problem relating measurements to the spatial distribution of the impedances is ill-posed and non-unique, making a direct mapping from data to image impossible. To limit the solution space, a priori knowledge about the surroundings, including boundary conditions and geometry are required.

We are working on novel algorithms that use statistical learning that rely on both resistive and capacitive sensing, to identify, differentiate and track objects for implementing obstacle avoidance and target tracking in unfavorable underwater conditions. 