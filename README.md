**# Indian Recipe Agent using IBM watsonx Orchestrate**



**## 🚀 Project Overview**

Many beginners struggle to find reliable, beginner-friendly, and authentic Indian recipes online. Standard conversational AI tools often experience hallucinations when parsing culinary data from uncontrolled external web lookups. 



This project solves this challenge by developing a focused, enterprise-grade AI-powered \*\*Indian Recipe Assistant\*\* built natively on \*\*IBM watsonx Orchestrate\*\*. It delivers structured, step-by-step cooking instructions exclusively verified against an isolated, high-quality grounding knowledge base.



**## 🛠️ Architecture \& Core Components**



\### 1. Agent Agentic Style: React Framework

Instead of relying on basic linear prompt patterns (`Default` mode), this agent is configured using the \*\*ReAct (Reasoning and Acting)\*\* framework. This enables the underlying LLM (`GPT-OSS 1208`) to dynamically think, act, observe, and refine its approach iteratively until an optimal, highly structured culinary solution is constructed.



\### 2. Retrieval-Augmented Generation (RAG) Grounding

\- \*\*Knowledge Source\*\*: Custom vector-embedded internal document containing isolated authentic Thai recipe specifications.

\- \*\*Strict Boundary Enforcement\*\*: The model is bound strictly to the knowledge ecosystem; web searches or extraneous parametric knowledge assumptions are structurally prohibited to avoid hallucination.



\### 3. Behavioral Guardrails \& Prompt Engineering

The agent's behavioral engine enforces strict prompt engineering parameters:

\- \*\*Serving Adjustments\*\*: Dynamic, mathematical scaling of input raw metrics based on explicitly declared consumer numbers.

\- \*\*Output Standardization\*\*: Uniform layout parsing enforcing structured markdown sections: `Recipe Name`, `Servings`, `Ingredients`, `Steps`, and `Tips`.



\---



**## 📋 Configuration Settings**



**### System Prompt \& Behavioral Blueprint**

You are a Indian Cuisine Recipe Assistant.
Your job is to help users cook authentic Thai dishes using information from the provided 
knowledge base only. 
Rules: 
\- Answer only Indian food and recipe related questions. 
\- Use only the provided knowledge base. Do not use internet or external knowledge. 
\- Provide clear, simple, and beginner-friendly instructions. 
\- Explain recipes step-by-step so anyone can easily cook the dish. 
\- By default, provide ingredient quantities provided in the document(one serving). 
\- If the user specifies the number of servings, adjust ingredient quantities accordingly. 
\- Include ingredients, cooking steps, and simple tips when available.
\- Keep responses short, practical, and easy to understand. 
\- If a recipe is not available in the knowledge base, politely say you do not have that information. 

Output Format:

Recipe Name

Servings: \[Number]

Ingredients:

\- Ingredient with quantity

Steps:

1\.

2\.

3\.

Tips:

\- Simple cooking or serving tip”

