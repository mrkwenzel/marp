Mastodon Ansible Rollout Playbook
=================================

(Für die Deutsche Version [hier klicken](README.de.md))

This playbook was used to create the [WenzIT Mastodon instance](https://mastodon.wenzit.de)

It is only created to initially install an instance. Updates are currently not covered.

This rollout repository will help you to setup your own small Mastodon instance at Hetzner Cloud.
Currently no other provider is in planning, but may be added in future releases.

Prerequisites
-------------
- Hetzner Cloud Instance CX21
- Domain with set up A record to upper instance (e.g. at www.domainssaubillig.de)
- SendGrid account setup with upper domain
- Python 3.10

Some YouTube links might follow to explain how to setup.

Run
---
Venv is recommended.

Copy `inventory.yaml.example` to `inventory.yaml` and fix the hostname.
Copy `vars.yaml.example` to `vars.yaml` and fix emtpy fields.
Copy `vault.yaml.example` to `vault.yaml` and fix emtpy fields. Make sure you secure this file with `ansible-vault`.

```shell
#> python3 -m venv venv
#> pip install -r requirements.txt
#> ansible-playbook -i inventory/prod -u root site.yaml
```

Relays
------
```
https://mastodon-relay.moew.science/inbox
https://relay.101010.pl/inbox
https://relay.beckmeyer.us/inbox
https://relay.chocoflan.net/inbox
https://relay.fedibird.com/inbox
https://relay.fedi.agency/inbox
https://relay.homunyan.com/inbox
https://relay.intahnet.co.uk/inbox
https://relay.libranet.de/inbox
https://relay.freespeech.club/inbox
https://relay.mistli.net/inbox
https://relay.retronerd.at/inbox
https://relay.toot.yukimochi.jp/inbox
```