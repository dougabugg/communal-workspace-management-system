# communal-workspace-management-system
An application for managing a communal workspace

# Project goals
Currently, the makerspace I'm a part of manages communication via Slack, and collects member dues via a managed credit card payment processor web app. Ideally, we would have an "auxilary" database that organizes all of our members, tracks various resource utilization (heat, power, building access), and makes it simple to add and remove members from our payment processor. Slack is great for communicating between members, but there's a lot of automation technology and services that our organization would benefit from, and that we either have to build into Slack (via a bot or APIs) or just create from scratch (hence this repo).

I think a good limit on the scope is security; sensitive data (private member info, credit card payments, etc) shouldn't be directly handled or stored. Best not to make this application a vector for exploitation by reducing the potential reward for breaking in. If the system is infiltrated remotely, the worst that should happen is the lights are kept on over night, or data is corrupted that can easily be restored from a backup. For example, if an adversary attempts to turn on the furnace/heat during the summer, there should be an offline failsafe mechanism in place that says "hey, it's 80 deg F in here, cut power to furnace and open a window", that cannot be overriden from the internet connected system.
