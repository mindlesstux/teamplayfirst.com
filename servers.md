---
layout: page
title: Servers
subtitle: A list of community servers
---

{% for game in site.data.servers %}
# {{ game.game_name }}

<table>
    <thead>
        <tr>
            <th>Server Name</th>
            <th>Address</th>
            <th>Owner</th>
        </tr>
    </thead>
    <tbody>
    {% for commserv in game.community_servers %}
        <tr>
            <td>{{ commserv.name }}</td>
            <td>{{ commserv.address }} <a href="steam://connect/{{ commserv.address }}">[🔗]</a></td>
            <td><a href="{{ commserv.owner_steamprofile }}" target="_blank">{{ commserv.owner_name }}</a></td>
        </tr>
    {% endfor %}
    </tbody>
</table>
{% endfor %}