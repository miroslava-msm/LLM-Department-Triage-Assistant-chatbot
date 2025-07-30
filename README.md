# Department Triage Assistant Chatbot

This project is a local, AI-powered chatbot that helps Nova Scotians navigate healthcare services by identifying the appropriate hospital department or specialist based on their symptoms and concerns. Built for the Halifax Regional Municipality and surrounding areas, the chatbot guides users to the right starting point for their healthcare needs while reducing misdirected visits and patient frustration.

The chatbot is built using the **Ollama + AnythingLLM** stack and retrieves information from local, authoritative Nova Scotia Health documents. It is designed as an educational navigation tool to help patients understand the healthcare system structure and prepare for their visits.

---

##  Features

- **Department Mapping**: Matches common symptoms and conditions to appropriate hospital departments
- **Specialist Guidance**: Explains what each department handles (Emergency, Cardiology, Orthopedics, Mental Health, etc.)
- **Referral Pathways**: Clarifies when specialist referrals are needed vs. direct visits
- **Visit Preparation**: Provides guidance on what to bring and what to expect at appointments
- **Alternative Care Options**: Recommends walk-in clinics, family physicians, or telehealth when appropriate
- **Document-backed Responses**: All answers are sourced from official Nova Scotia Health materials
- **Operates Entirely Locally**: No internet connection required for privacy and reliability
- **Educational Focus**: Maintains strict boundaries by avoiding medical diagnosis

---

##  Repository Structure

```text
department-triage-chatbot/
├─ knowledge_base/
│  ├─ knowledge_document_1.pdf    # Nova Scotia Health Department Descriptions
│  ├─ knowledge_document_2.md     # QEII Health Sciences Centre Service Directory
│  ├─ knowledge_document_3.txt    # Hospital Patient Preparation Guidelines
│  ├─ knowledge_document_4.pdf    # Specialist Referral Pathways
│  ├─ knowledge_document_5.txt    # Emergency vs. Urgent vs. Primary Care
│  └─ knowledge_document_6.md     # Mental Health Department Services
├─ prompt/
│  └─ system_prompt.txt
├─ documentation/
│  ├─ scenario_pack.md
│  └─ use_case_description.md
├─ demo/
│  ├─ demo_video.mp4
│  └─ chat_transcript.txt
└─ README.md
```

---

##  How to Run Locally

### 1. Install Ollama
- Download from [https://ollama.com/download](https://ollama.com/download)
- Run: `ollama run mistral` or `ollama run llama3`

### 2. Install AnythingLLM
- Download from [https://anythingllm.com/desktop](https://anythingllm.com/desktop)
- Configure your workspace and connect to Ollama at `http://127.0.0.1:11434`

### 3. Upload Documents
- Go to the Knowledge tab inside your AnythingLLM workspace
- Upload all files from the `/knowledge_base` folder
- Allow the system to process and embed the documents

### 4. Set the System Prompt
- Navigate to workspace settings in AnythingLLM
- Paste contents of `prompt/system_prompt.txt` into the system prompt field

### 5. Test the Chatbot
- Start with the core scenario questions:
  - "I have chest discomfort but also heartburn—should I see cardiology or gastroenterology?"
  - "What should I bring when I go to my specialist appointment?"

---

##  Sample Questions to Try

### Department Navigation
- "I have persistent chest pain - should I go to Emergency or Cardiology first?"
- "My knee has been hurting for weeks after a fall - do I need Orthopedics or should I start elsewhere?"
- "I'm having trouble sleeping and feeling anxious - which department handles mental health concerns?"

### Visit Preparation
- "What should I bring to my cardiology appointment?"
- "How do I prepare for an orthopedic consultation?"
- "What can I expect during my first visit to the Mental Health department?"

### System Navigation
- "Do I need a referral to see a specialist?"
- "What's the difference between Emergency and Urgent Care?"
- "When should I go to a walk-in clinic instead of the hospital?"

---

##  MEDICAL DISCLAIMER - NOT FOR MEDICAL DIAGNOSIS

**This chatbot provides general information about healthcare navigation and department services in Nova Scotia. The information is for educational purposes only.**

### This chatbot:
- **Does NOT provide medical advice, diagnosis, or treatment**
- **Is NOT a substitute for professional medical care**
- **Does NOT establish a doctor-patient relationship**
- **Should NOT be used in medical emergencies**
- **Cannot replace clinical judgment or professional medical assessment**

### Important Safety Information:
- **Always seek the advice of qualified healthcare professionals** regarding any medical condition
- **In case of life-threatening emergency, call 911** or go to your nearest emergency department immediately
- **All guidance provided is for navigation purposes only** and does not constitute medical advice
- **Consult with healthcare providers** for proper medical assessment and treatment decisions

**By using this chatbot, you acknowledge that it is an educational navigation tool only and agree to these terms.**

---

##  Educational Use Only

This project is developed for **educational research purposes only** and must not be used for real diagnosis or treatment. It demonstrates the application of RAG-based AI systems in healthcare navigation and patient education.

---

## Author(s)

- Mirna Saldierna - MBAN Program
- **Date**: July 2025

---

## License

This project is for educational use only. All Nova Scotia Health materials remain the property of their respective copyright holders.
