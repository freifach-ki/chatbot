# Lokaler Chatbot mit Tkinter

## Projektübersicht

Diese Python-Anwendung bietet eine grafische Benutzeroberfläche (GUI) für einen lokalen Chatbot, der mit OpenAI's API kommuniziert. Mit der Anwendung können Benutzer:
- Ein Modell aus vordefinierten Optionen auswählen.
- Dateien (PDFs oder Bilder) hochladen, um der Unterhaltung Kontext zu geben.
- Nachrichten eingeben und die Chat-Historie anzeigen.
- Den Chat-Verlauf in ein Word-Dokument (`.docx`) exportieren.

---

## Ziele der Übung

Diese Übung richtet sich an Studierende, die lernen möchten, wie man:
1. Ein GitHub-Repository klont und lokal auf dem eigenen Rechner bearbeitet.
2. Verbesserungen am Code vornimmt, um neue Funktionen hinzuzufügen.
3. Änderungen testet und überprüft.
4. Die Änderungen im ursprünglichen Repository (per Pull Request) einreicht, damit der Code integriert wird.

---

## Schritt-für-Schritt-Anleitung: Repository klonen und Projekt bearbeiten

### 1. Voraussetzungen

Bevor du startest, stelle sicher, dass folgende Programme installiert sind:
- **Python (mindestens Version 3.8)**: [Python herunterladen](https://www.python.org/downloads/)
- **GitHub Desktop**: [GitHub Desktop herunterladen](https://desktop.github.com)
- **Visual Studio Code (VS Code)**: [VS Code herunterladen](https://code.visualstudio.com)

---

### 2. GitHub Desktop installieren und das Repository klonen

1. **GitHub Desktop installieren**:
   - Lade GitHub Desktop von [desktop.github.com](https://desktop.github.com) herunter.
   - Installiere die Anwendung und melde dich mit deinem GitHub-Account an.

2. **Repository klonen**:
   - Besuche das Repository im Browser (die URL wird vom Dozenten bereitgestellt).
   - Klicke auf die grüne Schaltfläche **Code** und kopiere die Repository-URL (z. B. `https://github.com/username/repo.git`).
   - Öffne GitHub Desktop, klicke auf **File > Clone Repository**, füge die URL ein und wähle einen Speicherort auf deinem Computer aus.
   - Klicke auf **Clone**, um das Projekt auf deinen Computer herunterzuladen.

---

### 3. `.env`-Datei konfigurieren

1. **Beispiel-Datei kopieren**:
   - Im Projektverzeichnis gibt es eine Datei namens `.env.example`. Kopiere diese Datei und benenne sie in `.env` um.
   - Unter macOS/Linux kannst du dies im Terminal mit folgendem Befehl tun:
     ```bash
     cp .env.example .env
     ```
   - Unter Windows kannst du die Datei mit einem beliebigen Texteditor öffnen und als `.env` speichern.

2. **API-Key einfügen**:
   - Öffne die `.env`-Datei mit einem Texteditor.
   - Füge deinen OpenAI API-Schlüssel in die Zeile `OPENAI_API_KEY=` ein, sodass sie folgendermaßen aussieht:
     ```plaintext
     OPENAI_API_KEY=dein-api-schlüssel-hier
     ```
   - Speichere die Datei, nachdem du den Schlüssel hinzugefügt hast.

---

### 4. Projekt in Visual Studio Code öffnen

1. **VS Code starten**:
   - Öffne Visual Studio Code auf deinem Computer.

2. **Projektverzeichnis öffnen**:
   - Klicke auf **File > Open Folder** (oder **Datei > Ordner öffnen**) und navigiere zu dem geklonten Repository.
   - Wähle das Verzeichnis aus, um alle Dateien und Ordner im VS Code-Explorer anzuzeigen.

---

### 5. Abhängigkeiten installieren

1. **Terminal öffnen**:
   - In VS Code: Klicke auf **Terminal > New Terminal** (oder drücke `Strg + Shift + `).

2. **Python-Bibliotheken installieren**:
   - Gib im Terminal den folgenden Befehl ein, um die benötigten Bibliotheken zu installieren:
     ```bash
     pip install -r requirements.txt
     ```

---

### 6. Anwendung starten

1. **Anwendung ausführen**:
   - Gib im Terminal den folgenden Befehl ein:
     ```bash
     python script_name.py
     ```
     (Ersetze `script_name.py` durch den tatsächlichen Namen der Python-Datei, z. B. `chatbot_app.py`.)

2. **Chatbot verwenden**:
   - Die grafische Benutzeroberfläche (GUI) wird geöffnet. Teste die Funktionen, z. B. Nachrichten eingeben, Dateien anhängen und die Chat-Historie exportieren.

---

### 7. Ordnerstruktur vorbereiten

Falls der Code die benötigten Ordner nicht automatisch erstellt, lege die folgenden Ordner im Hauptverzeichnis des Projekts an:
- `chat_history`: Speichert Chat-Verläufe.
- `exported_chats`: Enthält exportierte Chats als `.docx`.
- `prompts`: Hier befinden sich vordefinierte Prompts für das Modell.
- `attachments`: Speichert hochgeladene Dateien wie PDFs oder Bilder.

---

## Erweiterungsaufgaben für Studierende

### 1. "Chat löschen"-Button hinzufügen

**Beschreibung**: Füge einen Button hinzu, der den Chat-Verlauf löscht und die aktuelle Sitzung zurücksetzt. Dies ermöglicht es dem Benutzer, eine neue Unterhaltung zu starten, ohne alte Nachrichten im Verlauf.

**Prompt**:
```plaintext
Ich habe eine Tkinter-basierte Chatbot-Anwendung und möchte einen "Chat löschen"-Button hinzufügen. Beim Klicken soll dieser Button den Chat-Anzeigebereich leeren und die aktuelle Sitzung zurücksetzen. Dies ermöglicht es Benutzern, eine neue Unterhaltung zu starten, ohne Überreste des vorherigen Chats. Bitte geben Sie die Codeänderungen und Erklärungen an, die erforderlich sind, um diese Funktion zu implementieren.
Hier ist der der Code:
[fügen Sie den Code hier ein]
```

---

### 2. Hochgeladene Dateien für mehrere Abfragen aktiv halten

**Beschreibung**: Aktuell wird eine hochgeladene Datei nur für eine einzelne Interaktion verarbeitet. Ändere die Anwendung so, dass die Datei während der gesamten Chatsitzung aktiv bleibt, bis der Benutzer eine neue Datei hochlädt oder die Sitzung beendet.

**Prompt**:
```plaintext
Ich habe eine Python Tkinter-Anwendung für einen Chatbot, die es Benutzern erlaubt, Dateien (PDFs oder Bilder) hochzuladen und mit der OpenAI-API zu interagieren. Derzeit wird eine hochgeladene Datei nur für eine einzelne Interaktion verarbeitet. Ich möchte die Anwendung so erweitern, dass die hochgeladene Datei während der gesamten Chatsitzung aktiv bleibt, sodass Benutzer mehrere Fragen zu derselben Datei stellen können, ohne sie erneut hochzuladen. Die Datei soll aktiv bleiben, bis der Benutzer eine neue Datei hochlädt oder die Sitzung beendet. Bitte geben Sie die erforderlichen Codeänderungen und Erklärungen an, um diese Funktion zu implementieren.
Hier ist der der Code:
[fügen Sie den Code hier ein]
```

---

### 3. UI-Layout und Design verbessern

**Beschreibung**: Verbessere die Benutzeroberfläche, indem du das Layout übersichtlicher und optisch ansprechender gestaltest (Farben, Schriften, Ausrichtung der Widgets).

**Prompt**:
```plaintext
Ich habe eine Tkinter-GUI für eine Chatbot-Anwendung, die Labels, Buttons und Textbereiche enthält. Ich möchte das Layout und Design verbessern, damit es benutzerfreundlicher und ansprechender wird. Dazu gehören eine bessere Ausrichtung der Widgets, konsistente Abstände und möglicherweise Farben oder Schriftarten. 
Hier ist der der Code:
[fügen Sie den Code hier ein]
```

---

### 4. Integration mit anderen KI-Diensten

**Beschreibung**: Erweitere die Anwendung, um zwischen mehreren KI-Diensten wie Anthropics `Claude.ai` oder Googles `Gemini` zu wechseln. Benutzer sollten API-Schlüssel für diese Dienste in der `.env`-Datei angeben und den gewünschten Dienst aus einer Dropdown-Liste auswählen können.

**Prompt**:
```plaintext
Ich habe eine Python-Chatbot-Anwendung, die derzeit die OpenAI-API verwendet, um Antworten zu generieren. Ich möchte die Anwendung so erweitern, dass sie zusätzliche KI-Dienste wie Anthropics Claude und Googles Gemini unterstützt. Benutzer sollten API-Schlüssel für diese Dienste in einer Konfigurationsdatei angeben können und den gewünschten Dienst aus einem Dropdown-Menü in der Anwendung auswählen. Bitte geben Sie die erforderlichen Codeänderungen und Erklärungen an, um diese Funktion zu implementieren.
Hier ist der der Code:
[fügen Sie den Code hier ein]
```

---

### 5. Fortgeschrittene: Änderungen zurück in das ursprüngliche Repository einfügen

**Schritt-für-Schritt-Anleitung**:

1. **Änderungen committen**:
   - Nachdem du deine Änderungen getestet hast, öffne GitHub Desktop.
   - Wähle die Dateien aus, die du geändert hast, und beschreibe die Änderungen in der Commit-Nachricht (z. B. `UI verbessert` oder `Funktion für Chat-Löschen hinzugefügt`).
   - Klicke auf **Commit to main**, um die Änderungen lokal zu speichern.

2. **Änderungen pushen**:
   - Klicke in GitHub Desktop auf **Push origin**, um deine Änderungen in deinem Fork des Repositorys hochzuladen.

3. **Pull Request erstellen**:
   - Besuche dein GitHub-Fork im Browser.
   - Klicke auf **New Pull Request**, beschreibe die Änderungen und reiche den Pull Request ein.

4. **Feedback einholen**:
   - Dein Dozent wird den Pull Request überprüfen und entweder Feedback geben oder die Änderungen akzeptieren.

---

## Unterstützende Bibliotheken
- **Tkinter**: GUI-Framework
- **OpenAI**: API-Interaktionen
- **python-dotenv**: Verwalten von Umgebungsvariablen
- **PyPDF2**: Verarbeiten von PDF-Dateien
- **Pillow**: Arbeiten mit Bildern
- **python-docx**: Erstellen von Word-Dokumenten

---

## Lizenz

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
```