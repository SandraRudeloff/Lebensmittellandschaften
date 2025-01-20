# **Neue Inhalte hinzufügen**

## Zum Ordner navigieren

Gehe zu dem Ordner, in dem du die neue Seite speichern möchtest (z. B. `Getreide/`).

## Datei erstellen

Klicke auf den Button **"Add file"** und wähle **"Create new file"** aus.

## Datei benennen

Gib der Datei einen sinnvollen Namen (z. B. `Agrarhaendler.md`).

## Struktur hinzufügen

Füge oben in der Datei die folgende Struktur ein:

```yaml
---
title: ""
---
```

## Schaubild

Wenn es sich um ein Schaubild handelt

1. Lade das Schaubild als PDF in den entsprechenden Ordner hoch.
2. Hinterlege in der .md-Datei folgenden Code, um das Schaubild einzubinden:

```html
<iframe
  src="Pfad-zum-Schaubild.pdf"
  style="width: 100%; height: 500px; border: none;"
></iframe>
```

Hinweis: Ersetze Pfad-zum-Schaubild.pdf durch den tatsächlichen relativen Pfad zur PDF-Datei. Beispiel:

```html
<iframe
  src="Getreide/Getreide-Schaubild.pdf"
  style="width: 100%; height: 500px; border: none;"
></iframe>
```

## Unterseite

Wenn es sich um eine Unterseite handelt 1. Füge am Ende der .md-Datei den folgenden Code hinzu, um das Literaturverzeichnis einzubinden:

```html
<br />
---
<br />
{% capture literaturverzeichnis %} {% include Literaturverzeichnis.md %}
{%endcapture %} {{ literaturverzeichnis | markdownify }}
```

## Literaturverzeichnis bearbeiten

Wenn du etwas zum Literaturverzeichnis hinzufügen möchtest, findest du es im Ordner "\_includes".
