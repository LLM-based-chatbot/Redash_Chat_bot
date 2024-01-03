# Redash Chat Add-on
This repository contains the frontend and backend code for the Redash Chat Add-on, a chat integration for Redash, an open-source data visualization and dashboard tool.

## 1. Introduction

The Redash Chat Add-on provides a seamless chat integration within Redash, allowing users to collaborate and discuss insights in real-time. This repository is organized into frontend and backend components, along with installation scripts and CI/CD workflows.

## 2. Installation

### 2.1 Prerequisites
- Docker
- Docker Compose
- Python

### 2.2 Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/alexa221/Redash_Chat_bot.git
   cd redash-chat-addon
### 3. Dependencies
poetry add openai

yarn add react-icons

yarn add react-syntax-highlighter
### 4. Integrating Plugin Files
Copy the entire client/app/components/chat folder to redash's client/app/components folder. 

Copy the entire redash/handlers/chat.py file to redash's redash/handlers folder. 

Now, integrate these two parts inside the Redash source code: 

Go to your Redash source code and locate the path client/app/components/ApplicationArea/ApplicationLayout/index.jsx. 

Copy and paste the following inside index.jsx:
import ChatBox from "@/components/chat/ChatBox";

// Existing code...



return (
  <React.Fragment>
    {/* Existing code... */}
    <div>
      <DynamicComponent name="ApplicationDesktopChat">
        <ChatBox />
      </DynamicComponent>
    </div>
    {/* Existing code... */}
  </React.Fragment>
);


