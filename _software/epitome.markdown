---
layout: page
title: epitome
description: Prediction of epigenetic events using chromatin accessibility
img: /assets/project_img/epitome.png
importance: 2
---

Epitome leverages chromatin accessibility (either DNase-seq or ATAC-seq) to predict epigenetic events in a novel cell type of interest.
      Such epigenetic events include transcription factor binding sites and histone modifications.
      Epitome computes chromatin accessibility similarity between ENCODE cell types and the novel cell type, and uses this information
      to transfer known epigentic signal to the novel cell type of interest.

You can view and install the tool from [GitHub](https://github.com/YosefLab/epitome).

<br>
<br>

<h3 class="year">Relevant publications</h3><hr>

{% for paper in site.data.publications %}

{% if paper.epitome == true %}
<div id = "{{ paper.title | replace: ' ', '-' | remove: '.' }}" class="clearfix" width="100%" style="padding-top: 5px; padding-bottom: 25px; clear: both;">
<div valign="top" style="overflow: hidden">
  <b>{{paper.title}}</b><br>
  {{paper.authors | markdownify | remove: '<p>' | remove: '</p>'}}<br>
  <i>{{paper.details | markdownify | remove: '<p>' | remove: '</p>'}}</i>
  , {{paper.year}}<br>
  {% if paper.openaccess %}<i class="ai ai-open-access ai-fw"></i> <a href="{{paper.openaccess}}" target="_blank">Open Access</a><br>{% endif %}
  {% if paper.file %}<i class="far fa-file-alt fa-fw"></i> <a href="{{ paper.file | prepend: '/assets/publications/' | prepend: site.baseurl | prepend: site.url }}" target="_blank">{{paper.filetype}}</a><br>{% endif %}
  {% if paper.pmcid %}<i class="fas fa-landmark fa-fw"></i> <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/{{paper.pmcid}}" target="_blank">PubMed Central {{paper.pmcid}}</a><br>{% endif %}
  {% if paper.contentshare %}<i class="fas fa-door-open fa-fw"></i> <a href="{{paper.contentshare}}" target="_blank">Content Sharing link</a><br>{% endif %}
  {% if paper.doi %}<i class="ai ai-doi ai-fw"></i> <a href="https://doi.org/{{paper.doi}}" target="_blank">{{paper.doi}}</a><br>{% endif %}
  {% if paper.github %}<i class="fab fa-github fa-fw"></i> <a href="{{paper.github}}" target="_blank">GitHub</a><br>{% endif %}
  {% if paper.biorxiv %}<i class="ai ai-biorxiv ai-fw"></i> <a href="{{paper.biorxiv}}" target="_blank">bioRxiv preprint</a><br>{% endif %}
  {% if paper.arxiv %}<i class="ai ai-arxiv ai-fw"></i> <a href="{{paper.arxiv}}" target="_blank">arXiv preprint</a><br>{% endif %}
  {% if paper.preregistered %}<i class="ai ai-preregistered ai-fw"></i> <a href="{{paper.preregistered}}" target="_blank">Preregistration</a><br>{% endif %}
  {% if paper.opendata %}<i class="ai ai-open-data ai-fw"></i> <a href="{{paper.opendata}}" target="_blank">Open Data</a><br>{% endif %}
  {% if paper.openmaterials %}<i class="ai ai-open-materials ai-fw"></i> <a href="{{paper.openmaterials}}" target="_blank">Reproducibility code</a><br>{% endif %}
  {% if paper.newsandviews %}<i class="ai ai-conversation ai-fw"></i> <a href="{{paper.newsandviews}}" target="_blank">News and Views</a><br>{% endif %}
    </div>
</div>

{% endif %}
{% endfor %}
