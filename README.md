# SGFN-RDC — Système de Gestion Foncière Numérique

Cadastre numérique officiel de la République Démocratique du Congo.

## Setup rapide

### 1. Base de données MySQL

```bash
mysql -u root -p'minitmoney@sql' < backend/database/schema.sql
mysql -u root -p'minitmoney@sql' sgfn_rdc < backend/database/seed.sql
```

### 2. Backend (port 4001)

```bash
cd backend
npm install
node src/app.js
```

### 3. Frontend (port 3001)

```bash
cd frontend
npm install
npm run dev
```

## Comptes de démonstration

| Rôle | Email | Mot de passe |
|------|-------|--------------|
| Admin | admin@sgfn-rdc.cd | Admin2026! |
| Agent | agent1@sgfn-rdc.cd | Admin2026! |
| Citoyen | citizen1@sgfn-rdc.cd | Admin2026! |

## Stack technique

- **Backend**: Express.js + MySQL2 + JWT + bcrypt
- **Frontend**: Next.js 14 + Tailwind CSS + Leaflet.js
- **Base de données**: MySQL 8
- **Carte**: OpenStreetMap (gratuit, sans clé API)
- **Charts**: Recharts
- **Documents**: PDFKit (e-Titres PDF)

## URLs

- Frontend: http://localhost:3001
- Backend API: http://localhost:4001/api
- Health check: http://localhost:4001/api/health
# cadastre
