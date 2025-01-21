Diese Website basiert auf [Markdown-Dateien](https://www.markdownguide.org/getting-started/), die mit [Jekyll](https://jekyllrb.com/) in HTML-Seiten umgewandelt werden.

# **Neue Inhalte hinzufügen**

## 1. Zum Ordner navigieren

Gehe zu dem Ordner, in dem du die neue Seite speichern möchtest (z. B. `Getreide/`).

## 2. Datei erstellen

Klicke auf den Button **"Add file"** und wähle **"Create new file"** aus.

## 3. Datei benennen

Gib der Datei einen sinnvollen Namen (z. B. `Agrarhaendler.md`). Achte darauf, dass der Dateiname auf `.md` endet, da es sich dabei um eine Markdown-Datei handelt. Du kannst auch Ordnerstrukturen erstellen, indem du im Dateinamen einen Ordner angibst, z. B. `Getreide/Agrarhaendler.md`, um neben der Datei auch den entsprechenden Ordner anzulegen. Sobald du die Datei speicherst und auf **"Commit changes..."** klickst, wird sie automatisch von Jekyll in eine HTML-Seite umgewandelt und auf der Website angezeigt.

## 4. Struktur hinzufügen

Füge oben in der Datei die folgende Struktur ein:

```yaml
---
title: "Titel der Seite"
---
```
Hinweis: Ersetze `Titel der Seite` durch den tatsächlichen Titel der Seite.

## 5. Arten von Seiten

Je nachdem, welche Art von Seite du anlegst, beachte bitte die folgenden Schritte:

### 5a. Schaubild

Wenn es sich um ein Lebensmittel-Schaubild handelt:

1. Lade das Schaubild als PDF in den entsprechenden Ordner hoch.
2. Hinterlege in der `.md-Datei` folgenden Code, um das Schaubild einzubinden:

```html
<iframe
  src="Pfad-zum-Schaubild.pdf"
  style="width: 100%; height: 500px; border: none;"
></iframe>
```

Hinweis: Ersetze `Pfad-zum-Schaubild.pdf` durch den tatsächlichen relativen Pfad zur PDF-Datei. Beispiel:

```html
<iframe
  src="Getreide-Schaubild.pdf"
  style="width: 100%; height: 500px; border: none;"
></iframe>
```

### 5b. Erklärende Unterseite zu einem Schaubild

Wenn es sich um eine Unterseite handelt

1. Füge am Ende der `.md-Datei` den folgenden Code hinzu, um das Literaturverzeichnis einzubinden:

```html
<br />
---
<br />
{% capture literaturverzeichnis %} {% include Literaturverzeichnis.md %}
{%endcapture %} {{ literaturverzeichnis | markdownify }}
```

## 6. Literaturverzeichnis bearbeiten

Das Literaturverzeichnis findest du im Ordner `\_includes`. Ergänze dort neue Einträge nach Bedarf.
