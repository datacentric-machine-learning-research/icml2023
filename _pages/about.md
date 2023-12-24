---
layout: about
title: about
permalink: /
description: Data-centric Machine Learning Research (DMLR) Workshop at ICLR 2024 (May 11 in Vienna, Austria)

profile:
  align: #right
  image: #prof_pic.jpg

news: true  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---
<!---
add
https://mlcommons.org/working-groups/research/dmlr/
-->

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

<br>

### Harnessing Momentum for Science

This is the fourth edition of highly successful workshops focused on data-centric AI, following the success of the Data-Centric AI workshop at NeurIPS 2021, ICML 2022, and ICML 2023.

**AI for science:** Unlike general AI, AI for Science uses AI to tackle unique scientific challenges, uncover rare
phenomena, deepen our understanding of scientific domains, and accelerate discoveries. The traditional model-
centric AI approach primarily focuses on algorithmic improvements and often overlooks the foundational role of
data. This is particularly problematic in scientific contexts where there are strong emphases on both prediction
from and explanation of data. In large science projects and missions that produce vast amounts of data (e.g., at CERN, NASA), efficient data-centric AI frameworks are essential for maximizing the potential of expensive experiments and missions. In contrast, biomedical research surfaces different data-centric AI issues surrounding sparsity (e.g., to understand OOD cases, estimate causal effects), privacy, and fairness. The significance of a data-centric AI framework in science is manifold:
* Scientific research is inherently data-driven.
* The integrity of AI systems is intrinsically tied to the quality of their training data. The high stakes in science leave no room for errors due to poor data. For scientists to trust AI systems, data quality, including precise labeling and comprehensive coverage, is vital.
* The vastness of scientific data demands robust data management for consistent future model evaluations.
* Ethical considerations, such as data privacy, biases, and diverse representation, are central to scientific re-
search.
* Science domain experts provide insights that models alone cannot, ensuring data aligns with scientific objec-
tives and bolsters research reliability.
* There is a need for strong norms around rigorous, data-driven machine learning akin to those surrounding
mathematical and statistical modeling.

This workshop aims to showcase the latest research in the area of AI for science. By showcasing these breakthroughs and fostering collaboration, it seeks to break down the research barriers between AI and science. Our ultimate goal is to cultivate a collaborative environment that brings together a diverse array of researchers, practitioners, domain experts, data and platform providers, and engineers, all of whom are tackling pressing data-related challenges in science research and application.

**Topics will include, but are not limited to:**
* Data collection and benchmarking techniques
* Data governance frameworks for ML
* Impact of data bias, variance, and drifts
*	Role of data in foundation models: pre-training, prompting, fine-tuning
*	Optimal data for standard evaluation framework in the context of changing model landscape
*	Domain specific data issues
*	Data-centric explainable AI
* Data-centric approaches to AI alignment
* Active learning, Data cleaning, acquisition for ML

**Modality: hybrid**

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

DMLR open community

We organize workshops, maintain a journal, partner with UN organizations for public good data sourcing and run a formal working group at MLC to advance infrastructure projectsJournal

Many of the Organized by members of the DMLR working group at [MLCommons](https://mlcommons.org/working-groups/research/dmlr/)


<!-- {% if page.news %}
  {% include news.html %}
{% endif %} -->

<!-- {% twitter https://twitter.com/icmlconf maxwidth=1000 limit=5 %} -->
