---
title: People
permalink: /people/
---

<br><br>

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|gradstudent|researchstaff" | split: "|" %}
 
{% for role in role_array %}

 {% assign people_in_role = people_sorted | where: 'position', role %}

 <div class="pos_header">
  {% if role == 'pi' %}
 <h3>Principal Investigator</h3>
  {% elsif role == 'gradstudent' %}
 <h3>Graduate Students</h3>
 {% endif %}
 </div>
 
<div class="content list people">
  {% for profile in people_sorted %}
     {% if profile.position contains role %}
         <div class="list-item-people">
           <p class="list-post-title">
               {% if profile.avatar %}
                   <a href="={{ site.url }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
               {% else %}
                   <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/default.png"></a>
               {% endif %}
               <a class="name" href="{{ site.url }}{{ profile.url }}">{{ profile.name }}</a>
         </p></div>
     {% endif %}
  {% endfor %}
</div>

{% endfor %}

<div class="pos_header">
 <h3>Alumni 4</h3></div>
 
 <br>

| Name | Position | Current Position |
| :------------- |:-------------| :-----------|
| Jordan Haskel | Master of Science in Robotics Student | Brain Corp |
| Chen Chen | Graduate Student | Apple Computer |
| Kiran Bhattacharyya | Graduate Student (2013 - 2019) | Intuitive Surgical |
| Sam Minkowicz | Rotation Student | Northwestern (Genia Kozorvitskiy's Lab)  |
| Michael Wiznitzer | Master of Science in Robotics Student | BITO Robotics |
| Matthew Green | Postdoc | - |
| Luke Shi | Master of Science in Robotics Student | - |
| Abhishek N. Patil | Master of Science in Robotics Student | Hilti Group |
| Sandra Fang | Masters Student | Raytheon |
| Ritwik Ummaleneni  | Master of Science in Robotics Student | Auris Health Inc. |
| Yang Bai | Graduate Student  | Google |
| Izaak Neveln | Graduate Student | Postdoc at Georgia Tech |
| Alfred Astor | Undergraduate (Mechanical Eng. and Neurobiology) | - |
| Jonathan Denose | Undergraduate (Electrical Engineering) | Ford Motor Company |
| Michael Smith | Undergraduate (Computer Science) | Northwestern |
| Nicholas Ohl | Undergraduate (Biomedical Engineering | Epic |
| Scott Schaper | Undergraduate (Mechanical Engineering) | Deublin Company |
| Yue Sun  | Master of Science in Robotics Student | - |
| Adam Binrbaum | Undergraduate | - |
| Alexandra Faye Salomon | Undergraduate (HHMI Mentoring Fellows Program) | - |
| Aliza Abraham | Undergraduate (Integrated Science Program) | Researcher, Universtiy of Minnesota |
| Brad Patterson | Graduate Student (with David McLean) | US Army Intelligence |
| Yoni Silverman | Masters Student | Nuclear power controls company |
| James Snyder | Graduate Student | Progeny Systems Corporation |
| Rahul Bale | Graduate Student (with Neelesh Patankar) | Postdoc at RIKEN, Japan |
| Oscar Curet | Graduate Student (with Neelesh Patankar) | Assistant Professor at Florida Atlantic University |
| Chris Mullens | Rotation Student | Northwestern |
| Kyle Liske | Undergraduate (Mechanical Engineering) | Titan Aerospace |
| Ethan Coeffel | Undergraduate (Computer Science) | Postdoc at Dartmouth |
| Leland Gossett | Undergraduate (Biomedical Engineering) | - |
| Chris Semple | Undergraduate (Biomedical Engineering) | Brandt Group of Companies |
| Uzair Admani | Undergraduate (Biomedical Engineering) | Resident Physician, University of Rochester |
| Omar Hassan | Undergraduate (Biomedical Engineering) | Resident Physician, University of California, San Francisco |
| Srinivas Ramakrishnan | Postdoc (with Neelesh Patankar) | ANSYS, Inc. |
| Anup Shirgaonkar  | Postdoc (with Neelesh Patankar) | Investment Management, Quantitative Machines |
| Ricardo Ruiz-Torres | Rotation Student | Northwestern (Lee Miller's Lab) |
| Claire Postlethwaite | Postdoc (with Mary Silber) | Assistant Professor at University of Auckland, New Zealand |
| Aravinda Gunda | Undergraduate (SINE Intern, George Washington University) | - |
| Jad Garson | Undergraduate (Biomedical Engineering) | Booz Allen Hamilton |
| Benjamin Proznitz | Undergraduate (Engineering Science and Applied Math) | - |
| Jangir Selimkhanov | Undergraduate (Engineering Science and Applied Math) | Takeda San Diego, Inc. |
| Alec Zopf | Undergraduate (Biomedical Engineering) | Wellth |
| Michael Epstein | Graduate Student (with Ed Colgate) | Consulting |
| James Solberg | Graduate Student (with Kevin Lynch) | HDT Expeditionary Systems Inc. |
| Aimee Schultz | Masters Student | Academic science paper writer |
| Irene Chiang | Undergraduate (Biochemistry, Molecular, and Cell Biology) | - |
| Alfred Shoukry | Undergraduate (Biomedical Engineering) | Physician, University of Pittsburgh |
| Vicky Huang | Undergraduate (Biomedical Engineering) | - |
| Clif Lin | Undergraduate (College of Arts and Science) (with T. Kuiken) | - |
| Lydia Wood | Rotation Student | Northwestern (Gordon Shepherd's Lab) |
| Brian London | Rotation Student | Norhtwestern (Lee Miller's Lab) |
| Tiffany Keung | Undergraduate (Biomedical Engineering) | - |
| Marie Kyle | Undergraduate (Mechanical Engineering) (with E. Colgate) | wefox Group |
| Elana Green | Undergraduate (Mechanical Engineering) (with E. Colgate) | - |
| Colin Tan | Undergraduate (Biomedical Engineering) | EndoMaster Pte Ltd |
| Karin Stensvad | Undergraduate (Biomedical Engineering) | - |
| Beth Lapour | Undergraduate (Mechanical Engineering, Washington University) (with E. Colgate) | - |
| Ani Chatterjee | Undergraduate (Biomedical Engineering) | BD |

