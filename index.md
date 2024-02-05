---
layout: default
---

# Complexity Theory of Solvers

Conflict-driven clause-learning (CDCL) SAT solvers, as well as satisfiability modulo theories (SMT) solvers, routinely solve formulas with thousands to millions of variables and clauses, despite the satisfiability problem being NP-complete. At the same time, small randomly generated formulas are difficult for the same solvers. The goal of this work is to understand which aspects of modern SAT/SMT solvers, as well as which measures of SAT/SMT formulas, relate best to solving performance.

Our line of work follows along 4 main lines of reasoning:
* Deriving proof complexity lower bounds to demonstrate the hardness of certain formulas for modern solvers;
* Deriving parameterized complexity upper bounds to demonstrate how certain measures of formulas relate to hardness;
* Characterizing SAT/SMT solvers through the lens of machine learning;
* Improving our understanding of encodings and reductions of formulas.

# Publications
{% for item in site.data.publications %}
{% capture links %}
{%- if item.pdf -%} [[pdf]]({{ item.pdf }}) {% endif %}
{%- if item.bib -%} [[bib]]({{ item.bib }}) {% endif %}
{%- if item.slides -%} [[slides]]({{ item.slides }}) {% endif %}
{%- if item.talk -%} [[talk]]({{ item.talk }}) {% endif %}
{% endcapture %}

* **{{ item.title }}**  
	{{ item.authors }} {% if item.pub-type %}  
	{{ item.pub-type }} {% endif %} {% if item.date %}   
	{{ item.date }} {% endif %} {% if item.award %}  
	**{{ item.award }}** {% endif %}  
	{{ links }}	{% if item.note %}  
	\* {{ item.note }} {% endif %}
{% endfor %}