# OpenClaw Guide

This document provides the required information and commands for deploying and managing OpenClaw in a cloud environment.

---

## Project Structure

```md
3_OpenClaw
├── assets/          # Asset files (images, media, etc.)
├── results/         # Output data, logs, or test results
├── slides/          # Presentation slides or materials
├── Prompts.md       # Markdown file containing project prompts
└── README.md        # Project documentation (this file)
```

---

## Instance Information

**EC2 Instance**

- **Name:** `iris-openclaw-demo`
- **Key Pair:** `iris-openclaw-demo-key-pair`

---

# Prerequisites

## For Cloud Deployment

The following components are required to deploy OpenClaw in the cloud:

- AWS Account
- OpenAI API Key
- Discord Account

## For the Workshop / Demo

For this demonstration, only **Discord** is required.  

No additional setup is needed from participants.

---

# Installation

## Install OpenClaw

Run the following command on the target machine:

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

If the `openclaw` command is not available after installation:

```bash
source ~/.bashrc
```

---

# Configuration & Management

## Check Status

```bash
openclaw status
openclaw gateway status
```

## Update OpenClaw

```bash
openclaw update
```

## Update Configuration

```bash
openclaw configure
```

## Manage Automations

```bash
# List all automation jobs
openclaw cron list

# Remove a specific automation job
openclaw cron rm <job-id>
```

## Restart Gateway

After any configuration change, restart the gateway:

```bash
openclaw gateway
```

---

# Agent Management

## Add a New Agent

```bash
openclaw agents add <agent-name>
```

---

### Dashboard URL

```text
http://127.0.0.1:18789/#token=<GATEWAY_TOKEN>
```

### Retrieve Gateway Token

If you do not know the gateway token:

```bash
cat ~/.openclaw/openclaw.json
```

Locate the value associated with:

```json
gateway_token
```

---

# Server Access

## SSH into the Instance

```bash
ssh -i "iris-openclaw-demo-key-pair.pem" ubuntu@<PUBLIC-IP-V4>
```

---

# File Transfer

## Download Files from the Server

### Windows

```bash
scp -i "iris-openclaw-demo-key-pair.pem" ubuntu@<PUBLIC-IP-V4>:/home/ubuntu/.openclaw/workspace/<PATH_TO_FILE> "C:/Users/<USER>/Downloads"
```

### macOS / Linux

```bash
scp -i "iris-openclaw-demo-key-pair.pem" ubuntu@<PUBLIC-IP-V4>:/home/ubuntu/.openclaw/workspace/<PATH_TO_FILE> ~/Downloads/
```

---

# OpenAI Configuration

Set your OpenAI API key:

```bash
OPENAI_API_KEY="YOUR_OPENAI_API_KEY"
```

---

# Discord Configuration

## Discord Developer Portal

https://discord.com/developers/applications

Create a Discord application and bot, then configure the following values:

```bash
APP_NAME="OpenClaw_Demo"
DISCORD_BOT_TOKEN="YOUR_DISCORD_BOT_TOKEN"
```

---

# Quick Start Checklist

- [ ] Launch EC2 instance
- [ ] Connect via SSH
- [ ] Install OpenClaw
- [ ] Configure OpenAI API key
- [ ] Create Discord application and bot
- [ ] Configure OpenClaw settings
- [ ] Start the gateway
- [ ] Create an SSH tunnel
- [ ] Access the dashboard

---

**End of Document**