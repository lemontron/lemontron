---
layout: guide
title: BOM
thumbnail: /assets/guide/intro---print-the-parts.jpg
---

{% include printer-context.html %}
{% assign csv_link = '/' | append: slug | append: '/exports/bom.csv' %}

This comprehensive list includes all the parts required to assemble a Lemontron 3D printer. Parts that need
trimming, cutting, etc. are marked with MOD.

<div class="paragraph">
    {% include button.html title="Download CSV" icon="cloud_download" link=csv_link %}
    {% include button.html title="Tools Needed" icon="carpenter" link="/tools-needed/" %}
</div>

{%- assign total_new = 0 -%}
{%- assign bom_sorted = site.bom | sort: "url" -%}
{%- assign bom_required = bom_sorted | where: "optional", false -%}

{%- assign total_price = 0 -%}
{%- for bom in bom_required -%}
{%- assign total_price = total_price | plus: bom.total -%}

{%- if bom.new -%}
{%- assign total_new = total_new | plus: bom.total -%}
{%- endif -%}
{%- endfor -%}

{%- for screw in screws -%}
{%- assign total_price = total_price | plus: screw.total -%}
{%- endfor -%}

## Positron Parts

{% assign positron = bom_required | where: "category", "Positron" %}
{% include bom_list.html items=positron %}

## Hardware

{% assign hardware = bom_required | where: "category", "Hardware" %}
{% include bom_list.html items=hardware %}

## Electronics

{% assign electronics = bom_required | where: "category", "Electronics" %}
{% include bom_list.html items=electronics %}

## Optional Upgrades

{% assign bom_optional = bom_sorted | where: "optional", true %}
{% include bom_list.html items=bom_optional %}

## Screws (${{screws_price}})

There are only {{screws | size}} types of screws used.

{% include screws_list.html %}

The **NEW** badge is for current owners of a [JourneyMaker](/lemontron-rev-a/lemontron-journeymaker-origins) who wish to
convert it to a
Lemontron. The cost for the **NEW** parts is **${{total_new}}**, plus another [stepper motor](/lemontron-rev-a/bom/stepper).
If you're converting a JourneyMaker, you can re-use your entire tool head, so you don't need to buy
the [positron one](/lemontron-rev-a/bom/hotend) but it's a big upgrade.

## Total: **${{total_price}}**