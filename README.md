# Agentic-AI-Risk-Whisperer
Agentic AI Risk Whisperer is an intelligent risk management system designed to evaluate, track, and analyze organizational risks in real time
The system was built using Lovable for frontend interface development and CrewAI for backend agent orchestration and processing. RESTful APIs connect a structured database with predictive analytics modules to ensure seamless communication between user actions and AI-driven analysis.
The most challenging aspect of development was ensuring consistent, structured outputs from multiple AI agents. This was resolved through iterative prompt refinement, controlled testing cycles, and the implementation of a clear role-based agent architecture that enforced output discipline.

#  System Interface
<img width="932" height="437" alt="Screenshot 10000" src="https://github.com/user-attachments/assets/d3e77983-56a6-424d-ad7b-596a4a1dbcbd" />
<img width="940" height="440" alt="Screenshot 20000" src="https://github.com/user-attachments/assets/c431d118-80fb-4df2-8a2f-b259d5289e09" />

<img width="935" height="434" alt="Screenshot 3000" src="https://github.com/user-attachments/assets/72776287-502d-4716-a63d-f5bdfea5866f" />


 #  Architecture
The system follows a structured flow:
•	Frontend: Built with Lovable for responsive UI and interaction handling
•	Backend: CrewAI-powered agent orchestration
•	API Layer: RESTful APIs for communication between frontend and backend
•	Database: Structured storage for risks and AI-generated assessments
•	Analytics Layer: Predictive logic for risk scoring and classification

How It Works: 
1. Dashboard Overview:
The landing page provides a real-time snapshot of organizational risk posture:
•	Metric Cards: Total risks, Active, Mitigating, and Resolved counts
•	Risk Gauge: Overall risk score (0–10) with exposure level
•	Trend Chart: Risk volume over time
•	Category Breakdown: Cybersecurity, Operational, Compliance, Financial, Strategic, and HR
This gives decision-makers instant situational awareness.

2. Risk Registry
A searchable and filterable registry of tracked risks.
Users can:
•	Search by title, ID, category, or owner
•	Filter by risk level (Critical, High, Medium, Low)
•	Filter by status (Active, Mitigating, Resolved)
•	Expand a row to view description, owner, updates, and mitigations
This layer acts as the structured control center.

3. AI Risk Evaluation (Evaluate Candidate):
This is the core intelligence engine.
When Actions → Evaluate Candidate is clicked:
Step	Process
Kickoff	Risk data is sent to a CrewAI-powered backend via an edge function
Async Processing	CrewAI agents analyze severity, impact, likelihood, and mitigations
Polling	Frontend polls every 3 seconds showing progress, elapsed time, and poll count
Result	AI assessment appears inline within the risk row
Persistence	Assessment is saved to the database for future access

4. Data Flow:
User clicks Evaluate 
      ↓
Edge Function (Kickoff)
      ↓
CrewAI API processes risk
      ↓
Frontend polls for status
      ↓
Assessment returned
      ↓
Result displayed & stored in database

Current State:
• useRisks.ts` performs real CRUD against  database (insert, update, delete, select)
•  RLS policies scope data per authenticated user
•  Risk registry fully dynamic
•  AI evaluation results persist in the `evaluation_results` table via upsert
• 	Predictive risk forecasting
•	 Mitigation recommendation scoring

Next Iteration:
•	Connect to live enterprise data sources


#AgenticAI #EnterpriseAI  #RiskManagement  #CyberRisk  #RiskAnalytics  #BuildInPublic #TechInnovation
