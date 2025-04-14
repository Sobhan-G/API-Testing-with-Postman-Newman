Detta projekt innehåller en uppsättning automatiserade API-tester för ett publikt REST API på [reqres.in](https://reqres.in). Tester är skapade med Postman och kan köras både manuellt i Postman eller automatiserat via Newman – en CLI-testrunner.

## 🎯 Syfte

Att visa förståelse för API-testning, felhantering och automatisering inom test/QA. Projektet simulerar verkliga användarflöden såsom inloggning, datahämtning, dataskapande och borttagning av resurser.

## 🚀 Funktioner

- ✅ Inloggning (med och utan lösenord)
- 👥 Hämta användarlista
- ➕ Skapa ny användare
- 🗑️ Ta bort användare
- 🔄 Validering av HTTP-statuskoder, JSON-respons och felhantering

## 🧰 Använda verktyg

- [Postman](https://www.postman.com/)
- [Newman](https://www.npmjs.com/package/newman)
- JavaScript (för testskript)
- reqres.in (mock API)

## 📦 Projektstruktur

```
API-Testing-with-Postman-Newman/
├── README.md
├── collections/
│   └── QA-Demo.postman_collection.json
├── environments/
│   └── reqres-environment.postman_environment.json
└── reports/
    └── (kan läggas till via Newman CLI)
```

## 🛠️ Kom igång

### 1. Klona projektet

```bash
git clone https://github.com/Sobhan-G/API-Testing-with-Postman-Newman.git
cd API-Testing-with-Postman-Newman
```

### 2. Installera Newman

```bash
npm install -g newman
```

### 3. Kör testsviten

```bash
newman run collections/Sobhan-QA-Demo.postman_collection.json \
  -e environments/reqres-environment.postman_environment.json
```

### 4. Skapa HTML-rapport (valfritt)

```bash
newman run collections/Sobhan-QA-Demo.postman_collection.json \
  -e environments/reqres-environment.postman_environment.json \
  -r cli,html --reporter-html-export reports/test-report.html
```

## 🧪 Testfall

| Testnamn            | Endpoint             | Vad testas                          |
|---------------------|----------------------|-------------------------------------|
| Login - Success     | POST /api/login      | Lyckad inloggning, token skapas     |
| Login - Fail        | POST /api/login      | Misslyckad inloggning (saknar lösenord) |
| Get Users           | GET /api/users?page=2| Användardata hämtas korrekt         |
| Create User         | POST /api/users      | Ny användare skapas                 |
| Delete User         | DELETE /api/users/2  | Användare raderas korrekt           |

## 📈 Resultat

Exempel på output via CLI:

```
→ Login - Success
  ✓ Status 200
  ✓ Token är en sträng

→ Login - Fail
  ✓ Status 400
  ✓ Felmeddelande: "Missing password"
```

## 📚 Lärdomar

Detta projekt förbättrade min praktiska förståelse för:
- API-design och teststrategier
- Automatisering av tester med Newman
- Felhantering och testdrivna testscenarier
- Förberedelse för CI/CD-integrering

## 🧩 Möjlig utökning

- Lägga till CI/CD via GitHub Actions
- Använda data-driven testing (JSON/datafiler)
- Lägg till testsuite för andra API-miljöer (t.ex. auth, e-handel, osv.)

