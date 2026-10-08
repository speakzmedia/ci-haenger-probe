# ci-haenger-probe

Probe-Repo für [speakz#203](https://github.com/speakzmedia/speakz/issues/203). Hier laufen nur Testläufe für den Wächter `ci-haenger-abbrechen` in speakz:

- `freigabe.yml` wartet an `probe-freigabe`, die einen Reviewer hat. Der Wächter darf diesen Lauf nie anfassen.
- `haengt.yml` wartet an `probe-haengt`. Während er wartet, wird dort der Reviewer entfernt: dann steht er an einer Umgebung ohne Reviewer, wie die drei sdrs-Läufe vom 07.10.2026.
- `schlange.yml` hat eine Concurrency-Gruppe auf Workflow-Ebene; der zweite Lauf zeigt, welchen Status GitHub einem wartenden Lauf gibt.

Nichts hier wird ausgeliefert.
