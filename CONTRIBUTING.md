# Contributing to Ecom-Agent-Swarm

First off, thank you for considering contributing to Ecom-Agent-Swarm! This project relies on community collaboration to build robust, autonomous logistics workflows for e-commerce developers worldwide.

Whether you are fixing a bug, adding a new platform integration, or improving the LLM reasoning prompts, your help is deeply appreciated.

## How Can I Contribute?

### 1. Reporting Bugs & Requesting Features
If you find a bug or have an idea for a new feature (such as a new storefront integration), please open an Issue. 
* Use a clear and descriptive title.
* Include as much relevant context as possible (e.g., your Node.js or Python version, the specific platform API that failed, and the steps to reproduce).

### 2. Improving the Core Agents
The core of this project is the multi-agent orchestration. We are particularly looking for pull requests that address:
* **LLM Reliability:** Improvements to prompt engineering for the Reasoning Agent to minimize hallucinations during catalog metadata generation and copy standardization.
* **Webhook Handling:** Enhancing the Ingestion & Triage Agent to securely and efficiently handle high-volume webhook streams from active storefronts.
* **Logistics Routing:** Expanding the Context & Logistics Agent to support more regional shipping, courier APIs, and RTO prevention logic.

### 3. Submitting a Pull Request
1. **Fork the repository** and create your branch from `main`.
2. **Setup your environment** by copying `.env.example` to `.env` and adding your development API keys.
3. **Write tests** for your changes. Multi-agent workflows are complex; tests ensure new logic does not break existing routing rules.
4. **Ensure cross-compatibility** if you are modifying core infrastructure that bridges the Node.js ingestion layer and the Python reasoning scripts.
5. **Issue a Pull Request** with a detailed explanation of the changes and the specific operational problem it solves. 

## Development Setup
1. Clone the repo and install dependencies: `npm install` (and `pip install -r requirements.txt` for the Python modules).
2. Set up your environment variables (see `.env.example`).
3. Run the development server to test local webhooks.

## Code of Conduct
By participating in this project, you agree to maintain a welcoming, inclusive, and professional environment for all developers, regardless of their background or experience level.

Thank you for helping us scale e-commerce automation!