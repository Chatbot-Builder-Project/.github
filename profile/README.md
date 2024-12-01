# Chatbot Builder Platform

## Overview

The **Chatbot Builder Platform** is a drag-and-drop application that empowers users to create advanced,
interactive chatbots by combining structured logic workflows (like facebook bots) with dynamic, generative AI
capabilities (like chatgpt). This platform bridges the gap between traditional static chatbot builders and cutting-edge
generative AI tools, enabling users to design chatbots that are both deeply structured and highly interactive.

Checkout this diagram for an early look at the drag-and-drop builder design:
[Miro Link](https://miro.com/app/board/uXjVLIMWgVc=/?share_link_id=293187166089)

And the following is a UML diagram for the Workflow Schema:
[LucidChart Link](https://lucid.app/lucidchart/d16f99d0-b77c-4775-a268-9dd7e13e61d4/edit?viewport_loc=-1975%2C-1326%2C5637%2C2481%2CHWEp-vi-RSFO&invitationId=inv_739e5d58-0c53-414e-822e-1b6ec0848b59)

---

## Why This Platform?

The Chatbot Builder Platform is designed to address key challenges in chatbot development:

1. **Static vs. Generative**: Combines structured logic with dynamic interactivity.
2. **Ease of Use**: Enables non-technical users to create advanced LangChain chatbots visually with huge flexibility.

---

## Features

### 1. Hybrid Chatbot Design

- **Static Logic**: Supports structured workflows similar to traditional tools like Chatfuel.
- **Generative AI**: Utilizes LangChain for dynamic conversations and enhanced interactivity.
- **Drag-and-Drop Interface**: Provides an intuitive user experience for designing complex chatbot workflows.

### 2. Node-Based Workflow

Nodes represent functional units in a chatbot workflow, each with specific roles:

- **Static Node**: Stores constant values.
- **Input Node**: Captures user input.
- **Output Node**: Displays responses to users.
- **Prompt Node**: Text placeholders, injected dynamically at runtime.
- **Generation Node**: Executes generative AI task.
- **Switch Node**: Directs the workflow based on an option.
- **Smart Switch Node**: Directs the workflow based on a text.
- **Group Node**: Encapsulates reusable sub-flows for modular design.

### 3. Microservices Architecture

The platform consists of several microservices:

- **chatbot-builder-api**: API Gateway for authentication and service orchestration.
- **chatbot-builder-engine**: Manages workflows and node execution.
- **chatbot-builder-executor**: Executes LangChain logic for generative responses.
- **chatbot-builder-infra**: Handles deployment using Terraform and Kubernetes.
- **chatbot-builder-client**: Frontend built with React Native.
- **chatbot-builder-protos**: Protobuf definitions for efficient microservices communication.

---

## Key Technologies

- **Backend**:
    - **ASP.NET Core** for the API Gateway and Engine Service.
    - **Python**: Executor Service for LangChain integration.
    - **gRPC** for inter-service communication.
    - Infrastructure as Code with **Terraform** and **Kubernetes**.
- **Frontend**:
    - **React Native**: Drag-and-drop user interface.
    - Website and mobile app with **Expo**.
