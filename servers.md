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
Servers:

| Server Name   | Address    | Quick Connect   | Owner   |
|:-------------	|:---------  |:--------------- |:------- |
{% for commserv in game.community_servers %}
| {{ commserv.name }} | {{ commserv.address }} | = | [{{ commserv.owner_name }} ]({{ commserv.owner_steamprofile }}) |
{% endfor %}

{% endfor %}