---
# [[@{{citekey}}]]
title: {{title}}
authors: 
{% for type, creators in creators | groupby("creatorType") -%}
{%- for creator in creators -%}
    {%- if creator.name %} - {{creator.name}}  
    {%- else %} - {{creator.firstName}} {{creator.lastName}}  
    {%- endif %}  
{% endfor %} 
{%- endfor %}
year: {{date | format("YYYY")}}
aliases:
    - {{title}}
tags:
---
# {{title}}

>[!summary]
>

## Notes

# Citation

{{bibliography}}


