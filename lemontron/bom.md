---
layout: guide
title: Order the parts
header_title: BOM
kofi: true
thumbnail: /assets/guide/intro---print-the-parts.jpg
permalink: /lemontron/bom/
---

This comprehensive list includes all the parts required to assemble a Lemontron 3D printer. Parts that need
trimming, cutting, etc. are marked with MOD.

<div class="paragraph">
    {% include button.html title="Download CSV" icon="cloud_download" link="/lemontron/exports/bom.csv" %}
    {% include button.html title="Tools Needed" icon="carpenter" link="/lemontron/tools-needed/" %}
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

{%- for screw in site.data.screws -%}
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

{% assign screws_price = 0 %}
{%- for screw in site.data.screws -%}
{%- assign screws_price = screws_price | plus: screw.total -%}
{%- endfor -%}

## Screws (${{screws_price}})

These {{site.data.screws | size}} screws are all that are needed to assemble a Lemontron. This screw list is subject to further optimization.

{% include screws_list.html %}

The **NEW** badge is for current owners of a [JourneyMaker](/lemontron/lemontron-journeymaker-origins) who wish to
convert it to a
Lemontron. The cost for the **NEW** parts is **${{total_new}}**, plus another [stepper motor](/lemontron/bom/stepper).
If you're converting a JourneyMaker, you can re-use your entire tool head, so you don't need to buy
the [positron one](/lemontron/bom/hotend) but it's a big upgrade.

## Total: **${{total_price}}**