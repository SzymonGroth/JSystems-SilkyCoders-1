# JSystems-SilkyCodders-1

Projekt typu Fullstack (Spring Boot + React SPA).

## Wymagania
- Java 21 lub nowsza
- Maven (opcjonalnie, dołączony wrapper `./mvnw`)

## Budowanie aplikacji
Aby zbudować pełną aplikację (backend + frontend) do pojedynczego pliku JAR, wykonaj polecenie:

```bash
./mvnw clean package
```

Podczas tego procesu:
1. `frontend-maven-plugin` automatycznie pobierze Node.js i npm do katalogu `target`.
2. Zostaną zainstalowane zależności frontendu (`npm install`).
3. Frontend zostanie zbudowany (`npm run build`), a jego pliki trafią do `src/main/resources/static`.
4. Maven skompiluje kod Javy i utworzy plik JAR w katalogu `target/`.

## Uruchamianie aplikacji
Po pomyślnym zbudowaniu, aplikację można uruchomić poleceniem:

```bash
java -jar target/JSystems-SilkyCodders-1-0.0.1-SNAPSHOT.jar
```

Aplikacja będzie dostępna pod adresem: [http://localhost:8080](http://localhost:8080)

## Rozwój (Development)
### Frontend
Możesz uruchomić frontend niezależnie w trybie deweloperskim:
```bash
cd frontend
npm install
npm run dev
```

### Backend
Standardowe uruchamianie aplikacji Spring Boot z poziomu IDE lub przez Maven:
```bash
./mvnw spring-boot:run
```
