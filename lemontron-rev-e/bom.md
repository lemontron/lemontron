---
layout: documentation
title: BOM
icon: shopping_cart
order: 2
---

This comprehensive list includes all the parts required to assemble a Lemontron Rev E 3D printer. Parts that need
trimming, cutting, etc. are marked with MOD.

{% include printer-context.liquid %}

{%- assign total_new = 0 -%}

{%- assign bom = site.pages | where: "layout", "bom" | where_exp: "item", "item.url contains slug" | sort: "url" -%}

{%- assign total_price = 0 -%}
{%- for item in bom -%}

{%- assign slug = item.url | split: "/" | last -%}
{%- assign library_item = site.data.library[slug] -%}
{%- assign total = library_item.price | multiply: item.qty -%}

{%- assign total_price = total_price | plus: total -%}

{%- if library_item.new -%}
{%- assign total_new = total_new | plus: total -%}
{%- endif -%}

{%- endfor -%}

{%- assign total_price = total_price | plus: printer_screws_price -%}

<div></div>

## Positron Parts

{% assign positron = bom | where_exp: "item", "item.url contains '/positron/'" %}
{% include bom-list.html items=positron %}

## Hardware

{% assign hardware = bom | where_exp: "item", "item.url contains '/hardware/'" %}
{% include bom-list.html items=hardware %}

## Electronics

{% assign electronics = bom | where_exp: "item", "item.url contains '/electronics/'" %}
{% include bom-list.html items=electronics %}

## Optional Upgrades

{% assign bom_optional = bom | where_exp: "item", "item.url contains '/optional/'" %}
{% include bom-list.html items=bom_optional %}

## Screws (${{printer_screws_price}})

There are only {{printer.screws | size}} types of screws used.

{% include screws_list.html %}

The **NEW** badge is for current owners of a [JourneyMaker](/news/journeymaker) who wish to
convert it to a
Lemontron. The cost for the **NEW** parts is **${{total_new}}**, plus
another [stepper motor](/lemontron-rev-e/bom/electronics/stepper/).
If you're converting a JourneyMaker, you can re-use your entire tool head, so you don't need to buy
the [positron one](/lemontron-rev-e/bom/positron/positron-hotend/) but it's a big upgrade.

## Total: **${{total_price}}**

{% assign csv_link = '/' | append: slug | append: '/exports/bom.csv' %}
<div class="paragraph">
    {% include button.liquid title="Download CSV" icon="cloud_download" link=csv_link %}
</div>
