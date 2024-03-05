---
layout: page
title: Servers
subtitle: A list of community servers
---

# Team Fortress 2

| Server Name 	| Address 	                    | Quick Connect                                              	| Owner 	|
|-------------	|---------	                    |------	                                                        |-------	|
| MindlessTux Testing Grounds - TF2          |  ares.mindlesstux.com:27015 	| [Click Here](steam://connect/ares.mindlesstux.com:27015)     	    | [MindlessTux](https://steamcommunity.com/id/mindlesstux/)      	|
| MindlessTux Testing Grounds - Balloon Race          |  ares.mindlesstux.com:27016 	| [Click Here](steam://connect/ares.mindlesstux.com:27016)     	    | [MindlessTux](https://steamcommunity.com/id/mindlesstux/)      	|

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
            <td>{{ commserv.address }} [🔗](steam://connect/{{ commserv.address }})</td>
            <td>[{{ commserv.owner_name }} ]({{ commserv.owner_steamprofile }})</td>
        </tr>
    {% endfor %}
    </tbody>
</table>
{% endfor %}