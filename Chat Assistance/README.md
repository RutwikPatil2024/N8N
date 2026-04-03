# AI Agent Workflow with OpenAI and Google Tasks

## Overview

This project demonstrates a simple AI agent workflow that processes incoming chat messages, uses an OpenAI chat model for responses, maintains memory, and interacts with Google Tasks.

## Workflow Description

1. Trigger: When Chat Message Received
   The workflow starts when a new chat message is received.

2. AI Agent
   Acts as the central processing unit.
   Handles user input and generates responses.
   Connects to:

   * OpenAI Chat Model (for intelligence)
   * Memory (to retain context)
   * Tools (for external integrations)

3. OpenAI Chat Model
   Provides natural language understanding and response generation.
   Connected as the main model for the AI agent.

4. Simple Memory
   Stores conversation context.
   Helps the agent remember previous interactions.

5. Google Tasks Integration
   Retrieves tasks using getAll: task.
   Enables task-related automation and responses.

## Features

* Real-time chat processing
* Context-aware responses using memory
* Integration with Google Tasks
* Modular and extensible design

## Use Cases

* Task management assistants
* Personal productivity bots
* Chat-based automation systems

## Requirements

* OpenAI API access
* Google Tasks API integration
* Workflow automation platform (such as n8n or similar)

## Setup

1. Configure OpenAI API credentials
2. Set up Google Tasks API access
3. Connect nodes as shown in the workflow
4. Enable memory storage
5. Activate the workflow

## Notes

* Ensure API keys are securely stored
* Memory can be replaced with advanced storage if needed
* Additional tools can be integrated into the AI Agent

## Author

Rutwik Patil
