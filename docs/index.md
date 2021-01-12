---
layout: default
---

# AI Lifecycle | Mapping Study 🎓
by [Yuanhao Xie], [Luís Cruz], [Petra Heck], [Jan Rellermeyer]

This webpage presents the results of the mapping study submitted to the [1st Workshop on AI Engineering – Software Engineering for AI (WAIN'21)], colocated with [ICSE2021]. A replication package is available at <PLACEHOLDER FOR DOI.ORG>. For more details, check the [preprint at arxiv]().

TODO- What is AI lifecycle

TODO- What is the mapping study we did.

This mapping study analyzes the publications that look into the lifecycle of artificial intelligence projects from 2009 to May 2020 and maps it into 5 overarching categories:

- [Trustworthy](#trustworthy)
- [Production](#production)
- [Model Management](#model-management)
- [Lifecycle Management](#lifecycle-management)
- [Data Management](#data-management)

TODO-  Stats: how many papers etc,

🔗 [The dataset of publications is available as a CSV file](https://github.com/luiscruz/ai-lifecycle-mapping-study/blob/main/docs/_data/publications.csv).


## Trustworthy
{% for paper in site.data.publications %}
{%if paper.Main_Topic == "Trustworthy"%}
<p markdown='1'> - {{paper.Authors}} ({{paper.Year}}). [{{paper.Title}}](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22{{paper.Title}}%22&btnG=). {{paper.venue}}</p>
{% endif %}
{% endfor %}
[🔝back to top]()
## Production
{% for paper in site.data.publications %}
{%if paper.Main_Topic == "Production"%}
<p markdown='1'> - {{paper.Authors}} ({{paper.Year}}). [{{paper.Title}}](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22{{paper.Title}}%22&btnG=). {{paper.venue}}</p>
{% endif %}
{% endfor %}
[🔝back to top]()

## Model Management
{% for paper in site.data.publications %}
{%if paper.Main_Topic == "Model Management"%}
<p markdown='1'> - {{paper.Authors}} ({{paper.Year}}). [{{paper.Title}}](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22{{paper.Title}}%22&btnG=). {{paper.venue}}</p>
{% endif %}
{% endfor %}
[🔝back to top]()

## Lifecycle Management
{% for paper in site.data.publications %}
{%if paper.Main_Topic == "Lifecycle Management"%}
<p markdown='1'> - {{paper.Authors}} ({{paper.Year}}). [{{paper.Title}}](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22{{paper.Title}}%22&btnG=). {{paper.venue}}</p>
{% endif %}
{% endfor %}
[🔝back to top]()

## Data Management

{% for paper in site.data.publications %}
{%if paper.Main_Topic == "Data Management"%}
<p markdown='1'> - {{paper.Authors}} ({{paper.Year}}). [{{paper.Title}}](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22{{paper.Title}}%22&btnG=). {{paper.venue}}</p>
{% endif %}
{% endfor %}

[Delft University of Technology]: https://www.tudelft.nl
[MSc in Computer Science – Software Technology]: https://www.tudelft.nl/onderwijs/opleidingen/masters/cs/msc-computer-science/

[1st Workshop on AI Engineering – Software Engineering for AI (WAIN'21)]: https://conf.researchr.org/home/icse-2021/wain-2021
[ICSE2021]: https://conf.researchr.org/home/icse-2021

[Yuanhao Xie]: https://repository.tudelft.nl/islandora/search/author%3A%22Xie%2C%20Yuanhao%22
[Luís Cruz]: https://luiscruz.github.io/
[Petra Heck]: https://fontysblogt.nl/author/petraheck/
[Jan Rellermeyer]: https://www.tudelft.nl/ewi/over-de-faculteit/afdelingen/software-technology/distributed-systems/people/jan-rellermeyer/

