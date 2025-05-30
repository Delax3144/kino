# 🎬 KinoApp – System Rezerwacji Biletów

KinoApp to pełnoprawna aplikacja internetowa do rezerwacji miejsc w kinie, stworzona przy użyciu **Java + Spring Boot** po stronie backendu oraz **React + Vite** po stronie frontendowej. Dane przechowywane są w lokalnej bazie danych **MySQL**.

---

## 🧰 Technologie

- Java 17+ / Spring Boot
- React + Vite
- Tailwind CSS
- MySQL
- Maven
- Node.js

---

## 📁 Struktura projektu

```
kino-app/
├── booking-backend/
│   └── booking-api/         # Backend z pom.xml
└── booking-frontend/        # Frontend React (Vite)
```

---

## ✅ Wymagania

Zanim rozpoczniesz:

- Java 17+ (np. OpenJDK)
- Maven
- Node.js i npm
- MySQL (lub XAMPP)
- Git

---

## 🚀 Jak uruchomić projekt lokalnie?

### 1. Klonowanie repozytorium

```bash
git clone https://github.com/Delax3144/kino-backend.git
cd kino-backend
```

---

### 2. Konfiguracja bazy danych

#### Utwórz bazę danych

1. Uruchom MySQL / XAMPP.
2. Zaloguj się do phpMyAdmin lub terminala.
3. Wykonaj:

```sql
CREATE DATABASE booking;
```

#### Sprawdź plik konfiguracji

Otwórz plik:

```
booking-backend/booking-api/src/main/resources/application.properties
```

Upewnij się, że zawiera:

```
spring.datasource.url=jdbc:mysql://localhost:3306/booking
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
```

> Zmień `username` i `password`, jeśli masz inne dane logowania.

---

### 3. Uruchom backend

```bash
cd booking-backend/booking-api
mvn spring-boot:run
```

Po uruchomieniu, backend będzie działał pod adresem:

```
http://localhost:8080
```

Sprawdź np.: `http://localhost:8080/api/movies`

---

### 4. Uruchom frontend

```bash
cd booking-frontend
npm install
npm run dev
```

Frontend uruchomi się pod:

```
http://localhost:5173
```

---

## 🧪 Testowanie aplikacji

1. Otwórz `http://localhost:5173`
2. Zarejestruj konto
3. Przeglądaj filmy
4. Kliknij na jeden z dostępnych seansów
5. Wybierz miejsca
6. Kliknij „Zarezerwuj”
7. Sprawdź zakładkę „Moje rezerwacje”

---

## 👤 Panel administratora

Jeśli zalogujesz się jako: `admin@gmail.com`, zobaczysz panel **Admin Panel**, który pozwala dodawać filmy i godziny seansów.

---

## 🛠️ Rozwiązywanie problemów

- Sprawdź, czy serwer MySQL działa
- Upewnij się, że baza danych `booking` istnieje
- Sprawdź logi backendu (`mvn spring-boot:run`) i konsolę przeglądarki (frontend)
- Upewnij się, że w `localStorage` znajduje się zapisany email użytkownika

---

## 🖼️ Zrzuty ekranu

Dodaj własne zrzuty ekranu w folderze `screenshots/` i uzupełnij je tutaj:

- Strona główna
- Rezerwacja miejsc
- Moje rezerwacje

---

## 📜 Licencja

Projekt edukacyjny. W pełni otwarty do użycia i modyfikacji.

---

Miłego korzystania z **KinoApp**! 🎟️