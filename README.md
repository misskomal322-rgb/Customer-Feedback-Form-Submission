# Customer-Feedback-Form-Submission
This workflow is designed to intelligently process customer feedback submitted through a form and categorize it automatically using an AI agent. The automation identifies whether the feedback is a complaint, compliment, or a feature request, and then routes it into the correct workflow branch. Each category is stored in its respective Google Sheet, and team notifications are sent through Slack and Gmail—making feedback handling smooth, organized, and efficient.

🧠 How the Workflow Operates

The process starts when a customer submits feedback through the UserFeedbackForm. The submitted text is passed to an AI Agent, powered by the Google Gemini Chat Model, which analyzes the message and determines its correct category. This AI-driven classification eliminates manual sorting and ensures that every piece of feedback is handled accurately.

Both the raw input and the AI-generated output are then combined using a Merge node, keeping the customer’s original feedback and the AI analysis together. The combined data is passed into a Switch node, which uses rule-based routing to send the feedback to the correct path:

Complaints

Compliments

Feature Requests

Each path has its own Google Sheet where the data is appended for record-keeping.

🚀 What Happens After Categorization

Once the feedback is routed:

🟥 Complaint Path

Saved into the Complaints Sheet

A Slack message is sent to notify the support team

A Gmail message is triggered for escalation

🟩 Compliment Path

Stored in the Compliments Sheet

Team receives a Slack “positive feedback” notification

🟦 Feature Request Path

Logged in the Feature Requests Sheet

Slack notification sent to product/development team

This ensures each team receives exactly the updates they need—nothing extra, nothing missed.

🔍 Key Features

🔹 AI-powered classification using Google Gemini

🔹 Automated routing with the Switch node

🔹 Separate storage for complaints, compliments, and feature requests

🔹 Real-time Slack updates for immediate team visibility

🔹 Automated Gmail notification for urgent issues

🔹 Clean, organized data flow built for scalability

📚 Ideal Use Cases

Customer support teams

SaaS feedback management

Product improvement workflows

Automated ticket creation

Centralized customer experience reporting

🗂 Repository Contains

workflow.json — The exported n8n workflow

README.md — Complete documentation
