---
layout: "default"
title: "betűk"
description: "arab nyelv"
permalink: "/arabisztika/arab-nyelv/betuk"
---
<!--
This Source Code Form is subject to the terms of the Mozilla Public
License, v. 2.0. If a copy of the MPL was not distributed with this
file, You can obtain one at http://mozilla.org/MPL/2.0/.
-->

<style>
    td {
        font-size: 12pt;
    }
    .arabic {
        font-size: 20pt;
    }
    .translit {
        font-size: 14pt;
    }
</style>

# betűk

- Wikipedia: <a href="https://en.wikipedia.org/wiki/Arabic_alphabet" target="_blank">Arabic alphabet</a>

<table>
<tbody>
    <tr>
        <th>betű</th>
        <th>nap / hold</th>
        <th>név</th>
        <th>átírás</th>
        <th>Unicode</th>
    </tr>
    {% for letter in site.data.arabisztika.arabic-alphabet %}
    <tr>
        <td class="arabic">{{ letter.arabic }}</td>
        <td>{{ letter.sun_moon }}</td>
        <td>{{ letter.name }}</td>
        <td class="translit">{{ letter.small }} / {{ letter.capital }}</td>
        <td>
            <a href="{{ letter.arabic_utf_link }}" alt="{{ letter.arabic_utf_name }}" target="_blank">arab</a> /
            &nbsp;<a href="{{ letter.small_utf_link }}" alt="{{ letter.small_utf_name }}" target="_blank">kicsi</a> /
            &nbsp;<a href="{{ letter.capital_utf_link }}" alt="{{ letter.capital_utf_name }}" target="_blank">nagy</a>
        </td>
    </tr>
    {% endfor %}
</tbody>
</table>

## további betűk

<table>
<tbody>
    <tr>
        <th>betű</th>
        <th>név</th>
        <th>átírás</th>
        <th>Unicode</th>
    </tr>
    {% for letter in site.data.arabisztika.arabic-chars.letters-other %}
    <tr>
        <td class="arabic">{{ letter.arabic }}</td>
        <td>{{ letter.academic_name }}</td>
        <td class="translit">{{ letter.academic_small }} / {{ letter.academic_capital }}</td>
        <td>
            <a href="{{ letter.arabic_unicode_link }}" alt="{{ letter.arabic_unicode_name }}" target="_blank">arab</a> /
            &nbsp;<a href="{{ letter.academic_small_unicode_link }}" alt="{{ letter.academic_small_unicode_name }}" target="_blank">kicsi</a> /
            &nbsp;<a href="{{ letter.academic_capital_unicode_link }}" alt="{{ letter.academic_capital_unicode_name }}" target="_blank">nagy</a>
        </td>
    </tr>
    {% endfor %}
</tbody>
</table>

## egyéb

<table>
<tbody>
    <tr>
        <th>név</th>
        <th>jel</th>
    </tr>
    {% for item in site.data.arabisztika.arabic-chars.other %}
    <tr>
        <td>{{ item.name }}</td>
        <td class="arabic">{{ item.arabic }}</td>
    </tr>
    {% endfor %}
</tbody>
</table>

## számok

<table>
<tbody>
    <tr>
        <th>nyugati arab</th>
        <th>keleti arab</th>
    </tr>
    {% for number in site.data.arabisztika.arabic-chars.numbers %}
    <tr>
        <td>{{ number.western_arabic }}</td>
        <td class="arabic">{{ number.eastern_arabic }}</td>
    </tr>
    {% endfor %}
</tbody>
</table>

## Unicode

### Arabic

- Range: 0600—06FF
- Number of characters: 256
- <a href="https://unicode-table.com/en/blocks/arabic/" target="_blank">Unicode Table: Arabic</a>

### Arabic Presentation Forms-B

- Range: FE70—FEFF
- Number of characters: 144
- <a href="https://unicode-table.com/en/blocks/arabic-presentation-forms-b/" target="_blank">Unicode Table: Arabic Presentation Forms-B</a>

### Arabic Presentation Forms-A

- Range: FB50—FDFF
- Number of characters: 688
- <a href="https://unicode-table.com/en/blocks/arabic-presentation-forms-a/" target="_blank">Unicode Table: Arabic Presentation Forms-A</a>

### Arabic alphabet

- <a href="https://unicode-table.com/en/alphabets/arab/" target="_blank">Unicode Table: Arabic alphabet</a>

<table>
<tbody>
    <tr>
        <th>isolated form</th>
        <th>final form</th>
        <th>medial form</th>
        <th>initial form</th>
    </tr>
    {% for letter in site.data.arabisztika.arabic-alphabet %}
    <tr>
        <td class="arabic">
            <a href="{{ letter.isolated_utf_link }}" alt="{{ letter.isolated_utf_name }}" target="_blank">{{ letter.isolated }}</a>
        </td>
        <td class="arabic">
            <a href="{{ letter.final_utf_link }}" alt="{{ letter.final_utf_name }}" target="_blank">{{ letter.final }}</a>
        </td>
        <td class="arabic">
            <a href="{{ letter.medial_utf_link }}" alt="{{ letter.medial_utf_name }}" target="_blank">{{ letter.medial }}</a>
        </td>
        <td class="arabic">
            <a href="{{ letter.initial_utf_link }}" alt="{{ letter.initial_utf_name }}" target="_blank">{{ letter.initial }}</a>
        </td>
    </tr>
    {% endfor %}
</tbody>
</table>
