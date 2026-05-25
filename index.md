---
layout: default
title: Home
---
<div class="story-list">
  <h1>Stories</h1>
  <ul>
    {% assign sorted_stories = site.stories | sort: "date" | reverse %}
    {% for story in sorted_stories %}
    <li>
      <a href="{{ story.url | prepend: site.baseurl }}">{{ story.title }}</a>
      <span class="meta">{{ story.date | date: "%B %Y" }}</span>
    </li>
    {% endfor %}
  </ul>
</div>
