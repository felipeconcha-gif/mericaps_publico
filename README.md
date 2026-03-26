# MERICAPS

**Version: March 11, 2026**

For questions, collaboration requests, or institutional inquiries please contact:

**[felipeconcha@centroarbol.cl]

---

# MERICAPS

**MERICAPS (Measurement and Research of Change in Psychotherapy)** is an open infrastructure and web-based platform designed to enable **Routine Outcome Monitoring (ROM)** in psychotherapy and mental health services across Latin America.

The platform provides clinicians, supervisors, and institutions with tools to systematically collect, analyze, and visualize psychotherapy outcome data, supporting **data-informed clinical decisions, supervision, and program evaluation**.

MERICAPS was originally developed to support the implementation of ROM in **Centro Médico Árbol (Chile)** and **Proyecto T at Universidad Diego Portales**, and emerged from technological needs identified by clinical centers participating in the **Consorcio Latinoamericano de Investigación en Psicoterapia (CLIP)**.

MERICAPS is currently used in real clinical environments and was developed within the context of psychotherapy services and research initiatives in Latin America.

The project aims to **remove the technical and economic barriers** that historically limited the adoption of ROM systems in the region.

---

# Why MERICAPS Exists

In many psychotherapy settings across Latin America, treatment outcomes are rarely measured systematically.

Existing solutions are often:

• expensive
• technically complex
• dependent on research projects
• difficult to adapt to local clinical contexts

As a result:

• therapists rely mostly on subjective impressions of improvement
• clinical programs lack systematic evaluation
• the region depends on research produced outside its cultural context

MERICAPS was created to **democratize access to outcome monitoring infrastructure**, allowing clinical centers to generate their own evidence about psychotherapy effectiveness.

---

# Core Concept: Routine Outcome Monitoring (ROM)

Routine Outcome Monitoring involves **regularly measuring patient progress throughout psychotherapy** using standardized instruments.

When implemented effectively, ROM can:

• detect early signs of deterioration or stagnation
• support therapist decision-making
• improve supervision processes
• evaluate clinical programs
• generate research data about psychotherapy effectiveness

MERICAPS provides the technological infrastructure necessary to implement this approach in real clinical environments.

---

# Open Infrastructure & Adaptability

MERICAPS was designed as an **open-access code base** that clinical centers and institutions can adopt, deploy, and adapt according to their specific needs.

Rather than functioning as a closed proprietary platform, MERICAPS provides a **flexible technological foundation for implementing Routine Outcome Monitoring in psychotherapy services**.

The system was developed within the **Firebase ecosystem**, allowing institutions to easily deploy and modify the platform using tools such as **Firebase Studio and its AI-assisted code editor**.

This design enables users to:

• deploy their own instance of the platform
• customize assessment instruments and workflows
• adapt the system to local clinical practices
• extend functionality using modern cloud development tools

By combining **open infrastructure with AI-assisted development environments**, MERICAPS lowers the technical barriers traditionally associated with building and maintaining clinical data systems.

This approach allows psychotherapy services across Latin America to implement outcome monitoring **without depending on expensive proprietary software or specialized engineering teams**.

---

# Clinical Context & Real-World Use

MERICAPS was developed in response to real clinical needs identified in psychotherapy services in Latin America.

The platform is currently being implemented in the following contexts.

---

## Centro Médico Árbol (Chile)

Centro Médico Árbol is a psychotherapy center with a strong social orientation, where many therapists are in professional training.

Routine Outcome Monitoring is used to:

• monitor the quality of clinical care
• support supervision processes
• detect early signs of deterioration or stagnation in treatment
• help therapists and patients observe change trajectories over time

MERICAPS was originally created to replace a previous ROM platform that became financially unsustainable for the center.

---

## Proyecto T — Universidad Diego Portales

Proyecto T is a free psychological care program for **trans and gender non-conforming individuals** operated by Universidad Diego Portales.

In this context, Routine Outcome Monitoring plays a crucial role in:

• evaluating the effectiveness of the intervention program
• generating empirical data about therapeutic outcomes
• supporting evidence-based responses to public criticism and misinformation about the program

MERICAPS facilitates the systematic collection and analysis of this clinical data.

---

## CLIP — Consorcio Latinoamericano de Investigación en Psicoterapia

Centro Médico Árbol and Proyecto T are both members of the **Consorcio Latinoamericano de Investigación en Psicoterapia (CLIP)**.

Within the consortium, participating centers conducted a needs assessment to identify technological barriers to implementing Routine Outcome Monitoring across Latin America.

MERICAPS emerged as a response to these identified needs, aiming to provide an accessible technological infrastructure that clinical centers in the region can adopt and adapt.

---

# User Roles

MERICAPS supports multiple user roles designed to reflect real clinical workflows within psychotherapy services and training environments.

---

## Administrator

Administrators are responsible for the overall configuration and management of the platform.

Administrators can:

• create, edit, and delete user accounts
• assign roles to professionals within the system
• create and manage clinical assessment instruments
• configure institutional settings

This role ensures institutions maintain **full control over their own system and data governance**.

---

## Supervisor

Supervisors oversee the clinical work of therapists.

Supervisors can:

• create and manage clinical assessment instruments
• access the patient lists of assigned therapists
• review patient responses and outcome trajectories
• monitor treatment progress across multiple therapists

This role supports **evidence-informed supervision**.

---

## Professionals (Therapists / Clinicians)

Therapists are responsible for the day-to-day clinical use of the platform.

Professionals can:

• manage patient rosters
• assign clinical assessments to patients
• review patient responses and progress over time
• use visual dashboards to monitor treatment trajectories

These features support **data-informed clinical decision-making**.

---

## Patients

Patients access a secure portal where they can:

• complete assigned psychological assessments
• track their progress across sessions

This creates greater **transparency in psychotherapy**, allowing patients and therapists to observe change trajectories together.

---

# Key Features

### Role-Based Access Control

Separate dashboards and permissions for each user role.

### Patient Management

Professionals can add, manage, and monitor patient records.

### Clinical Test Editor

Flexible interface for creating customized psychological assessments.

### Interactive Mural Dashboard

Visual overview of results and trends across patients.

### Data Migration Tools

Import clinical data from sources such as Google Sheets.

### Modern UI / UX

Responsive interface built using a component-based design system.

---

# Technology Stack

## Frontend

TypeScript
Next.js (React)
Tailwind CSS
Shadcn/UI component library

---

## Backend & Infrastructure

Google Firebase
Firestore (NoSQL database)
Firebase Authentication
Firebase App Hosting

---

# System Architecture

MERICAPS uses a **serverless architecture built on Next.js and the Firebase ecosystem**.

---

## Frontend

The user interface is implemented as a Next.js application responsible for:

• rendering the UI
• managing user interactions
• communicating with Firebase services

---

## Backend (Serverless)

### Firebase Authentication

Handles login and role-based access control.

### Firestore Database

Stores data including:

• patients
• clinical tests
• assessment responses
• treatment results

Real-time listeners allow live updates in the interface.

---

## Google App Hosting

Runs and deploys the Next.js application.

---

# AI Services (Planned)

The architecture allows future integration of **AI-based clinical analysis workflows using Google Genkit**.

These workflows could analyze patient response patterns and generate structured summaries to support clinical interpretation and supervision.

This functionality is **currently under development** and not active in production.

---

# Project Structure

```
.
├── src
│   ├── app/
│   ├── ai/
│   ├── components/
│   │   ├── auth/
│   │   ├── patient/
│   │   ├── professional/
│   │   └── ui/
│   ├── firebase/
│   ├── hooks/
│   └── lib/
│
├── firebase.json
├── apphosting.yaml
└── next.config.ts
```

---

# Installation

Clone repository

```
git clone https://github.com/felipeconcha-gif/mericaps.git
cd mericaps
```

Install dependencies

```
npm install
```

---

# Environment Configuration

Create a file named `.env.local` in the root of the project by copying the `.env` template. Then, fill in the values from your Firebase project.

```
# .env.local
NEXT_PUBLIC_FIREBASE_API_KEY="YOUR_API_KEY"
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN="YOUR_PROJECT_ID.firebaseapp.com"
NEXT_PUBLIC_FIREBASE_PROJECT_ID="YOUR_PROJECT_ID"
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET="YOUR_PROJECT_ID.appspot.com"
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID="YOUR_SENDER_ID"
NEXT_PUBLIC_FIREBASE_APP_ID="YOUR_APP_ID"
NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID="YOUR_MEASUREMENT_ID"
```

These values are available at: Firebase Console → Project Settings → General → Your apps → Web app.

---

# Running the Project

```
npm run dev
```

Open

```
http://localhost:3000
```

---

# Deployment

Install Firebase CLI

```
npm install -g firebase-tools
```

Login

```
firebase login
```

Initialize

```
firebase init hosting
```

Deploy

```
firebase deploy
```

---

# Example Workflow

1. Administrator creates user accounts
2. Supervisor assigns therapists
3. Therapist creates clinical assessments
4. Patient completes assessments
5. Results appear in real-time dashboards
6. Supervisor monitors treatment trajectories

---

# Impact & Vision

MERICAPS was designed not only as software, but as infrastructure supporting the development of a **data-informed psychotherapy culture in Latin America**.

If widely adopted, systems like MERICAPS could allow clinical centers across the region to:

• systematically measure psychotherapy outcomes
• improve clinical decision-making
• strengthen supervision and training processes
• evaluate mental health programs
• generate regional evidence about psychotherapy effectiveness

By lowering the barriers to implementing Routine Outcome Monitoring, MERICAPS aims to help Latin American institutions **generate their own data about psychotherapy outcomes**.

---

# Future Development

Potential extensions include:

• AI-assisted clinical summaries
• advanced visualization tools
• real-time notifications
• institutional analytics dashboards
• large-scale clinical deployment infrastructure

---

# Contributions
MERICAPS is currently maintained by the project creator.

If you are interested in collaborating, implementing MERICAPS in your institution, or contributing to its development, please contact:

felipeconcha@centroarbol.cl

---

# Términos de Uso y Reconocimiento

Al ser una infraestructura abierta y gratuita, el uso de MERICAPS está sujeto a las siguientes condiciones para asegurar el reconocimiento del trabajo original y la sostenibilidad del proyecto:

1.  **No cambiar el nombre de la plataforma.** El nombre "MERICAPS" debe ser mantenido en cualquier instancia que se despliegue.
2.  **Mantener el footer intacto.** El pie de página, que incluye los créditos al creador (Dr. Felipe Concha) y la institución patrocinante (Centro Médico Árbol), no debe ser modificado ni eliminado.
3.  **Mantener el botón de donaciones.** El botón "Buy me a coffee" debe permanecer visible y con su enlace original para apoyar el mantenimiento y desarrollo continuo de la plataforma.
4.  **Responsabilidad sobre los datos.** La configuración de la seguridad de los datos, así como la gestión de la privacidad y confidencialidad de la información clínica, es responsabilidad exclusiva de la persona o institución que despliega y utiliza la plataforma.

El cumplimiento de estos términos permite que MERICAPS siga siendo una herramienta accesible para la comunidad.

---

# License

Distributed under the **MIT License**.

See `LICENSE`.
