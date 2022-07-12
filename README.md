# Ansible Role: MaSc

Mit dieser Ansible Role lässt sich aus der [MaSc-Software](http://kv-it-gmbh.de/masc/)
eine App für macOS bauen (vorbereitet für MaSc-Version 7.2).

## Voraussetzungen

Folgende Software muss auf dem Mac installiert sein, auf dem die App gebaut
werden soll:

- das Java-Runtime-Environment OpenJDK 17.0.x (Installationspakete sind bei
  [Adoptium](https://adoptium.net/de/) verfügbar)
- die App [Keka](http://www.kekaosx.com/de/)
- Ansible, z.B. über [Homebrew](https://brew.sh/index_de) mit dem Befehl `brew install ansible`
- `git` (z.B. über die Commandline-Tools von Xcode)

## An die Arbeit

Vorher muss die Variable `masc_jre_dir` in `site.yml` angepasst werden, sodass
diese auf das "Home"-Verzeichnis des entpackten / installierten
Java-Runtime-Environment zeigt.
Danach:

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
