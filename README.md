# CODEX-DeliverGuard
AI-powered multi-trigger insurance platform for delivery workers using real-time disruption data, zone-based risk scoring, and fraud detection to protect against income loss.

DeliverGuard – AI-Powered Insurance for Delivery Workers

1. Requirement, Persona & Workflow
Requirement
Delivery workers experience income loss due to external disruptions such as heavy rain, pollution, heatwaves, and curfews. These are uncontrollable and currently lack automated income protection.
DeliverGuard provides a parametric insurance solution that compensates workers based on real-time disruption triggers.

Persona
Name: Ravi
 Role: Food Delivery Partner (Swiggy/Zomato)
 Location: Chennai
Scenario:
 Ravi earns daily income through deliveries. During heavy rain or high AQI:
 Orders reduce
 Movement becomes unsafe
 Income drops significantly

Workflow

User registers and selects location
System assigns a delivery zone
Risk engine computes zone risk score
Weekly premium is generated
User subscribes to policy
System monitors real-time triggers
Trigger condition met → claim auto-generated
Fraud detection validates claim
Payout is processed (simulated)

2. Weekly Premium Model, Parametric Triggers & Platform Choice
Weekly Premium Model
Risk_Score = (
   0.3 * Rain_Risk +
   0.2 * AQI_Risk +
   0.2 * Heat_Risk +
   0.2 * Flood_Risk +
   0.1 * Social_Risk
)

Premium = 30 + (Risk_Score * 50)

Low risk → ₹40/week

Medium risk → ₹55/week

High risk → ₹70/week

Parametric Triggers

Trigger
Condition
Rainfall
> 80 mm
AQI
> 300
Temperature
> 40°C
Flood Alert
Active
Curfew
Zone restricted

These triggers are objective, real-time, and automated, ensuring zero manual claim filing.

Platform Choice

We use a Web application (React) because:
Enables interactive dashboards and risk maps
Faster development and deployment
Easier integration with backend APIs

3. AI/ML Integration

Risk Prediction
Predicts disruption probability for each zone

Inputs: weather, AQI, historical trends

Model: Linear Regression

Fraud Detection
Model: Isolation Forest
Detects:
GPS spoofing
Claims from unaffected zones
Duplicate claims
Weather mismatch
Example:
 Rain claim + no rainfall in API → claim rejected

4. Tech Stack & Development Plan

Tech Stack
Frontend: React.js
 Backend: Python (FastAPI)
 Database: PostgreSQL
 AI/ML: scikit-learn, pandas, numpy
 APIs: OpenWeatherMap, AQICN, mock APIs
 Payments: Razorpay/Stripe (sandbox)


6. Additional Relevant Features
   
Delivery Zone Risk Map: Visual heatmap showing risk levels and premium suggestions

Multi-Trigger Monitoring: Simultaneous tracking of weather, pollution, heat, and social disruptions

Automated Claims: Zero-touch claim processing with instant payouts

6. Conclusion
   
DeliverGuard is an AI-powered parametric insurance platform that provides:
Real-time disruption monitoring

Automated claim processing

Risk-based pricing

Fraud detection

It ensures financial protection and transparency for delivery workers.


