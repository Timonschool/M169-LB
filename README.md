# My PHP Project
 
Dies ist ein Beispielprojekt zur Demonstration der Verwendung von Dev-Containern mit Docker und Visual Studio Code. Das Projekt enthält eine einfache PHP-Anwendung mit MySQL-Datenbankintegration und einem phpMyAdmin-Tool zur Verwaltung der Datenbank.
 
## Projektbeschreibung
 
### Komponenten
 
 
1. **PHP-Webanwendung:**
   - Eine einfache PHP-Webanwendung, die eine Verbindung zu einer MySQL-Datenbank herstellt und Daten aus einer Tabelle anzeigt.
   - Der Quellcode der Anwendung befindet sich im Verzeichnis `src`.
 
2. **MySQL-Datenbank:**
   - Eine MySQL-Datenbank, die von der PHP-Anwendung genutzt wird.
   - Die Datenbank wird beim Starten des Containers automatisch mit einer Beispieltabelle (`users`) und einem Beispiel-Datensatz (`John Doe`) initialisiert.
   - Das Initialisierungsskript befindet sich in der Datei `database/init.sql`.
 
3. **phpMyAdmin:**
   - Ein Web-basiertes Administrationstool für MySQL-Datenbanken.
   - Läuft auf `http://localhost:8081` und kann verwendet werden, um die Datenbank zu verwalten und zu überprüfen.
 
### Verzeichnisstruktur
 
- **`.devcontainer/`**: Enthält Konfigurationsdateien für den Dev-Container.
- **`src/`**: Enthält den Quellcode der PHP-Anwendung.
- **`database/`**: Enthält das Initialisierungsskript für die MySQL-Datenbank.
- **`.env`**: Enthält Umgebungsvariablen wie die Datenbank-URL.
- **`.gitignore`**: Enthält Dateien und Verzeichnisse, die nicht ins Repository eingecheckt werden sollen.
- **`docker-compose.yml`**: Definiert die Docker-Dienste und deren Konfiguration.
- **`Dockerfile`**: Definiert das Docker-Image für die PHP-Anwendung.
- **`DevContainer_README.md`**: Anleitung zur Verwendung des Dev-Containers.
- **`env-schema.txt`**: Schema der `.env`-Datei.
- **`README.md`**: Allgemeine Projektbeschreibung und Anleitung.
 
## Voraussetzungen
 
1. **Docker installieren:**
   - Besuchen Sie die [Docker-Website](https://www.docker.com/products/docker-desktop) und laden Sie Docker Desktop herunter. Installieren Sie es auf Ihrem Computer.
 
2. **Visual Studio Code installieren:**
   - Besuchen Sie die [Visual Studio Code-Website](https://code.visualstudio.com/) und laden Sie den Editor herunter. Installieren Sie ihn auf Ihrem Computer.
 
3. **Dev Containers Erweiterung in VS Code installieren:**
   - Öffnen Sie Visual Studio Code.
   - Gehen Sie zur Erweiterungsansicht (Symbol mit vier Quadraten auf der linken Seitenleiste).
   - Suchen Sie nach "Dev Containers" und installieren Sie die Erweiterung.
 
## Schritt-für-Schritt-Anleitung
 
### 1. Projekt herunterladen
 
- Drücken Sie im Github Repository auf den Dev Container Open knopf
- 
 <a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Timonschool/M169-LB.git">
  <img 
    src="https://img.shields.io/badge/Open_in-DevContainer-blue?logo=visual-studio-code" 
    alt="Open in DevContainer" 
    height="40"
  >
</a>
### 2. Projekt in VS Code öffnen
 
- Öffnen Sie Visual Studio Code.
 
 
### 3. Anwendung starten
 
- Öffnen Sie ein neues Terminal in VS Code (`Terminal` -> `Neues Terminal`).
- Stellen Sie sicher, dass Sie sich im Projektverzeichnis befinden.
- Führen Sie den folgenden Befehl aus, um die Docker-Container zu starten:
  ```bash
  docker-compose up 
