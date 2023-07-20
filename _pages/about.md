---
layout: about
title: about
permalink: /
description: Data-centric Machine Learning Research (DMLR) Workshop at ICML 2023 (Saturday, July 29)

profile:
  align: #right
  image: #prof_pic.jpg

news: true  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---

{% include visual.html %}

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
          <h2 class="card-title">{{ speaker.name }}</h2>
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

This is the third edition of highly successful workshops focused on data-centric AI, following the success of the Data-Centric AI workshop at NeurIPS 2021 and DataPerf workshop at ICML 2022. 
Data and operations over data (e.g., cleaning, debugging, curation) have been continually fueling the success of machine learning for decades. While historically the ML community has focused primarily on model development, recently the importance of data quality has attracted intensive interest from the community, including the creation of the NeurIPS dataset and benchmark track, several data-centric AI benchmarks (e.g., DataPerf), and the flourishing of data consortiums such as LAION, the community’s attention has been directed to the quality of data used for ML training and evaluation. The goal of this workshop is to facilitate these essential topics in what we call Data-centric Machine Learning Research, which includes not only datasets and benchmarks, but tooling and governance, as well as fundamental research on topics such as data quality and data acquisition for dataset creation and optimization. Our ultimate goal is to engage the vibrant interdisciplinary community of researchers, practitioners and engineers that tackle practical data problems related to the following list (not exclusive) of topics:
* Benchmarking data collection, data generation, data labeling, data augmentation processes, generalizability of datasets, feature representations, text and image generation models
* Datasets for machine learning research, AI, and AGI
* Data governance, debt and its solutions
* Data bias, variance, uncertainty and its influence to ML
* Active learning, Data cleaning, acquisition for ML
* Data-centric quality evaluation for data benchmarking
* Influence of data benchmarks on ML research
* Data-centric approaches to AI alignment

Data is the primary object of interest underlying all of machine learning. Thus we expect that the topics of the workshop are of great interest to the broader machine learning community and its many specializations that crucially rely on data downstream. We seek to drive progress in addressing these core problems. We will bring together several communities including DataPerf at MLCommons, Data-centric AI, and Dataset 2030 initiatives. A huge amount of innovation — in algorithms, ideas, principles, and tools — is needed to make data-centric AI development efficient and effective. We hope this workshop will help spark innovations. 

The workshop will be organized in four components:
* Keynotes and invited talks: 30 min + 5 min Q&A / talk
* Contributed Papers (spotlight talks+posters): 10 min talk; 1h in person + 30 mins virtual poster
* Open Panel Discussion: open panel about how to facilitate research of data-centric machine learning
research, and how we should establish DMLR 2024 as a new ICML track or a standalone conference.
* The DataPerf Competitions results will be presented, winners of each competition showcase their solutions.
DataPerf Competitions launch March 21, 2023, ranging from dataset selection to cleaning to valuation.
DataPerf (https://dataperf.org/) is a community effort of machine learning researchers, data scientists
and engineers striving to advance data quality research.
* We will publish a position paper at the end of this workshop, inspired by the style of the MLSys position
paper (https://arxiv.org/abs/1904.03257). This paper will be discussed in both open panel and closed
panel discussion, drafted first by the organizing committee, integrated with feedback from the participants,
and with solicited feedback from broader communities before publication.

<!-- {% if page.news %}
  {% include news.html %}
{% endif %} -->

<!-- {% twitter https://twitter.com/icmlconf maxwidth=1000 limit=5 %} -->
