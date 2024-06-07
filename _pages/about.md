---
layout: about
title: about
permalink: /
description:

profile:
  align: #right
  image: #prof_pic.jpg

news: true  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---

### ICML 2024
* [Call for papers](https://dmlr.ai/cfp-icml24/)
* [Program](https://dmlr.ai/program/)
* [Submission portal](https://openreview.net/group?id=ICML.cc/2024/Workshop/DMLR)

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/time.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    A timeline of inflection points in the development of data-centric ideas. See the editorial <a href="https://openreview.net/forum?id=2kpu78QdeE">DMLR: Data-centric Machine Learning Research -- Past, Present and Future</a> for more details.
</div>
<br>


# Speakers
<div class="projects grid">

  {% assign sorted_speakers = site.speakers | sample:100 %}
  {% for speaker in sorted_speakers %}
  <div class="grid-item">
    {% if speaker.redirect %}
    <a href="{{ speaker.redirect }}" target="_blank">
    {% else %}
    <a href="{{ speaker.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if speaker.img %}
        <img src="{{ speaker.img | relative_url }}" alt="speaker thumbnail">
        {% endif %}
        <div class="card-body">
          <h3 class="card-title">{{ speaker.name }}</h3>
          <p class="card-title">{{ speaker.affiliation }}</p>
          <p class="card-text">{{ speaker.minibio }}</p>
          <br/>
          <div class="row ml-1 mr-1 p-0">
            {% if speaker.mail %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Email">
                <a href="mailto:{{ speaker.mail | encode_email }}"><i class="fas fa-envelope"></i></a>
              </div>
            </div>
            {% endif %}
            {% if speaker.website %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Website">
                <a href="{{ speaker.website }}" target="_blank"><i class="fas fa-globe"></i></a>
              </div>
            </div>
            {% endif %}
            {% if speaker.twitter %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Twitter">
                <a href="{{ speaker.twitter }}" target="_blank"><i class="fab fa-twitter"></i></a>
              </div>
            </div>
            {% endif %}
            {% if speaker.linkedin %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="LinkedIn">
                <a href="{{ speaker.linkedin }}" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
              </div>
            </div>
            {% endif %}
            {% if speaker.googlescholar %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Google Scholar">
                <a href="{{ speaker.googlescholar }}" target="_blank" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
              </div>
            </div>
            {% endif %}
            {% if speaker.github %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ speaker.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if speaker.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ speaker.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
<br>

### Topics and Theme

This is the fifth edition of highly successful workshops focused on data-centric AI, following the success of the Data-Centric AI workshop at NeurIPS 2021, ICML 2022, ICML 2023, and ICLR 2024.

#### Theme

Large-scale foundation models are revolutionizing machine learning, particularly in vision and language domains. While model architecture received significant attention in the past, recent focus has shifted towards the importance of data quality, size, and diversity, and provenance.  

This workshop aims to highlight cutting-edge advancements in data-centric approaches for large-scale foundation models in new domains, in addition to language and vision, and engage the vibrant interdisciplinary community of researchers, practitioners, and engineers who tackle practical data challenges related to foundation models. By featuring innovative research and facilitating collaboration, it aims to bridge the gap between dataset-centric methodologies and the development of robust, versatile foundation models that are able to work in and across a variety of domains in service of humanity.

#### Topics will include, but are not limited to
* Data sources for large-scale datasets: 
* Construction of datasets from large quantities of unlabeled/uncurated data 
* Model-assisted dataset construction
* Quality signals for large-scale datasets
* Datasets for evaluation
* Datasets for specific applications. 
* Impact of dataset drifts in large-scale models
* Ethical considerations for and governance of large-scale datasets 
* Data curation and HCI
* Submissions to benchmarks such as [DataPerf](https://www.dataperf.org/), [DynaBench](https://dynabench.org/), and [DataComp](https://www.datacomp.ai/)

If you are looking for examples of works previously presented at DMLR, you can find a list of papers [here](https://dmlr.ai/iclr24/accepted/).

An overview of the history and vision behind DMLR, including links to previous keynotes, you can find in our editorial [DMLR: Data-centric Machine Learning Research -- Past, Present and Future](https://openreview.net/forum?id=2kpu78QdeE).

### Awards

A few selected exceptional research papers from DMLR workshop 2024 will be invited to contribute to the **DMLR journal**; the latest member of the JMLR family, aiming to provide a top archival venue for high-quality scholarly articles focused on the data aspect of machine learning research. The top submissions to the DMLR workshops will be invited to submit extended versions of their papers to the DMLR journal.

### Logistics

**Important Dates**

(Time zone: Anywhere on Earth)

* Paper Submission deadline: ~~May 24, 2024~~ May 30, 2024
* Notification of Acceptance: June 17, 2024
* Camera Ready Copy due: Coming Soon

**Session organization: virtual + in-person engagement**

We aim at a discussion-centric workshop to allow for in-depth coverage of state-of-art and work-in-progress
efforts and panel discussion and poster presentation along the data lifecycle in machine learning research and
engineering: creation, quality and processing, governance and management/infrastructure.

The workshop will be organized in four components:
* Keynotes and invited talks
* Open panel discussions
* Poster sessions
* Networking sessions


# About DMLR

DMLR is an open, distributed community organizing activities to discuss and advance research in data-centric machine learning.

We organize [workshops and research retreats](https://dmlr.ai/), maintain [a journal](https://data.mlr.press/), and run a [working group at Machine Learning Commons (MLC)](https://mlcommons.org/working-groups/research/dmlr/) to support infrastructure projects.

You can find more details about the scope and history of our activities in the editorial [Data-centric Machine Learning Research -- Past, Present and Future](https://openreview.net/forum?id=2kpu78QdeE).



<!-- {% if page.news %}
  {% include news.html %}
{% endif %} -->

<!-- {% twitter https://twitter.com/icmlconf maxwidth=1000 limit=5 %} -->
