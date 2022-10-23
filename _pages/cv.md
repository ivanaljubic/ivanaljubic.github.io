---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# Education

- Education 1
- Education 2
- Education 3

# Work experience

- Experience 1

  - Detail 1
  - Detail 2

- Experience 2
  - Detail 1
  - Detail 2

# Skills

- Skill 1
- Skill 2
  - Sub-skill 2.1
  - Sub-skill 2.2
  - Sub-skill 2.3
- Skill 3

# Publications

  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

<!-- # Talks

## Plenary/Keynote Talks

{% for post in site.talks reversed %}
{% if post.type == 'plenarykeynote' %}
{% include archive-single-talk-cv.html %}
{% endif %}
{% endfor %}

## Other Invited Talks, Seminars and Tutorials

{% for post in site.talks reversed %}
{% if post.type == 'othertalk' %}
{% include archive-single-talk-cv.html %}
{% endif %}
{% endfor %}

## Recent Presentations at International Conferences

{% for post in site.talks reversed %}
{% if post.type == 'intlpresentation' %}
{% include archive-single-talk-cv.html %}
{% endif %}
{% endfor %}

## Other Visited Events

- 17th Combinatorial Optimisation Workshop, Aussois, France, January 7-11, 2013.
- 12th Combinatorial Optimisation Workshop, Aussois, France, January 7-11, 2008.
- 11th Combinatorial Optimisation Workshop, Aussois, France, January 7-12, 2007.
- 7th Combinatorial Optimisation Workshop, Aussois, France, March 9-15, 2003.
- International Summer School on Metaheuristics
- Tenerife (Canary Islands), Spain, March 3-7, 2003.

## Research Visits Abroad

- Visiting Professor at the University Adolfo Ibanez, Santiago, Chile (March 2015)
- Visiting Professor at the University of Paris, Dauphine (September 2014)
- Visiting Researcher at the TU Berlin (October 2012 - Mai 2013)
- Visiting Researcher at the TU Dortmund (April 2012 - September 2012)
- Visiting Assistant Professor at the University of Maryland (July 2011 - March 2012)
- Other Research Visits:
- Optical Access Networks, COGA, TU Berlin (Andreas Bley), Germany, August, 2010
- The Generalized Regenerator Location Problem, Robert H. Smith School of Business, University of Maryland (S. Raghavan) College Park, MD, May 2010
- Solving two-stage stochastic Steiner tree problems by two-stage branch-and-cut, Department of Computer Science, TU Dortmund (Petra Mutzel), Dortmund, Germany, April 2010
- Two-Level Network Design Problems, Department of Statistics and Operations Research, Faculty of Sciences, Centro de Investigação Operacional (Luis Gouveia), Portugal, February 2010
- Polyhedral Study of the Connected Facility Location Polytope, Department of Computer Science, TU Dortmund (Petra Mutzel), Dortmund, Germany, May 2009
- The Generalized Regenerator Location Problem, Robert H. Smith School of Business, University of Maryland (S. Raghavan) College Park, MD, October 2008
- The Regenerator Location Problem, Robert H. Smith School of Business, University of Maryland (S. Raghavan) College Park, MD, April 2008
- Exact Approaches to Network Design Problems, Department of Computer Science, TU Dortmund (Petra Mutzel), Dortmund, Germany, July 2007
- k-Cardinality Tree Problems , Department of Computer Science, TU Dortmund (Petra Mutzel), Dortmund, Germany, July 2006
- An evolutionary approach to the fractional prize-collecting Steiner tree problem, University of La Laguna (Belen Melian), La Laguna, Spain, July & August 2004 -->

# Talks

  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>

<!-- Teaching

  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->
