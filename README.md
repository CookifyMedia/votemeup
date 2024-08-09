# VoteMeUp

**VoteMeUp** är en webbaserad applikation byggd med SvelteKit och Supabase. Den låter användare skapa projekt, nominera namnförslag och rösta på de bästa förslagen. Applikationen är flexibel och enkel att använda, med stöd för både autentisering och cookie-baserad röstning.

## Funktioner

- **Skapa Projekt:** Användare kan skapa sina egna projekt, beskriva dem och bjuda in andra att nominera och rösta på namn.
- **Nominera och Rösta:** Andra användare kan nominera namn och rösta på de mest populära förslagen.
- **Användarautentisering:** Användare kan logga in med Supabase Auth för att skapa projekt och spåra sina nomineringar.
- **Cookie-baserad Röstning:** Röststatus sparas i cookies för att tillåta enkel och smidig röstning utan krav på inloggning.

## Installation och Setup

### 1. Förutsättningar

- Node.js och npm installerat på din maskin.
- Ett konto på Supabase.

### 2. Klona Repositoriet

Klona detta repo till din lokala maskin och navigera till projektmappen:

```bash
git clone https://github.com/CookifyMedia/votemeup.git
cd votemeup
```

### 3. Installera beroenden

Installera nödvändiga npm-paket:

```bash
npm install
```

### 4A. Konfigurera Lokalt Supabase

1. Starta Docker
2. Starta Supabase:

```bash
supabase start 
```

3. Skapa nödvändiga tabeller i Supabase med hjälp av SQL-schemat som finns i dokumentationen.
4. Ändra .env.example till .env i projektroten och lägg till dina Supabase-uppgifter:

```js
SUPABASE_URL=din_supabase_url  
SUPABASE_ANON_KEY=din_supabase_anon_key
```

### 4B. Konfigurera Cloud Supabase

1. Skapa ett nytt projekt på Supabase.
2. Skapa nödvändiga tabeller i Supabase med hjälp av SQL-schemat som finns i dokumentationen.
3. Skapa en .env-fil i projektroten och lägg till dina Supabase-uppgifter:

```js
SUPABASE_URL=din_supabase_url  
SUPABASE_ANON_KEY=din_supabase_anon_key
```

### 5. Kör Applikationen Lokalt

Starta utvecklingsservern med:

```bash
npm run dev
```

Applikationen kommer nu att vara tillgänglig på http://localhost:5173.

## Användning

- **Skapa Projekt:** Gå till /my/projects/new för att skapa ett nytt projekt.
- **Visa och Välj Projekt:** Se en lista över tillgängliga projekt på startsidan, välj ett projekt för att nominera och rösta på namn.
- **Nominera och Rösta:** När du är inne i ett projekt kan du nominera nya namnförslag och rösta på befintliga förslag.

## Deployment

Du kan enkelt deploya VoteMeUp till plattformar som Vercel eller Netlify. Följ deras instruktioner för att deploya en SvelteKit-applikation.

## Bidra

Bidrag till VoteMeUp är välkomna! Om du vill bidra, följ dessa steg:

1. Forka detta repo.
2. Skapa en ny branch (git checkout -b feature/my-feature).
3. Gör dina ändringar och committa (git commit -am 'Add my feature').
4. Pusha till branchen (git push origin feature/my-feature).
5. Skicka in en pull request.

## Licens

VoteMeUp är licensierat under MIT-licensen. Se LICENSE för mer information.
