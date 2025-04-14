 API Testing with Postman & Newman

Detta projekt innehåller automatiserade tester av ett REST API med hjälp av Postman och testrunnern Newman. Projektet simulerar autentisering, dataskapande och felscenarier.

## ✅ Funktioner
- Testsvit i Postman med flera scenarier
- Körning via kommandorad med Newman
- Validering av statuskoder, svarstider och innehåll
- JSON-schema-validering

## 🛠️ Verktyg & Tekniker
- Postman
- Newman (CLI-runner för Postman)
- JavaScript (för testskript)
- Mock-server eller externt API (ex. reqres.in eller jsonplaceholder.typicode.com)

## 📦 Kom igång

1. **Installera Newman globalt**
```bash
npm install -g newman
```

2. **Kör testsviten (exempel)**
```bash
newman run TestSvit.postman_collection.json
```

3. **Visa testresultat**
```bash
newman run TestSvit.postman_collection.json -r cli,html
```

## 📋 Testscenarier
- `POST /login` – Testar korrekt och felaktig inloggning
- `GET /users` – Verifierar att data returneras korrekt
- `POST /users` – Skickar ny användare och validerar svar
- `DELETE /users/:id` – Säkerställer att användaren tas bort

## 🔍 Lärdomar
- Skapa återanvändbara och datadrivna API-tester
- Automatisera körningar för integration i CI/CD
- Felsöka API-respons och validera olika typer av felhantering

## 🔗 Extra: CI/CD-integration
Detta projekt kan enkelt kopplas till GitHub Actions eller Jenkins för att köra API-tester automatiskt vid kodändringar.

## 📁 Struktur
```
├── TestSvit.postman_collection.json
├── Testmiljö.postman_environment.json
└── README.md


