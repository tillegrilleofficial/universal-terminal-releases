# Universal Terminal — Downloads

Windows-Installer und Versionsinfo für **Universal Terminal**, ein serielles Terminal für BLE,
Bluetooth Classic, USB und Netzwerk (TCP / Telnet / RFC2217 / SSH).

Dieses Repository enthält **keinen Quellcode** — nur die Auslieferungsdateien.

## Herunterladen

Die aktuelle Version liegt unter **[Releases](../../releases/latest)** als `.msi`.

- Installation **ohne Administratorrechte**, ins Benutzerprofil.
- Eine neuere `.msi` einfach über die alte installieren: sie ersetzt die vorhandene Installation.
  Einstellungen, Makros und Automatisierungen bleiben erhalten (sie liegen unter
  `%APPDATA%\UniversalTerminal`) und werden beim Deinstallieren nicht gelöscht.
- Windows zeigt beim Ausführen unter Umständen eine SmartScreen-Warnung, weil der Installer nicht
  signiert ist. Über *Weitere Informationen → Trotzdem ausführen* lässt sich das bestätigen.

Die Android-Version kommt über Google Play und aktualisiert sich dort selbst.

## `latest.json`

Diese Datei sagt der Windows-App, welche Version aktuell ist. Die App liest sie höchstens **einmal
täglich**, zeigt bei einer neueren Version einen Hinweis mit Link — und lädt **nichts** herunter und
führt nichts aus. Abschalten lässt sich das in der App unter *Einstellungen → Updates*.

```json
{
  "schema": 1,
  "windows": {
    "version": "1.0.2",
    "url": "https://github.com/tillegrilleofficial/universal-terminal-releases/releases/latest",
    "notes_de": "…",
    "notes_en": "…"
  }
}
```

| Feld | Bedeutung |
|---|---|
| `schema` | Formatversion, derzeit `1`. Eine App verweigert eine Datei mit anderer Nummer, statt sie halb zu verstehen. |
| `version` | Neueste Version als `MAJOR.MINOR.PATCH`, zahlenweise verglichen (`1.0.10` > `1.0.9`). |
| `url` | Ziel des Hinweis-Knopfes. Muss `https://` sein, sonst verwirft die App die Adresse. |
| `notes_de` / `notes_en` | Ein bis zwei Sätze, die die App unter dem Hinweis anzeigt. |

**Reihenfolge bei einem Release:** erst die neue `.msi` als Release hochladen, **danach** `version`
in dieser Datei erhöhen. Andernfalls verweist der Hinweis auf eine Version, die es noch nicht zum
Herunterladen gibt.

## Lizenz

Universal Terminal ist **kostenlos nutzbar, aber nicht quelloffen** — siehe [LICENSE](LICENSE).
Kommerzielle Nutzung erfordert eine Vereinbarung mit dem Entwickler.

Die verwendeten Fremdkomponenten und ihre Lizenzen sind vollständig in der App aufgeführt unter
*Info → Rechtliches → Open-Source-Lizenzen*.

Kontakt: tillegrilleofficial@gmail.com
