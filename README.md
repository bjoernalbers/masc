# Ansible Role: MaSc

Mit dieser Ansible Role lässt sich aus der [MaSc-Software](http://kv-it-gmbh.de/masc/)
eine App für macOS bauen (getestet mit MaSc Version 6.1).

## Voraussetzungen

Folgende Software muss auf dem Mac installiert sein, auf dem die App gebaut
werden soll:

- ein Java-Runtime-Environment (mindestens Java-Version "1.8.0_172")
- die App [Keka](http://www.kekaosx.com/de/)
- Ansible, z.B. über [Homebrew](https://brew.sh/index_de) mit dem Befehl `brew install ansible`
- git (z.B. über XCode)

## An die Arbeit

1. Lade dir die MaSc-Software von der [offiziellen
   Webseite](http://kv-it-gmbh.de) aus dem Kundenbereich runter.
2. Entpacke die zuvor geladene exe-Datei mit der Keka-App.
3. Installiere die darin enthaltene jar-Datei per Doppelklick in das
   Standardverzeichnis `/Applications`.
4. Klone dieses Repository mit git und wechsele in das Verzeichnis:
   `git clone https://github.com/bjoernalbers/masc && cd masc`
5. Führe das Ansible-Playbook aus: `ansible-playbook site.yml`.

Anschließend sollte im Unterverzeichnis eine pkg-Datei liegen, die du auf einem
Mac installieren kannst.
Fertig :-)

## Copyright

Diese Software ist unter der MIT-Lizenz veröffentlicht.
