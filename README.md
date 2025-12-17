# DAS Juridisch Portal - LegalEase AI

Een moderne, AI-aangedreven juridisch portaal voor DAS Rechtsbijstand. Dit platform biedt gebruikers een intuïtieve interface om juridische documenten te beheren, advies te krijgen via AI, en hun juridische zaken te volgen.

## ✨ Features

- **📊 Dashboard**: Overzicht van alle juridische activiteiten en documenten
- **📄 Document Management**: Upload en beheer juridische documenten met drag-and-drop functionaliteit
- **💬 AI Juridisch Advies**: Chat met een AI-assistent voor juridische vragen
- **🤖 Video Adviseur**: Geïntegreerde HeyGen AI video avatar voor persoonlijk advies
- **📅 Dossier Timeline**: Visuele tijdlijn van uw juridische zaak
- **⚙️ Instellingen**: Beheer uw persoonlijke gegevens en notificatie voorkeuren
- **🎨 Modern Design**: Glassmorphism design met responsive layout

## 🚀 Deployment

### Railway Deployment (Recommended)

1. **Push naar GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit: DAS Juridisch Portal"
   git push -u origin claude/create-das-portal-43pdQ
   ```

2. **Deploy op Railway**:
   - Ga naar [railway.app](https://railway.app)
   - Klik op "New Project"
   - Selecteer "Deploy from GitHub repo"
   - Kies de `DAS-Juridisch-Portal` repository
   - Selecteer de branch `claude/create-das-portal-43pdQ`
   - Railway detecteert automatisch de Node.js applicatie
   - Klik op "Deploy Now"

3. **Configureer Domain** (optioneel):
   - Ga naar Settings in je Railway project
   - Onder "Domains", klik op "Generate Domain"
   - Of voeg een custom domain toe

### Lokale Development

1. **Installeer dependencies**:
   ```bash
   npm install
   ```

2. **Start de server**:
   ```bash
   npm start
   ```

3. **Open in browser**:
   ```
   http://localhost:3000
   ```

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3 (Glassmorphism design), Vanilla JavaScript
- **Backend**: Node.js + Express
- **AI Integration**: HeyGen Video Avatar API
- **Deployment**: Railway
- **Version Control**: Git/GitHub

## 📱 Features Overview

### Dashboard
- Real-time overzicht van documenten en status
- Recente activiteiten feed
- Status badges voor verschillende acties

### Document Management
- Drag-and-drop file upload
- Ondersteunt PDF, DOC, DOCX, JPG, PNG
- Document preview en download opties
- Document verwijderen functionaliteit

### AI Chat
- Real-time chat met AI juridisch adviseur
- Contextbewust advies op basis van geüploade documenten
- Chat geschiedenis

### Video Adviseur (HeyGen)
- AI-aangedreven video avatar
- Real-time spraak interactie
- Gepersonaliseerd juridisch advies
- Geïntegreerd in het portaal

### Timeline
- Visuele weergave van zaak progressie
- Belangrijke mijlpalen en updates
- Toekomstige stappen en acties

## 🎨 Design Features

- **Glassmorphism UI**: Modern, semi-transparent design met blur effecten
- **Gradient Background**: Professionele blauw gradient in DAS kleuren
- **Responsive**: Werkt perfect op desktop, tablet en mobile
- **Smooth Animations**: Subtiele animaties voor betere UX
- **Accessibility**: Hoge contrast en leesbare typografie

## 🔐 Security

- HTTPS enforced (via Railway)
- Client-side file validation
- Secure document handling
- No sensitive data in client-side code

## 📝 Environment Variables

Geen environment variables nodig voor basic deployment. Voor productie:

- `PORT`: Server port (automatisch ingesteld door Railway)
- `NODE_ENV`: production/development

## 🤝 Contributing

Dit is een demonstratie project voor DAS Rechtsbijstand. Voor wijzigingen, neem contact op met het development team.

## 📄 License

MIT License - Copyright (c) 2024 DAS Rechtsbijstand

## 🆘 Support

Voor vragen of problemen:
- Email: support@das.nl
- Telefoon: +31 20 651 8888

---

**Powered by DAS Rechtsbijstand** - Juridische zekerheid, altijd en overal.
