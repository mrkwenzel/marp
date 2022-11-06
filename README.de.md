Mastodon Ansible Rollout Playbook
=================================

Dieses Rollout Repository soll dir helfen eine kleine Mastodon Instanz auf Hetzner Cloud zu hosten.

Dieses Playbook wurde genutzt um die [WenzIT Mastodon Instanz](https://mastodon.wenzit.de) zu erzeugen.

Es ist nur zur initialen Installation einer Instanz geschrieben worden. Updates sind aktuell nicht implementiert.

Aktuell ist kein anderer Provider geplant, aber könnte in zukünftigen Releases hinzugefügt werden.

Voraussetzungen
---------------
- Hetzner Cloud Instance CX21
- Domain mit A Record auf oben genannte Instanz (z.B. bei www.domainssaubillig.de)
- SendGrid Account eingerichtet mit oben genannter domain
- Python 3.10

Ein paar YouTube Videos könnten folgen um zu erklären wie man die einzelnen Teile verwendet.

Ausführen
---------
Venv ist epfohlen.

Kopiere `inventory.yaml.example` nach `inventory.yaml` und fülle den Hostname.
Kopiere `vars.yaml.example` nach `vars.yaml`und fülle die leeren Felder.
Kopiere `vault.yaml.example` nach `vault.yaml` und fülle die leeren Felder. Am besten sicherst du diese Datei mit `ansible-vault`.

```shell
#> python3 -m venv venv
#> pip install -r requirements.txt
#> ansible-playbook -i inventory/prod -u root site.yaml
```

Relays
------
Immer aktuell in der [Englischen README.md](README.md)