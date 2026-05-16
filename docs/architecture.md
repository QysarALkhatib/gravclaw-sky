# OpenClaw Architecture

## Overview
OpenClaw is a hybrid AI agent system combining:
- **Local Skills Engine** (Antigravity + 40 skills)
- **Online Workflow Agents** (n8n, 24/7)
- **GitHub as Single Source of Truth**

## Components

### 1. Router (Local - Auto-activate)
- Path: `master-skill-engine/router/`
- Handles: task classification, todowrite tracking, skill chaining

### 2. Router-Online (On-demand)
- Path: `router-online/`
- Handles: n8n workflow agents (podcast, video, audio, social, research, monitor)

### 3. GitHub Workspace (Persistent)
- `workspace/research/` — intermediate research files (Single Source of Truth)
- `workspace/outputs/` — final deliverables
- `workspace/queue/` — task queue (pending → in-progress → completed)
- `workflows/` — n8n workflow JSON files
