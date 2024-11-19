---


permalink: /category/
title: Categories
---
<style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    gap: 10px;
    padding: 10px;
  }
  .grid-item {
    background-color: #f4f4f4; /* Adjust the background color */
    border: 1px solid #ccc;   /* Optional border */
    border-radius: 20px;       /* Rounded corners */
    text-align: center;
    padding: 10px;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1); /* Optional shadow */
    transition: transform 0.2s;
    text-decoration: none;
    color: #252A34
  }
  .grid-item:hover {
    transform: scale(1.05); /* Hover effect */
    cursor: pointer;
    text-decoration: none;
  }

  a {
    text-decoration: none
  }

    a:hover {
    text-decoration: none
  }
 
</style>

<!-- {{site.categories}} -->

<div class="grid-container">

{% for category in site.categories %}
<a href = "{{category[0]}}">
<div class="grid-item">
{{category[0]}}
<span>({{ category[1].size }}) </span>
</div>
</a>
{% endfor %}

</div>

