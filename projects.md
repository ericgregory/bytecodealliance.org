---
layout: default
permalink: /projects
title: Projects
---

<section>
    <div class="container w-container">
        <div class="width-container" markdown="1">

## Bytecode Alliance Projects

An essential way the Bytecode Alliance pursues its mission is to identify and support projects that align with its vision for the evolution of WebAssembly.  Hosting such projects allows the Alliance to contribute greater attention and technical oversight both directly and through collaborative participation from its member organizations.  

Requirements for and recognition of adopted projects are managed by the Alliance's Technical Steering Committee per its [charter](https://github.com/bytecodealliance/governance/blob/main/TSC/charter.md), and approved by the Board. A complete [repository of active and archived Bytecode Alliance projects](https://github.com/bytecodealliance/governance/tree/main/projects) is maintained on GitHub. 

## Our active projects

<div>
    {% comment %}Assign projects from list in _data/projects.yml with active value "true" to active variable{% endcomment %}
    {% assign active = site.data.projects | where:"active", "true" %}
    {% comment %}Loop through projects in active variable{% endcomment %}
    {% for project in active %}
    <div>
            <div>
                <h3><a href="{{ project.repo }}">{{ project.name }}</a></h3>
                  {{ project.description }}
                  <p></p>
                  <ul class="project-list"><li><b>GitHub</b>: <a href="{{ project.repo }}">{{ project.repo }}</a></li>
                  {% if project.site %}
                     <li><b>Website</b>: <a href="{{ project.site }}">{{ project.site }}</a></li>
                  {% endif %}
                  {% if project.docs %}
                     <li><b>Docs</b>: <a href="{{ project.docs }}">{{ project.docs }}</a></li>
                  {% endif %}
                  </ul><br>
            </div>
            {% endfor %}
    </div>


<section>
    <div class="container w-container">
        <div class="width-container" markdown="1">

## Project security

The Bytecode Alliance maintains an active security management and monitoring posture across all of its projects.  If you think you have found a security issue in a Bytecode Alliance project or would like to know more, please consult our [Security Policy]({{ site.baseurl }}/security) for details on reporting, disclosure, and remediation.

</div>
</div>
</section>
