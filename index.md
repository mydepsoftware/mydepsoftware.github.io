---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---


<div>
    {% for item in site.data.navigation %}
    <div>
        <div>
            <div>
                <h3 >{{ item.title }}</h3>
            </div>
            <div>

                <p><a href="{{ item.url}}">{{ item.excerpt }}</a></p>

            </div>
        </div>
    </div>
    {% endfor %}
</div>
