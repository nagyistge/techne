---
title: Loading Spinner
keywords: loading, spinner
sidebar: components-sidebar
toc: false
permalink: loading-spinner.html
folder: components
summary:
---

<br>
Toggle the `aria-hidden` attribute to hide/show the spinner.

{% capture default %}
<div class="tn-spinner" aria-hidden="false" aria-label="Loading">
    <div></div>
</div>
{% endcapture %}

{% include display-component.html component=default %}

<br>

## [aria-busy="true"]
The spinnner is most often used within another component to indicate the loading state. Any container (even `ui-, app-, and page-level`) can be "activated" by setting `aria-busy="true"`.

The spinner should be included inside the container. Its visibility can be toggled in relation to the `aria-busy` attribute. They should always be opposites, i.e, if currently loading, `section[aria-busy="true"], .tn-spinner[aria-hidden="false"]`, once the content is loaded, toggle to false and true respectively.

{% capture aria %}
<div class="tn-panel" aria-busy="true">
    <div class="tn-spinner" aria-hidden="false" aria-label="Loading">
        <div></div>
    </div>
    <div class="tn-panel__header">
        <h1 class="tn-panel__title">Lorem ipsum</h1>
    </div>
    <!-- Loaded content goes here -->
    <div class="tn-panel__footer">
        <p><em>Etiam pulvinar turpis sed velit porttitor vel adipiscing velit fringilla.</em></p>
    </div>
</div>
{% endcapture %}

{% include display-component.html component=aria %}
