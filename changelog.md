# Changelog

## [2026-01-21 14:19]
- **Task**: Dodanie sekcji "Code Review Guidelines" do `agents.md`.
- **Files Modified**:
    - `agents.md`
- **Decisions**: 
    - Wprowadzono nowe wytyczne dla agentów AI dotyczące przeprowadzania Code Review na Pull Requestach.
    - Wytyczne obejmują sposób komentowania, prefixowanie komentarzy, obsługę poprawek oraz wymagane narzędzia (GitHub CLI).
    - Dokumentację sporządzono w języku angielskim, aby zachować spójność z resztą pliku `agents.md`.

## [2026-01-21 13:45]
- **Task**: Naprawa uwag z PR #1 (initial).
- **Files Modified**:
    - `.gitignore`
    - `agents.md`
    - `frontend/index.html`
    - `frontend/package.json`
    - `pom.xml`
- **Files Deleted**:
    - `src/main/resources/static/index.html` (i artefakty w `assets/`)
- **Decisions**:
    - Poprawiono literówki w dokumentacji `agents.md`.
    - Dodano `vitest` i biblioteki testowe do frontendu.
    - Usunięto nieistniejącą ikonę `vite.svg` z `index.html`.
    - Zmieniono `installDirectory` dla Node w `pom.xml` na root projektu (`.`), aby uniknąć kasowania przy `mvn clean`.
    - Wykluczono katalogi `node/` oraz `src/main/resources/static/` z Git, usuwając wcześniej scommitowane artefakty.

## [2026-01-21 12:51]
- **Task**: Dodanie wymogu angielskich opisów PR do `agents.md`.
- **Files Modified**:
    - `agents.md`
- **Decisions**: Zaktualizowano wytyczne dla agentów, wprowadzając zasadę sporządzania opisów Pull Requestów w języku angielskim.

## [2026-01-21 12:20]
- **Task**: Dodanie wytycznych dotyczących strukturyzacji projektu do `agents.md`.
- **Files Modified**:
    - `agents.md`
- **Decisions**: Wprowadzono zasadę separacji kawałków biznesowych do osobnych katalogów/pakietów, aby ułatwić ich ewentualną ekstrakcję do niezależnych aplikacji w przyszłości (podejście modularne).

## [2026-01-21 12:08]
- **Task**: Utworzenie pliku `readme.md` z instrukcją budowania i uruchamiania.
- **Files Created**:
    - `readme.md`
- **Decisions**: Przygotowano dokumentację w języku polskim, opisującą wymagania, proces budowania za pomocą Mavena oraz sposób uruchamiania gotowego artefaktu JAR.

## [2026-01-21 12:06]
- **Task**: Uruchomienie zbudowanego artefaktu JAR.
- **Files Modified**:
    - `changelog.md`
- **Decisions**: 
    - Zlokalizowano plik `target/JSystems-SilkyCodders-1-0.0.1-SNAPSHOT.jar`.
    - Uruchomiono aplikację komendą `java -jar` w tle.
    - Zweryfikowano działanie aplikacji za pomocą `curl`, potwierdzając serwowanie strony `index.html` pod adresem `http://localhost:8080`.

## [2026-01-21 12:05]
- **Task**: Integracja frontend i backend w jeden artefakt JAR z wyświetlaniem "Hello World".
- **Files Modified**:
    - `frontend/src/App.jsx`
    - `frontend/vite.config.js`
    - `pom.xml`
    - `changelog.md`
- **Decisions**: 
    - Zaktualizowano `App.jsx`, aby wyświetlał prosty komunikat "Hello World".
    - Skonfigurowano Vite (`vite.config.js`), aby budował frontend do `src/main/resources/static`.
    - Dodano `frontend-maven-plugin` do `pom.xml`, aby automatyzować instalację Node/npm oraz budowanie frontendu podczas cyklu życia Mavena.
    - Zweryfikowano poprawność budowania za pomocą `./mvnw clean package`.

## [2026-01-21 12:05]
- **Task**: Utworzenie specyficznego dla frontendu pliku `agents.md` w katalogu `frontend`.
- **Files Created**:
    - `frontend/agents.md`
- **Decisions**: Przygotowano zestaw wytycznych dla React SPA oparty na dobrych praktykach (Hooki, komponenty funkcyjne, Vitest), dostosowany do struktury projektu Vite.

## [2026-01-21 11:58]
- **Task**: Add information about mandatory changelog to `agents.md` and create the initial `changelog.md`.
- **Files Modified**:
    - `agents.md`
- **Files Created**:
    - `changelog.md`
- **Decisions**: Added `## Agent Changelog` section to `agents.md` to ensure traceability of AI-driven changes.
