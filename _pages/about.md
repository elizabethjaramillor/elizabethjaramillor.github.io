---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
# Elizabeth Jaramillo-Rojas

I am a Ph.D. candidate in Economics at Northwestern University. My research focuses on development, the economics of crime, and labor economics, with a particular interest in labor markets in developing countries, education, and the role of public policies in improving the lives of the poor.

I hold a MSc in Econometrics and Mathematical Economics from Tilburg University, a MA in Economics, a BSc in Industrial Engineering, and a BS in Economics from Universidad de los Andes. Previously, I worked as a Research Fellow at the Inter-American Development Bank.

You can contact me at [ejaramillo@u.northwestern.edu](mailto:ejaramillo@u.northwestern.edu), and find my CV [here](/files/CV1.pdf).

---

## Research

### Job Market Paper
**Beyond Recipients: Sibling Spillovers of College Financial Aid**  
<a href="/files/jmp_file.pdf" target="_blank" rel="noopener">PDF</a>
{%- comment -%} Add slides/BibTeX if you have them {%- endcomment -%}
{%- if site.static_files | where: "path", "/files/jmp_slides.pdf" | size > 0 -%} · <a href="/files/jmp_slides.pdf" target="_blank" rel="noopener">Slides</a>{%- endif -%}
{%- if site.static_files | where: "path", "/files/jmp.bib" | size > 0 -%} · <a href="/files/jmp.bib" download>BibTeX</a>{%- endif -%}

<details>
  <summary><em>Abstract</em></summary>
  <!-- 5–7 line abstract here -->
</details>

---

### Working Papers & Publications
{%- assign pubs_sorted = site.publications | sort: "date" | reverse -%}
{%- if pubs_sorted and pubs_sorted.size > 0 -%}
{%- for pub in pubs_sorted -%}
- **{{ pub.title }}**  
  {%- if pub.authors -%}{{ pub.authors }}.{%- endif -%}
  {%- if pub.venue -%} <em>{{ pub.venue }}</em>{%- endif -%}
  {%- if pub.date -%} {{ pub.date | date: "%Y" }}{%- endif -%}
  {%- if pub.paperurl -%} · <a href="{{ pub.paperurl }}" target="_blank" rel="noopener">PDF</a>{%- endif -%}
  {%- if pub.doi -%} · <a href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI</a>{%- endif -%}
  {%- if pub.slides -%} · <a href="{{ pub.slides }}" target="_blank" rel="noopener">Slides</a>{%- endif -%}
  {%- if pub.code -%} · <a href="{{ pub.code }}" target="_blank" rel="noopener">Code</a>{%- endif -%}
  {%- if pub.abstract -%}
  <details><summary>Abstract</summary>
  {{ pub.abstract }}
  </details>
  {%- endif -%}
{%- endfor -%}
{%- else -%}
_(I’ll list working papers here once they’re added to `_publications/`.)_
{%- endif -%}

---

## Teaching
{%- assign classes_sorted = site.teaching | sort: "date" | reverse -%}
{%- if classes_sorted and classes_sorted.size > 0 -%}
<table>
  <thead>
    <tr>
      <th>Course</th>
      <th>Term</th>
      <th>Role</th>
      <th>Materials</th>
    </tr>
  </thead>
  <tbody>
  {%- for c in classes_sorted -%}
    <tr>
      <td>{{ c.title }}</td>
      <td>
        {%- if c.semester -%}{{ c.semester }}{%- endif -%}
        {%- if c.year %} {{ c.year }}{%- endif -%}
      </td>
      <td>{{ c.role | default: c.type }}</td>
      <td>
        {%- if c.url -%}<a href="{{ c.url }}" target="_blank" rel="noopener">Syllabus</a>{%- endif -%}
        {%- if c.materials -%}
          {%- if c.url %} · {%- endif -%}
          <a href="{{ c.materials }}" target="_blank" rel="noopener">Materials</a>
        {%- endif -%}
      </td>
    </tr>
  {%- endfor -%}
  </tbody>
</table>
{%- else -%}
_(I’ll list teaching here once items are in `_teaching/`.)_
{%- endif -%}

---

## Talks & Media (optional)
{%- assign talks_sorted = site.talks | sort: "date" | reverse -%}
{%- if talks_sorted and talks_sorted.size > 0 -%}
{%- for t in talks_sorted -%}
- **{{ t.title }}**, {{ t.event }} — {{ t.date | date: "%b %Y" }}
  {%- if t.location %} ({{ t.location }}){%- endif -%}
  {%- if t.url %} · <a href="{{ t.url }}" target="_blank" rel="noopener">Details</a>{%- endif -%}
  {%- if t.slides %} · <a href="{{ t.slides }}" target="_blank" rel="noopener">Slides</a>{%- endif -%}
  {%- if t.video %} · <a href="{{ t.video }}" target="_blank" rel="noopener">Video</a>{%- endif -%}
{%- endfor -%}
{%- else -%}
_(Add items to `_talks/` to show them here.)_
{%- endif -%}

---

## Contact
You can contact me at <a href="mailto:ejaramillo@u.northwestern.edu">ejaramillo@u.northwestern.edu</a>.  
CV: <a href="/files/CV1.pdf" target="_blank" rel="noopener">PDF</a>
