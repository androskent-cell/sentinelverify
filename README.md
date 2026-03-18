# SentinelVerify

**AI-Powered Platform for Synthetic Document Fraud Detection and Digital Integrity**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status: In Development](https://img.shields.io/badge/Status-In%20Development-yellow.svg)]()
[![Python](https://img.shields.io/badge/Python-3.10+-green.svg)]()
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)]()

---

## Overview

SentinelVerify is an AI-powered platform designed to detect and prevent synthetic document fraud across financial, governmental, and commercial sectors in the United States. It leverages advanced digital forensics, convolutional neural networks (CNNs), natural language processing (NLP), and metadata analysis to identify AI-generated forgeries in image-based files and PDFs.

### The Threat Landscape (2025–2026)

The rise of generative AI has democratized document fraud at an unprecedented scale. The following tools and platforms are actively being used by fraudsters to produce synthetic documents that bypass traditional verification systems — and SentinelVerify is built to detect artifacts from all of them:

#### Image & Document Generation
| Tool | Type | Threat |
|------|------|--------|
| **DALL·E 3** (OpenAI) | Image generation | Fake IDs, passports, certificates |
| **Midjourney** | Image generation | Realistic document templates |
| **Stable Diffusion** | Open-source image gen | Highly customizable fake documents |
| **Adobe Firefly** | Image generation | Professional-quality forgeries |
| **Ideogram** | Image generation | Text-accurate fake documents |
| **Flux (Black Forest Labs)** | Image generation | Photorealistic ID replication |
| **Leonardo.ai** | Image generation | Consistent fake identity photos |

#### Language & Text Generation (LLMs)
| Tool | Type | Threat |
|------|------|--------|
| **ChatGPT / GPT-4o** (OpenAI) | LLM | Fake invoices, contracts, medical records, résumés |
| **Gemini** (Google) | LLM | Synthetic text documents with high coherence |
| **Grok** (xAI) | LLM | Fabricated personal histories and employment records |
| **Claude** (Anthropic) | LLM | Convincing narrative-based fraud documents |
| **Llama 3** (Meta, open-source) | LLM | Fine-tuned forgery at scale with no usage restrictions |
| **Mistral** (open-source) | LLM | Low-cost mass document generation |
| **Copilot** (Microsoft) | LLM | Office-integrated document manipulation |

#### Specialized Fraud-as-a-Service Platforms
| Tool | Type | Threat |
|------|------|--------|
| **OnlyFake** | Underground fake ID service | Realistic digital IDs in minutes for $15 |
| **ProKYC** | Synthetic identity service | Fake docs + liveness check bypass videos |
| **Vondy** | AI ID card generator | Student/employee badge forgeries |
| **GAN-based dark web tools** | Generative adversarial networks | Bulk synthetic identity packages |
| **Telegram/Signal fraud bots** | Automated fraud services | On-demand document creation at scale |

#### Deepfake & Face Generation
| Tool | Type | Threat |
|------|------|--------|
| **FaceSwap** | Deepfake | Replacing photos on real IDs |
| **DeepFaceLab** | Deepfake | Video liveness spoofing |
| **Reface / Avatarify** | Face synthesis | Biometric bypass |
| **ThisPersonDoesNotExist** | GAN face generation | Synthetic identity photos |
| **ElevenLabs** | Voice cloning | Audio fraud and voice verification bypass |

> **According to Sumsub's 2025–2026 Identity Fraud Report**, deepfakes ranked among the top five fraud types in 2025. **TransUnion** reported U.S. lenders faced $3.3 billion in exposure to synthetic identities in H1 2025 alone — an 18% increase year-over-year.

---

## What SentinelVerify Detects

SentinelVerify is specifically engineered to identify the forensic signatures left by all of the above tools:

- **GAN artifacts** — checkerboard patterns, unnatural skin textures, background inconsistencies
- **Diffusion model fingerprints** — over-smoothed edges, spectral anomalies, frequency-domain artifacts
- **LLM text signatures** — uniform syntax, lexical coherence patterns, absence of natural errors
- **Metadata contradictions** — mismatched software history, missing EXIF data, invalid creation timestamps
- **Template inconsistencies** — font irregularities, alignment errors, compression artifacts in specific document zones
- **Cross-registry mismatches** — entity names, EINs, and addresses that don't exist in official databases

---

## Core Services

| Module | Description |
|--------|-------------|
| **Visual Fraud Detection** | CNN-based analysis of image textures, edge distortions, and compression artifacts |
| **NLP Text Analysis** | Detects AI-generated linguistic patterns using RoBERTa and BERT models |
| **Metadata Forensics** | Extracts and validates hidden file properties, timestamps, and digital signatures |
| **Cross-Verification Engine** | Real-time validation against official registries (IRS, OpenCorporates, etc.) |
| **Risk Scoring Dashboard** | Web-based interface with composite fraud risk rating and audit trails |
| **REST API** | RESTful endpoints for institutional integration and white-label deployment |
| **Compliance Module** | NIST AI RMF, FedRAMP, and AI Bill of Rights alignment |

---

## Tech Stack

- **Backend:** Python 3.10+, FastAPI, PyTorch, Hugging Face Transformers
- **Frontend:** HTML5, CSS3, JavaScript
- **Admin Panel:** PHP 8+
- **Database:** PostgreSQL
- **Infrastructure:** Docker, Nginx, AWS GovCloud / Google Cloud FedRAMP
- **AI Models:** CNNs (image forensics), RoBERTa/BERT (NLP), Ensemble classifiers

---

## Project Structure

```
sentinelverify/
├── frontend/        # Public-facing website and document upload interface
├── backend/         # Python FastAPI core — AI detection pipeline
├── admin/           # Administrative panel (PHP)
├── database/        # SQL schemas and migrations
├── models/          # AI model configurations and placeholders
└── README.md
```

---

## Use Cases

- **Banking** — Mobile check deposit fraud detection
- **Government (DMV)** — Identity document and passport verification
- **Insurance** — Claims invoice and medical record validation
- **E-Commerce** — Seller KYC onboarding
- **HR / Academia** — Academic credential and diploma authentication
- **Healthcare** — Fake medical record and prescription detection
- **Immigration** — Travel document and visa fraud prevention
- **Financial Aid** — Ghost student and enrollment fraud detection

---

## Algorithm Overview

```
verify_document(document_path):
  1. Preprocessing       → normalize image, OCR text, extract metadata
  2. Feature Extraction  → CNN visual features, NLP semantic features, metadata probabilities
  3. Ensemble Scoring    → concatenate vectors → meta-classifier → fraud_probability
  4. Cross-Verification  → validate against official registries → adjustment score
  5. Risk Score          → final_score = 0.7 * fraud_prob + 0.3 * verification_score
  6. Decision            → Authentic (< 0.6) | Suspicious (≥ 0.6)
```

---

## Roadmap

- [x] Project architecture and documentation
- [ ] MVP backend — FastAPI core pipeline
- [ ] Frontend — public landing page and document upload
- [ ] Admin panel — dashboard and case management
- [ ] CNN model integration (pre-trained)
- [ ] NLP model integration (RoBERTa / BERT)
- [ ] Metadata forensics engine
- [ ] Cross-verification API integrations
- [ ] Production deployment (VPS)
- [ ] Phase 1 launch — Florida pilot
- [ ] Phase 2 expansion — Texas, California, New York

---

## Compliance & Ethics

SentinelVerify is developed in alignment with:
- NIST AI Risk Management Framework (AI RMF)
- White House AI Bill of Rights
- FedRAMP cloud compliance standards
- CCPA, GLBA, and HIPAA data privacy requirements
- 2024 Critical and Emerging Technologies (CET) List — NSC/OSTP

---

## Author

**Andros K. Blandon Barahona**  
AI-Powered Software & Digital Security Strategist  
Sandy, Utah — United States

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.