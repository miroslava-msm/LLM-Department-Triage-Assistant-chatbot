# Department Triage Assistant Chatbot Scenario

## User Profile
The target users are **Nova Scotians seeking healthcare services** who:
* Arrive at hospitals or clinics uncertain about which department or specialist to see
* Experience symptoms but are unsure if they need emergency care, urgent care, or specialist referral
* Are unfamiliar with how different medical departments handle specific conditions
* May be anxious about choosing the wrong department and facing additional delays
* Use mobile or web platforms to research healthcare options before visiting

## Problem Overview
Healthcare facilities across Halifax and Nova Scotia frequently see **misdirected patient visits**, where individuals present to inappropriate departments for their conditions. Patients with chest pain might go directly to cardiology instead of emergency care, while those with minor skin issues may visit the emergency department rather than dermatology or a walk-in clinic. This misdirection creates **bottlenecks in specialist departments**, **delays care for appropriate patients**, and increases **frustration and anxiety** for those seeking help. Current departmental information on hospital websites is often buried in complex navigation structures or written in medical terminology that patients find difficult to interpret.

## Proposed Solution
The proposed solution is a **locally hosted Department Triage Assistant chatbot**—powered by the Ollama + AnythingLLM stack—that:
* Uses **retrieval-augmented generation (RAG)** to access official Nova Scotia Health department guides and hospital resources
* **Maps common symptoms and conditions** to appropriate hospital departments and specialists
* Provides **clear explanations** of what each department handles (Emergency, Cardiology, Orthopedics, Mental Health, etc.)
* **Guides patients to the most appropriate starting point** for their healthcare concern
* Offers **alternative care pathways** when hospital departments aren't necessary (walk-in clinics, family physicians, telehealth)
* Includes **preparation guidance** for department visits (what to bring, what to expect)
* Maintains strict boundaries by **avoiding clinical diagnosis** and focusing on **navigation support**

## Success Criteria
The chatbot is successful if it can:

### 1. Accurately respond to core department triage questions:
* "I have persistent chest pain - should I go to Emergency or Cardiology first?"
* "My knee has been hurting for weeks after a fall - do I need Orthopedics or should I start elsewhere?"
* "I'm having trouble sleeping and feeling anxious - which department handles mental health concerns?"

### 2. Provide clear departmental guidance using uploaded hospital and Nova Scotia Health documents about:
* What conditions each department typically handles
* Referral requirements for specialist departments
* When emergency care is appropriate vs. scheduled appointments

### 3. Offer consistent, educational responses that:
* Include appropriate medical disclaimers
* Encourage consultation with healthcare providers for diagnosis
* Always prioritize emergency care for serious symptoms

### 4. Increase patient navigation efficiency by:
* Reducing misdirected visits to inappropriate departments
* Helping patients understand the healthcare system structure
* Providing preparation guidance for department visits

## Technologies Used
* **Ollama**: For running a local large language model (Mistral)
* **AnythingLLM**: For document ingestion, retrieval, and chatbot interface
* **Nova Scotia Health department guides, hospital websites, and specialist referral pathways**: As the knowledge base
* **Hospital directory information and departmental descriptions**: For comprehensive navigation support

## Ethical and Safety Notes
* The chatbot **strictly avoids medical diagnosis** and focuses solely on healthcare navigation
* Users experiencing **life-threatening symptoms** are immediately directed to call **911** or visit Emergency
* **Prominent disclaimers** emphasize that the tool provides guidance only, not medical advice
* All responses encourage **consultation with healthcare providers** for proper medical assessment
* The system **cannot replace clinical judgment** and serves only as an educational navigation tool
* **Privacy protection** ensures no personal health information is stored or transmitted

## Example Interaction Scenarios

### Scenario 1
**User Question**: "I have chest discomfort but also heartburn—should I see cardiology or gastroenterology?"

**Chatbot Response**: The chatbot explains that symptoms can have different causes and suggests visiting a family physician for proper referral or going to an emergency department if the symptoms worsen.

### Scenario 2
**User Question**: "What should I bring when I go to my specialist appointment?"

**Chatbot Response**: The chatbot explains all requirements to assist with the specialist appointment preparation.