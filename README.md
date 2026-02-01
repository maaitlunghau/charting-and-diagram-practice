<div align="left">

# 📊 Data Visualization & Diagramming Practice

*A comprehensive practice repository for mastering data visualization, charts, and technical diagrams*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

</div>

<div align="left">

![Whimsical](https://img.shields.io/badge/Whimsical-6C63FF?style=for-the-badge&logo=whimsical&logoColor=white)
![Draw.io](https://img.shields.io/badge/Draw.io-F08705?style=for-the-badge&logo=diagramsdotnet&logoColor=white)
![Next AI Drawio](https://img.shields.io/badge/Next_AI_Drawio-000000?style=for-the-badge&logo=ai&logoColor=white)
![PlantUML](https://img.shields.io/badge/PlantUML-0080FF?style=for-the-badge&logo=plantuml&logoColor=white)
![Mermaid](https://img.shields.io/badge/Mermaid-FF3670?style=for-the-badge&logo=mermaid&logoColor=white)
![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=for-the-badge&logo=obsidian&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-74AA9C?style=for-the-badge&logo=openai&logoColor=white)
![Amazon Q](https://img.shields.io/badge/Amazon_Q-FF9900?style=for-the-badge&logo=amazon&logoColor=white)
![Claude AI](https://img.shields.io/badge/Claude_AI-181818?style=for-the-badge&logo=anthropic&logoColor=white)

</div>

---

## 🎯 Overview

This repository serves as a hands-on learning environment for developing proficiency in data visualization and technical diagramming. Through practical exercises and real-world scenarios, I'm building expertise in creating clear, impactful visual representations of complex data and system architectures.


## 🗂️ Repository Structure

```
charting-and-diagram-practice/
├── assets/                             # Exported images and screenshots
├── diagrams/                           # Source diagram files
│   ├── sequence-diagram/               # Sequence diagrams
│   └── system-architecture-diagram/    # Architecture designs
│       └── microservices.drawio
├── flowchart/                          # Process flowcharts
└── use-case/                           # Use case diagrams
```

## 🎨 Featured Diagrams

### System Architecture

#### 1. Microservices Architecture

<div align="center">
  <img src="assets/microservices.drawio.png" alt="Microservices Architecture Diagram" width="800"/>
  <p>
    <em>https://drive.google.com/file/d/1jIH5deTAiAN4S-mBDxl1IrkdK66DKw8W/view?usp=sharing</em>
  </p>
</div>

**Tools:** Gemini AI + Draw.io

**Description:** Microservices diagram with API Gateway as the main entry point, independent services with separate databases. This design makes it easy to scale individual services and deploy independently without affecting the entire system.

<br/>

<div align="center">
  <img src="assets/microservices.png" alt="Microservices Architecture Diagram" width="800"/>
  <p>
    <em>https://sunteco.vn/11-thanh-phan-quan-trong-trong-kien-truc-microservices-phan-1/</em>
  </p>
</div>

**Tools:** Reference diagram from Sunteco.vn

**Description:** Reference diagram from an article about 11 important components in microservices architecture. Includes service discovery, load balancer, circuit breaker, and monitoring - essential components for real-world microservices deployment.

<br/>

#### 2. Admin Service System Architecture

<div align="center">
  <img src="assets/admin-service-system-architecture.png" alt="Admin Service System Architecture Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Admin Service as central hub querying User, Order, Payment, and Job services. Each service has its own database for data isolation.

<br/>


<hr/>

### Sequence Diagrams

#### 1. Admin Dashboard Sequence Diagram

<div align="center">
  <img src="assets/admin-dashboard-sequence-diagram.png" alt="Admin Dashboard Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Admin opens dashboard and fetches statistics from User, Order, and Payment services through API calls. Each service returns data (user stats, order stats, revenue) which the frontend aggregates and displays.

<br/>

#### 2. Catalog Service Sequence Diagram

<div align="center">
  <img src="assets/catalog-service-sequence-diagram.png" alt="Catalog Service Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Three-step workflow: Client fetches platform list (Facebook, Instagram, TikTok), selects a platform to get available services (Like, Follow, Comment), then retrieves pricing packages for the chosen service.

<br/>

#### 3. User Service Sequence Diagram

<div align="center">
  <img src="assets/user-service-sequence-diagram.png" alt="User Service Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Complete user authentication flow in three steps: registration (email validation, create user and wallet), login (verify credentials, generate JWT token), and profile access (verify JWT, fetch user data and wallet balance from database and Redis cache).

<br/>

#### 4. Transaction Sequence Diagram

<div align="center">
  <img src="assets/transaction-sequence-diagram.png" alt="Transaction Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Payment flow from bank webhook to user notification. Bank sends transaction data, Payment Service processes it with database transaction (insert payment, update wallet, log transaction), invalidates Redis cache, and triggers notification to user.

<br/>

#### 5. Referral Commission Sequence Diagram

<div align="center">
  <img src="assets/referral-commission-sequence-diagram.png" alt="Referral Commission Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Referral commission flow in three steps: User B registers via User A's referral link, User B creates an order (Order Service fetches referral data and creates commission for User A), order completes and Payment Service adds commission to User A's wallet.

<br/>

#### 6. Notification Sequence Diagram

<div align="center">
  <img src="assets/notification-sequence-diagram.png" alt="Notification Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Real-time notification flow when order is created. Client creates order, Order Service saves it and sends notification event to Notification Service, which pushes the message to user via WebSocket for instant updates.

<br/>

#### 7. Post Ticket Sequence Diagram

<div align="center">
  <img src="assets/post-ticket-sequence-diagram.png" alt="Post Ticket Sequence Diagram" width="800"/>
</div>

**Tools:** Amazon Q + Mermaid.ai

**Description:** Support ticket workflow with real-time chat. User creates ticket, Admin views ticket list and connects via WebSocket for live chat. Messages are saved to database and pushed instantly to both parties. Admin closes ticket when resolved.

<br/>


<hr/>

### Use Case Diagrams

#### 1. Social Media Seeding Use Case

<div align="center">
  <img src="assets/social-media-seeding-use-case.png" alt="Social Media Seeding Use Case Diagram" width="800"/>
  <p>
    <em>https://drive.google.com/file/d/1kEJH04aHo2yVr6EVNVzh1GoZKhIKEugU/view?usp=sharing</em>
  </p>
</div>

**Tools:** Gemini AI + Draw.io

**Description:** Use case diagram for social media seeding system. Shows the workflow from content creation, scheduling posts, to performance analytics. Clear role separation between Admin and Seeder, with integration to social media platforms through APIs.

---

<div align="center">

**Built with 💙 for continuous learning and improvement**

*Last Updated: 2024*

</div>