# ojesh
this is free AI agent promt
Upgrade my existing HumanAI project.

Core idea:
HumanAI is a simple, highly accessible AI agent that communicates naturally with humans and helps solve problems.

Add these capabilities:

1. SIMPLE MOBILE-FIRST UI
- Clean chat interface.
- Large readable text.
- Text input and Send button.
- Microphone button for voice input.
- Clear loading/thinking state.
- Make it responsive for mobile phones.
- Keep the interface simple and accessible.

2. AI AGENT
The backend should act as an agent, not just a basic chatbot.
It should:
- Understand the user's goal.
- Break complex requests into smaller steps.
- Decide when a tool is needed.
- Use the appropriate tool.
- Combine the results.
- Give the user a clear final answer.
- Never pretend it performed an action or searched the web when it did not.

3. COMPLEX PROBLEM SOLVING
Create an architecture that can handle multi-step tasks.
For example:
User request
→ understand goal
→ plan steps
→ execute tools
→ verify results
→ final response.

Start with safe tools such as:
- Calculator
- Date/time
- Web/current-information search if available
- A simple knowledge/retrieval tool

Do not add dangerous or unauthorized capabilities.

4. REAL-TIME ANSWERS
For questions requiring current information, use an actual search/API tool.
Do NOT rely only on the language model's stored knowledge.
Show a small indication when current information was retrieved.
Where possible, provide the source of current information.

5. VOICE ACCESS
Add browser-based voice input using the available Web Speech API or another appropriate browser-compatible approach.
Flow:
Microphone
→ speech-to-text
→ user message
→ AI agent
→ response
→ optional text-to-speech.

The website must gracefully handle browsers where speech recognition is unavailable.

6. API SECURITY
Never put API keys in frontend code.
Use environment variables/secrets on the backend.
Do not expose secrets to the browser.

7. ARCHITECTURE
Keep the code modular:
Frontend UI
Backend API
Agent/orchestrator
Tools
AI model provider
Optional memory/state

Before making major changes, inspect the existing project and explain:
- Current files
- Current technology
- What you will change
- Any dependencies you need

Do not delete the existing project unnecessarily.
Build a working MVP first, then improve it.