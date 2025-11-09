# AutoInbox - Full Project

**AutoInbox** is an AI-powered email automation platform that categorizes emails, generates summaries, and drafts smart replies automatically.  
This repository contains the **full project**, including the landing page, Dart backend, Flutter mobile app, Stripe integrations, and AI content/image workflows.

---

## Table of Contents

- [Project Aim](#project-aim)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Setup & Development](#setup--development)
- [AI Workflows](#ai-workflows)
- [Deployment & Domain Setup](#deployment--domain-setup)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)

---

## Project Aim

- Reduce time spent managing email by automating sorting, summarizing, and replying.
- Enable both web and mobile users to access AI-powered email automation.
- Provide a scalable, modular platform with **AI-assisted workflows** for copy, UI content, and automated responses.
- Launch a professional landing page for marketing and user acquisition.

---

## Key Features

**Landing Page**

- Hero section with AI-generated headline and subtext.
- Feature sections highlighting AI email capabilities.
- Security/privacy reassurance section.
- Social proof/testimonials and clear CTAs.
- AI-powered text and image updates via JSON + Code Overrides.

**Backend/API**

- Dart backend (serverless with Firebase Functions or Dart server).
- Handles user authentication via Firebase Auth.
- Manages email analysis, categorization, AI summaries, and draft replies.
- Stripe Connect integration for subscriptions or monetization.

**Flutter App**

- Mobile UI for user onboarding and email account connection.
- Displays categorized emails, AI summaries, and suggested replies.
- Allows users to accept, edit, or send AI-generated replies.
- Includes Stripe Connect dashboard for earnings or subscription management.
- Uses Dio for API requests; integrates Firebase for authentication and backend.

**AI Workflows**

- AI-driven text content for landing page, in-app prompts, and notifications.
- AI-driven image generation for landing page illustrations and in-app icons.
- JSON files (`content.js`, `images.js`) for rapid updates without manual UI changes.
- Supports bulk replacement and rapid iteration.

---

## Tech Stack

- **Frontend / Landing Page:** Framer, HTML, CSS, JS, Code Overrides.
- **Backend:** Dart (Firebase Functions or self-hosted Dart server).
- **Mobile App:** Flutter (iOS + Android), Dio, Firebase Auth.
- **Payments:** Stripe Connect (backend + Flutter UI).
- **AI Tools:** OpenAI API (text & prompt engineering), AI Studio / MidJourney for images.
- **Hosting:** GitHub Pages (landing page), Firebase Hosting / Dart server for backend.

---

## Repository Structure

landing-page/  
&nbsp;&nbsp;src/  
&nbsp;&nbsp;&nbsp;&nbsp;index.html  
&nbsp;&nbsp;&nbsp;&nbsp;styles.css  
&nbsp;&nbsp;&nbsp;&nbsp;scripts.js  
&nbsp;&nbsp;code/  
&nbsp;&nbsp;&nbsp;&nbsp;content.js  
&nbsp;&nbsp;&nbsp;&nbsp;images.js  
&nbsp;&nbsp;CNAME

dart-backend/  
&nbsp;&nbsp;functions/ # Firebase Functions or Dart server code  
&nbsp;&nbsp;pubspec.yaml # Dart dependencies

flutter-app/  
&nbsp;&nbsp;lib/  
&nbsp;&nbsp;&nbsp;&nbsp;main.dart  
&nbsp;&nbsp;&nbsp;&nbsp;pages/  
&nbsp;&nbsp;&nbsp;&nbsp;widgets/  
&nbsp;&nbsp;pubspec.yaml  
&nbsp;&nbsp;assets/

README.md  
docs/ # Optional diagrams, design files, flowcharts

---

## Setup & Development

### Landing Page

1. Open `landing-page/src/index.html` in browser.
2. Update text/images via `code/content.js` and `code/images.js`.
3. Push changes to GitHub Pages for live updates.

### Dart Backend

1. Navigate to `dart-backend/`.
2. Install dependencies:

```
dart pub get
```

3. Run locally (Firebase Functions):

```
firebase emulators:start
```

or, for a self-hosted Dart server:

```
dart run bin/server.dart
```

### Flutter App

1. Navigate to `/flutter-app`.
2. Install dependencies and run:

```
flutter pub get
flutter run
```

3. Configure Firebase credentials for authentication and backend API access.

---

## AI Workflows

- Landing page text/images are stored in JSON for Code Overrides.
- Flutter app uses similar JSON + prompt engineering for in-app copy and notifications.
- AI-generated images and icons are stored in `images.js` and can be swapped without touching layout.
- Supports bulk updates and rapid iteration.

---

## Deployment & Domain Setup

- Landing page hosted on **GitHub Pages**.
- Add a `CNAME` file with your domain (e.g., `autoinbox.app`).
- Update DNS:
  - **A records** for root domain → `185.199.108.153` … `185.199.111.153`
  - **CNAME** for www subdomain → `username.github.io`
- Enable HTTPS in GitHub Pages settings.
- Dart backend deployed via Firebase Functions or self-hosted server.
- Flutter app deployed to App Store and Play Store.

---

## Future Improvements

- Full AI integration for bulk text and image updates.
- Interactive 3D visuals using Three.js / WebGL.
- Analytics and conversion tracking.
- Multi-language support.
- Expand Code Override system for instant content refresh.

---

## Contributing

1. Fork the repo.
2. Create a new branch for your changes.
3. Make edits to `content.js`, `images.js`, backend Dart code, or Flutter UI as needed.
4. Submit a pull request with a clear description.

**Author:** Your Name  
**Website:** [https://autoinbox.app](https://autoinbox.app)
