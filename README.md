# Aarogya Aarohan Documentation

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Digital Public Good](https://img.shields.io/badge/DPG-Compliant-green.svg)](https://digitalpublicgoods.net/)
[![FHIR](https://img.shields.io/badge/FHIR-R4-orange.svg)](https://hl7.org/fhir/)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20Web%20%7C%20FHIR-brightgreen.svg)]()

Comprehensive documentation repository for Aarogya Aarohan, an open-source, FHIR-native digital healthcare platform.

---

## 📌 Overview

**Aarogya Aarohan** is a mobile phone-based app for screening subjects with oral suspicious lesions (Oral Potentially Malignant Disorders (OPMD) and oral cancer). It is developed by a consortium of 30 industry and academia partners led by the Indian Institute of Science.

The app is designed for front-line workers to screen for suspicious lesions in outreach programmes and opportunistic screening settings. It records demographic details, habit history, and oral cavity images. The data collected by the app is reviewed by Tele-specialists (Oral Medicine and Radiology/Oral Pathology specialists) for a provisional diagnosis and follow-up patient care.

The platform leverages the **HL7 FHIR** standard, Google's [Android FHIR SDK](https://github.com/google/android-fhir), and the [OpenSRP](https://github.com/opensrp) ecosystem.

---

## 📁 Repository Structure

```text
aarogya-aarohan-docs/
├── index.md                 # System overview and high-level platform flow
├── dpg/                     # Digital Public Good (DPG) submission & compliance package
│   ├── sdg-relevance.md     # Alignment with UN SDGs (SDG 3 & SDG 9)
│   ├── licensing.md         # Open source licensing (Apache License 2.0)
│   ├── platform-independence.md # Vendor neutrality and deployment flexibility
│   ├── installation-guide.md    # Technical deployment and reviewer setup
│   ├── data-export.md       # Non-PII data export and FHIR extraction
│   └── security-privacy.md  # Encryption, compliance, and privacy safeguards
├── engineering/             # In-depth technical architecture & developer guides
│   ├── android-app/         # Android mobile app (Kotlin, Jetpack Compose, MVVM)
│   ├── backend/             # Microservices, Keycloak IAM, HAPI FHIR server, and gateway
│   └── writing-fhir/        # SDC form authoring, FHIRPath, CQL, and resource definitions
├── features/                # Functional specifications & domain modules
│   ├── app-features/        # Mobile application capabilities for health workers
│   ├── admin-dashboard-features/ # Web portal for team & facility management
│   ├── supported-health-domains/ # Clinical modules (Oral Cancer Screening, etc.)
│   └── design/              # UI/UX principles, design system, and accessibility
├── project-information/     # Historical background, WHO SMART guidelines, and partners
```

---

## 🚀 Key Documentation Modules

### 1. Digital Public Good (DPG) Package (`dpg/`)
Documentation aligned with the [DPG Standard](https://www.digitalpublicgoods.net/submission-guide):
- [**SDG Relevance**](dpg/sdg-relevance.md): Direct contributions to Good Health & Well-being (SDG 3) and Industry, Innovation & Infrastructure (SDG 9).
- [**Platform Independence**](dpg/platform-independence.md): Zero vendor lock-in; deployable on any cloud or on-premise infrastructure.
- [**Data Export**](dpg/data-export.md): Standardized non-PII bulk export through FHIR APIs.
- [**Security & Privacy**](dpg/security-privacy.md): End-to-end data encryption at rest and in transit, RBAC, and healthcare regulatory compliance.
- [**Installation Guide**](dpg/installation-guide.md): Independent step-by-step verification instructions.

### 2. Engineering & Architecture (`engineering/`)
- **Android Application**:
  - Native Kotlin, MVVM architecture with Repository pattern, Jetpack Compose UI.
  - Offline-first storage powered by Google Android FHIR SDK (Room / SQLite database).
  - Dynamic Structured Data Capture (SDC) questionnaire rendering.
- **Backend & Cloud Services**:
  - Centralized Identity and Access Management (IAM) with **Keycloak**.
  - **HAPI FHIR** compliant data store with FHIR Gateway integrations.
  - Containerized production deployments via Docker and Kubernetes.
- **FHIR Resource Authoring**:
  - Clinical Quality Language (CQL) decision support.
  - FHIRPath expressions for validation and rule evaluations.
  - Custom Questionnaire, StructureMap, and PlanDefinition resource definitions.

### 3. Features & Health Domains (`features/`)
- **Oral Cancer Screening**: Specialized digital screening workflows, risk assessment questionnaires, and photographic capture for early screening.
- **Frontline Worker Support**: Task checklists, overdue patient tracking, and automated reminders for community health visits.
- **Administrative Portal**: Health system hierarchy configuration, user provisioning, and role assignment.

---

## 🛠️ Getting Started for Developers & Reviewers

1. **Prerequisites**:
   - Android Studio Hedgehog (or newer) & JDK 17+ for mobile development.
   - Docker & Docker Compose for local backend services (HAPI FHIR & Keycloak).
2. **Setup Instructions**:
   - Follow the detailed steps in [Installation Guide](installation-guide.md) to launch the stack locally.
   - Refer to [Android Developer Setup](engineering/android-app/developer-setup) for building the mobile APK.

---

## 🏛️ Contact

- **Contact**: `connect@artpark.in`

---

## 🤝 Contributing

Contributions, feedback, and issue reports are welcome! Please ensure any modifications to documentation or code maintain consistency with FHIR R4 specifications and DPG principles.
