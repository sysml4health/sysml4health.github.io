---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Co-located with MLSys'21 (Virtual)"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "Online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "FIXME"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "45"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-1"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "Apr 9, 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "FIXME"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2021-04-09      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-04-09        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: [] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: []     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["first@example.org","second@example.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---


{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}

<div class="alert alert-danger">
This is the workshop template. Delete these lines and use it to
<a href="https://carpentries.github.io/workshop-template/customization/index.html">customize</a>
your own website. If you are running a self-organized workshop or have not put
in a workshop request yet, please also fill in
<a href="{{site.amy_site}}/forms/self-organised/">this workshop request form</a>
to let us know about your workshop and our administrator may contact you if we
need any extra information.
</div>
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

{% comment %}
Check SWC curriculum
{% endcomment %}

{% if site.carpentry == "swc" %}
{% unless site.curriculum == "swc-inflammation" or site.curriculum == "swc-gapminder" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Software Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>swc-inflammation</code>, or <code>swc-gapminder</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<strong>Some adblockers block the registration window. If you do not see the
  registration box below, please check your adblocker settings.</strong>
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">General Information</h2>

This workshop focuses on the challenges involved in building integrated scalable distributed systems for the healthcare analytics domains. Healthcare analytics offers a unique opportunity to explore scalable system design since there has been a tectonic shift in the ability of medical institutions to capture and store unprecedented amounts of structured and unstructured medical data, including the new ability to stream unstructured medical data in real-time. This shift has already contributed to an ecosystem of Machine Learning (ML) models being trained for a variety of clinical tasks. However, new approaches are required to build systems that can develop and deploy ML models based on distributed healthcare data that must necessarily be accessed with privacy-preserving constraints. 

The goal of this workshop is to attract leading researchers to share and discuss their latest results involving approaches to building scalable platforms for privacy-aware collaborative learning and inference that can be applicable to the domain of healthcare analytics. The scope of the workshop includes (but is not limited to) the following challenges:

<ul>
  <li> Continuous federated learning with privacy constraints  </li>
  <li> Scalable and distributed learning  </li>
  <li> Enforcing soft real-time constraints for streaming data analytics  </li>
  <li> Specialized heterogeneous hardware for learning and inference  </li>
  <li> Scalable runtime and resource allocation systems  </li>
  <li> Productive systems for developing scalable data analytics applications  </li>
</ul>

We would like this workshop to help contribute new advances to healthcare analytics, which has the potential to result in significant benefits to society, by demonstrating how data can safely (with privacy preservation) be leveraged from distributed sources to improve the accuracy of trained ML models for various clinical tasks, how the models can be deployed in a scalable manner at all levels of the end-to-end system, and how these capabilities can help enable early warnings and rapid responses to hitherto unknown and rapidly evolving threats. Knowledge distilled from multiple sources of data can be embodied in recommendation systems that can run onsite to provide time-critical decision support to physicians. We expect principles that emerge from this workshop to be of interest to other application domains as well. 

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}



{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}


{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact:</strong>
  Please email sysml4health@gmail.com 
  for more information.
</p>

<hr/>

{% comment%}
CODE OF CONDUCT
{% endcomment %}

{% comment%}
<h2 id="code-of-conduct">CODE OF CONDUCT</h2>

<p>
Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>

<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Report a Code of Conduct Incident</button>
  </a>
</p>
<hr/>
{% endcomment %}


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Keynote Speakers</h2>
<ul>
  <li> Timothy Chou <a href="https://www.linkedin.com/in/timothychou/">[linkedin]</a> </li>
</ul>

<p>
  We are actively updating the list. Please stay tuned!
</p>

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.

Small changes to the schedule can be made by modifying the
`schedule.html` found in the `_includes` folder for your
workshop type (`swc`, `lc`, or `dc`). Edit the items and
times in the table to match your plans. You may also want to
change 'Day 1' and 'Day 2' to be actual dates or days of the
week.

For larger changes, a blank template for a 4-day workshop
(useful for online teaching for instance) can be found in
`_includes/custom-schedule.html`. Add the times, and what
you will be teaching to this file. You may also want to add
rows to the table if you wish to break down the schedule
further. To use this custom schedule here, replace the block
of code below the Schedule `<h2>` header below with
`{% include custom-schedule.html %}`.
{% endcomment %}

<h2 id="schedule">Tentative Schedule</h2>
{% include swc/schedule.html %}

{% comment %}
{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}
{% endcomment %}

<hr/>

<h2> Workshop Organizers </h2>
<ul>
<li> Tushar Krishna (Georgia Tech) </li>
<li> Vivek Sarkar (Georgia Tech) </li>
<li> Dawn Song (UC Berkeley) </li>
<li> Jimeng Sun (UIUC) </li>
<li> Alexey Tumanov (Georgia Tech) </li>
<hr/>


