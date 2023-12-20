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
This is the fourth edition of highly successful workshops focused on data-centric AI, following the success of the Data-Centric AI workshop at NeurIPS 2021, ICML 2022, and ICML 2023.

**AI for science** uses AI to tackle unique scientific challenges, uncover rare phenomena, deepen our understanding of scientific domains, and accelerate discoveries. The traditional model-centric AI approach primarily focuses on algorithmic improvements and often overlooks the foundational role of data. This is particularly problematic in scientific contexts where there are strong emphases on both prediction from and explanation of data. In science, ML pipelines are often interwoven with the inputs and outputs of theoretical models which depend on robust data and reliable model outputs. In large science projects and missions that produce vast amounts of data, efficient data-centric AI frameworks are essential for maximizing the potential of expensive experiments and missions. This being said, the integrity of AI systems is intrinsically tied to the quality of their training data. The high stakes in science leave no room for errors due to poor data. For scientists to trust AI systems, data quality, including precise labeling and comprehensive coverage, is vital.

This workshop aims to showcase the latest research in the area of AI for science. By showcasing these breakthroughs and fostering collaboration, it seeks to break down the research barriers between AI and science.

### Topics will include, but not limited to:
* Data collection and benchmarking techniques
* Data governance frameworks for ML
* Impact of data bias, variance, and drifts
*	Role of data in foundation models: pre-training, prompting, fine-tuning
*	Optimal data for standard evaluation framework in the context of changing model landscape
*	Domain specific data issues
*	Data-centric explainable AI

Bridging the gap between seasoned expertise and fresh perspectives, our keynote/invited/tutorial talks will showcase the work of established, mid and early-career researchers. This well-rounded mix promises a vibrant exchange of ideas and fosters dynamic advancements in the field.

## Awards
A few selected exceptional research papers from DMLR workshop 2024 will be invited to contribute to the **DMLR journal**; the latest member of the JMLR family, aiming to provide a top archival venue for high-quality scholarly articles focused on the data aspect of machine learning research. The top submissions to the DMLR workshops will be invited to submit extended versions of their papers to the DMLR journal.


## Student Scholarship

*tba*

<!-- {% if page.news %}
  {% include news.html %}
{% endif %} -->

<!-- {% twitter https://twitter.com/icmlconf maxwidth=1000 limit=5 %} -->
