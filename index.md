---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: LEZ Model Documentation
---

The ICCT’s LEZ model is a Python-based tool designed to assess the impact of low emission zone (LEZ) implementations on fleet emissions in cities. Fleet-average emission factors (EFs), in terms of g/km, can be evaluated for local pollutants such as particulate matter (PM) and nitrogen oxides (NOx), as well as greenhouse gases (GHG), both for Tank-to-Wheel (TTW) and Well-to-Wheel (WTW) emissions. The model includes a turnover module that projects future fleet evolution, incorporating varying powertrain shares for future sales and natural vehicle retirements. The LEZ model allows for the evaluation of impacts on the fleet and average EFs across different scenarios of LEZ implementation and vehicle owner response (section Consumer-response Modelling), enabling easy comparison of relative emission reductions due to LEZ policies.

The LEZ model was first developed in 2020 by Caleb Braun, Yoann Bernard, and Josh Miller to inform the [TRUE publication "Impacts of the Paris low-emission zone and implications for other cities"](https://theicct.org/publication/impacts-of-the-paris-low-emission-zone-and-implications-for-other-cities/). Version 2.1 was developed in 2022-2023 by Jakob Schmidt, Rohit Nepali, Kaylin Lee, and Yoann Bernard.

## Versions

The LEZ model is under continuing development. Documentation of all versions since v2.1 can be found here.

{% assign pages = site.pages | sort: "title" | reverse %}
{% for page in pages %}
{% if page.dir contains '/versions/' and page.title contains 'LEZ v'%}
<li><a class="page-link" href="{{ page.url | relative_url }}">{{ page.title | escape }}</a></li>
{% endif %}
{% endfor %}
