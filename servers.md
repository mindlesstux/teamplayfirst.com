---
layout: page
title: Servers
subtitle: A list of community servers
---

# Team Fortress 2

| Server Name 	| Address 	                    | Quick Connect                                              	| Owner 	|
|-------------	|---------	                    |------	                                                        |-------	|
| ASDF          |  ares.mindlesstux.com:27015 	| [Click Here](steam://connect/206.191.148.46:27016)     	    | [MindlessTux](https://steamcommunity.com/id/mindlesstux/)      	|

{% for game in site.data.servers %}
# {{ game.shorthand }}, {{ game.game_name }}

| Server Name   | Address    | Quick Connect   | Owner   |
|:-------------	|:---------  |:--------------- |:------- |
{% for commserv in game.community_servers %}
| {{ commserv.name }} | {{ commserv.address }} | = | [{{ commserv.owner_name }} ]({{ commserv.owner_steamprofile }}) |
{% endfor %}

{% endfor %}