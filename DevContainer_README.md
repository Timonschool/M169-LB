# Dev Container Setup Guide

## Einleitung

Dieses Projekt verwendet einen Dev-Container, um eine konsistente Entwicklungsumgebung zu gewährleisten. Diese Anleitung beschreibt, wie das Repository in einem Dev-Container geöffnet und die Anwendung gestartet wird.

## Schritte zur Einrichtung

1. **VS Code und Dev Containers Erweiterung installieren**
   - Stelle sicher, dass du [Visual Studio Code](https://code.visualstudio.com/) und die Erweiterung "Dev Containers" installiert hast.

2. **Repository klonen**
   ```bash
   git clone <repository-url>
   cd my_php_project
   ```

3. **Dev-Container öffnen**
   - Öffne das Projekt in VS Code.
   - Öffne die Kommando-Palette (F1) und wähle `Remote-Containers: Reopen in Container`.

4. **Anwendung starten**
   - Nach dem Öffnen des Containers in VS Code kannst du die Anwendung starten.
   - Öffne eine neue Terminalinstanz und führe folgenden Befehl aus:
     ```bash
     docker-compose up --build
     ```

## Debugging

- Du kannst Debugging direkt in VS Code nutzen, indem du `F5` drückst.

## Wichtige Extensions

- **PHP Debug**: Unterstützt die PHP-Entwicklung mit Debugging-Funktionen.
- **Intelephense**: Bietet leistungsstarkes IntelliSense und Typprüfung für PHP.
- **Docker**: Ermöglicht die Verwaltung von Docker-Containern und -Images direkt in VS Code.

## Datenbankintegration

- Das Projekt verwendet eine MySQL-Datenbank.
- Der Datenbankinhalt kann über phpMyAdmin überprüft werden, das unter `http://localhost:8081` erreichbar ist (Standard-Login: root / rootpassword).

## Sicheres Handling sensibler Daten

- Verwende die `.env`-Datei, um sensible Daten zu speichern. Diese Datei wird nicht ins Repository eingecheckt.
- Die Struktur der `.env`-Datei ist in der `env-schema.txt`-Datei dokumentiert.
