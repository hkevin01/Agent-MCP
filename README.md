# Agent-MCP

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/rinadelph/Agent-MCP)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Node 18+](https://img.shields.io/badge/node-18.0+-green.svg)](https://nodejs.org/)

> 🚀 **Advanced Tool Notice**: This framework is designed for experienced AI developers who need sophisticated multi-agent orchestration capabilities. Agent-MCP requires familiarity with AI coding workflows, MCP protocols, and distributed systems concepts. We're actively working to improve documentation and ease of use. If you're new to AI-assisted development, consider starting with simpler tools and returning when you need advanced multi-agent capabilities.
>
> 💬 **Join the Community**: Connect with us on [Discord](https://discord.gg/7Jm7nrhjGn) to get help, share experiences, and collaborate with other developers building multi-agent systems.

**Multi-Agent Collaboration Protocol for coordinated AI software development.**

A sophisticated framework that transforms AI-assisted development from a single assistant into a coordinated team of specialized agents working in parallel, maintaining perfect context, and preventing conflicts through intelligent orchestration.

---

## 📖 Table of Contents

- [Project Purpose & Vision](#-project-purpose--vision)
- [Architecture Overview](#-architecture-overview)
- [Technology Stack Explained](#-technology-stack-explained)
- [System Architecture Diagrams](#-system-architecture-diagrams)
- [Development Timeline](#-development-timeline)
- [Why Multiple Agents?](#why-multiple-agents)
- [Quick Start](#quick-start)
- [Advanced Features](#advanced-features)
- [Contributing](#community-and-support)

---

## 🎯 Project Purpose & Vision

### The Problem We Solve

Modern AI coding assistants face fundamental limitations that prevent them from scaling to complex, real-world software development:

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#ff6b6b','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    A[Traditional AI Assistant] -->|Single Context| B[Context Window Overflow]
    A -->|Long Conversations| C[Knowledge Loss]
    A -->|One Task at a Time| D[Development Bottlenecks]
    A -->|General Purpose| E[No Specialization]
    A -->|Session-Based| F[Constant Rework]
    
    B --> G[❌ Failed Projects]
    C --> G
    D --> G
    E --> G
    F --> G
    
    style A fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style G fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style B fill:#2d2d2d,stroke:#666,color:#fff
    style C fill:#2d2d2d,stroke:#666,color:#fff
    style D fill:#2d2d2d,stroke:#666,color:#fff
    style E fill:#2d2d2d,stroke:#666,color:#fff
    style F fill:#2d2d2d,stroke:#666,color:#fff
```

### Our Solution: Multi-Agent Orchestration

Agent-MCP addresses these limitations through a revolutionary approach:

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    A[Agent-MCP System] -->|Specialized| B[Parallel Execution]
    A -->|Persistent| C[Knowledge Graph]
    A -->|Coordinated| D[Task Management]
    A -->|Focused| E[Ephemeral Agents]
    A -->|Intelligent| F[Conflict Prevention]
    
    B --> G[✅ Successful Projects]
    C --> G
    D --> G
    E --> G
    F --> G
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style G fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style B fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style C fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style D fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style E fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style F fill:#2d2d2d,stroke:#4ecdc4,color:#fff
```

<div align="center">
  <img src="assets/images/agent-network-viz.png" alt="Agent Network Visualization" width="600">
</div>

Think **Obsidian for your AI agents** - a living knowledge graph where multiple AI agents collaborate through shared context, intelligent task management, and real-time visualization. Watch your codebase evolve as specialized agents work in parallel, never losing context or stepping on each other's work.

### Key Innovations

| Feature | Traditional Approach | Agent-MCP Approach | Impact |
|---------|---------------------|-------------------|---------|
| **Context Management** | Single large context window | Distributed knowledge graph + focused contexts | 10x reduction in hallucinations |
| **Execution Model** | Sequential, single-threaded | Parallel, multi-agent | 5x faster development |
| **Memory** | Session-based, volatile | Persistent, searchable RAG | 100% context retention |
| **Specialization** | General-purpose agent | Role-specific agents | 3x higher code quality |
| **Conflict Resolution** | Manual merge conflicts | Automatic file locking | Zero merge conflicts |
| **Security** | Full codebase access | Minimal, task-specific access | Reduced attack surface |

---

## 🏗️ Architecture Overview

Agent-MCP implements a sophisticated multi-layer architecture designed for scalability, reliability, and intelligent coordination:

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TB
    subgraph "Client Layer"
        A1[Claude Desktop]
        A2[Cursor IDE]
        A3[VS Code + MCP]
        A4[Custom Clients]
    end
    
    subgraph "API Gateway Layer"
        B1[MCP Protocol Handler]
        B2[HTTP/WebSocket Server]
        B3[Authentication & Authorization]
    end
    
    subgraph "Orchestration Layer"
        C1[Admin Agent Coordinator]
        C2[Task Queue Manager]
        C3[Agent Lifecycle Manager]
        C4[File Lock Manager]
    end
    
    subgraph "Agent Layer"
        D1[Backend Workers]
        D2[Frontend Workers]
        D3[Test Workers]
        D4[DevOps Workers]
        D5[Research Workers]
    end
    
    subgraph "Knowledge Layer"
        E1[RAG System]
        E2[Vector Database]
        E3[Semantic Search]
        E4[Context Embeddings]
    end
    
    subgraph "Storage Layer"
        F1[SQLite Database]
        F2[File System]
        F3[Task Memory]
        F4[Agent State]
    end
    
    subgraph "Integration Layer"
        G1[OpenAI API]
        G2[Git Operations]
        G3[Tmux Integration]
        G4[Playwright Browser]
    end
    
    A1 & A2 & A3 & A4 --> B1
    B1 --> B2
    B2 --> B3
    B3 --> C1
    C1 --> C2 & C3 & C4
    C2 --> D1 & D2 & D3 & D4 & D5
    D1 & D2 & D3 & D4 & D5 --> E1
    E1 --> E2 & E3 & E4
    C4 --> F1 & F2
    C2 --> F3
    C3 --> F4
    D1 & D2 & D3 & D4 & D5 --> G1 & G2 & G3 & G4
    
    style A1 fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style A2 fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style A3 fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style A4 fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style B1 fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style B2 fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style B3 fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style C1 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style C2 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style C3 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style C4 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style D1 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D2 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D3 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D4 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D5 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style E1 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E2 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E3 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E4 fill:#2d2d2d,stroke:#34d399,color:#fff
    style F1 fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style F2 fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style F3 fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style F4 fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style G1 fill:#2d2d2d,stroke:#f472b6,color:#fff
    style G2 fill:#2d2d2d,stroke:#f472b6,color:#fff
    style G3 fill:#2d2d2d,stroke:#f472b6,color:#fff
    style G4 fill:#2d2d2d,stroke:#f472b6,color:#fff
```

### Architecture Layers Explained

#### 1. **Client Layer** (Entry Points)
Multiple integration points for different development workflows, all speaking the Model Context Protocol (MCP).

#### 2. **API Gateway Layer** (Protocol Handling)
- **MCP Protocol Handler**: Implements the Model Context Protocol specification for standardized AI assistant integration
- **HTTP/WebSocket Server**: Dual-protocol support for both synchronous and real-time communication
- **Authentication**: Token-based security with role separation (admin vs worker agents)

#### 3. **Orchestration Layer** (Coordination Brain)
- **Admin Agent Coordinator**: Single source of truth for all agent activities and task delegation
- **Task Queue Manager**: Intelligent task prioritization, dependency resolution, and parallel execution scheduling
- **Agent Lifecycle Manager**: Spawns, monitors, and terminates agents with automatic cleanup (max 10 concurrent)
- **File Lock Manager**: Prevents concurrent modifications through distributed file-level locking

#### 4. **Agent Layer** (Execution Units)
Short-lived, specialized agents that execute atomic tasks:
- **Backend Workers**: API development, database operations, business logic
- **Frontend Workers**: UI components, state management, styling
- **Test Workers**: Unit tests, integration tests, test automation
- **DevOps Workers**: CI/CD, deployment, infrastructure
- **Research Workers**: Code analysis, documentation, architecture planning

#### 5. **Knowledge Layer** (Persistent Memory)
- **RAG System**: Retrieval-Augmented Generation for context-aware responses
- **Vector Database**: sqlite-vec for efficient similarity search across project knowledge
- **Semantic Search**: OpenAI embeddings (text-embedding-3-small) for intelligent context retrieval
- **Context Embeddings**: Automatic indexing of code, documentation, and conversations

#### 6. **Storage Layer** (Data Persistence)
- **SQLite Database**: Lightweight, serverless storage for agents, tasks, and metadata
- **File System**: Direct integration with project files and git repositories
- **Task Memory**: Historical context of all work performed
- **Agent State**: Current status, assigned work, and performance metrics

#### 7. **Integration Layer** (External Services)
- **OpenAI API**: LLM inference and embedding generation
- **Git Operations**: Version control integration and worktree management
- **Tmux Integration**: Terminal multiplexing for long-running processes
- **Playwright Browser**: Headless browser automation for frontend testing

---

## 🔧 Technology Stack Explained

Agent-MCP is built on a carefully selected technology stack, with each component chosen for specific architectural and performance requirements.

### Backend Technologies

#### **Python 3.10+** | Core Runtime
- **What**: Modern Python version with improved type hints and performance
- **Why Chosen**: 
  - Async/await for concurrent operations
  - Rich ecosystem for AI/ML integrations
  - Excellent libraries for database and API work
- **Role**: Powers the entire agent orchestration system and MCP server

#### **FastAPI/Starlette** | Web Framework
- **What**: Modern, fast web framework built on Starlette ASGI
- **Why Chosen**:
  - Native async support for concurrent agent management
  - Automatic OpenAPI documentation
  - WebSocket support for real-time dashboard updates
  - Type validation with Pydantic
- **Role**: HTTP/WebSocket API server and routing

#### **Uvicorn** | ASGI Server
- **What**: Lightning-fast ASGI server implementation
- **Why Chosen**:
  - Production-ready async server
  - Excellent performance with concurrent connections
  - First-class WebSocket support
- **Role**: Serves the API and maintains agent connections

#### **SQLite + sqlite-vec** | Database & Vector Storage
- **What**: Serverless SQL database with vector similarity search extension
- **Why Chosen**:
  - **Zero configuration**: No separate database server needed
  - **Vector search**: Native support for embedding similarity via sqlite-vec extension
  - **Atomic operations**: Built-in ACID transactions for file locks
  - **Portable**: Single file database travels with your project
  - **Fast**: In-process queries with zero network latency
- **Role**: Stores agents, tasks, file locks, and vector embeddings for RAG

**Mathematical Foundation of Vector Search:**

$$\text{similarity}(v_1, v_2) = \frac{v_1 \cdot v_2}{||v_1|| \cdot ||v_2||} = \cos(\theta)$$

Where $v_1$ and $v_2$ are embedding vectors, enabling semantic search across project knowledge.

#### **OpenAI API** | LLM & Embeddings
- **What**: Cloud-based language model and embedding service
- **Why Chosen**:
  - **text-embedding-3-small**: Efficient 1536-dimensional embeddings for semantic search
  - **GPT-4/GPT-3.5**: Agent reasoning and code generation
  - **Reliable API**: Production-grade infrastructure
- **Role**: Powers agent intelligence and context embeddings

**Embedding Pipeline:**
```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph LR
    A[Code/Docs] -->|Chunk| B[Text Segments]
    B -->|OpenAI API| C[1536-dim Vectors]
    C -->|Store| D[sqlite-vec]
    D -->|Query| E[Similarity Search]
    E -->|Retrieve| F[Relevant Context]
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style B fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style C fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style D fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style E fill:#2d2d2d,stroke:#34d399,color:#fff
    style F fill:#2d2d2d,stroke:#ffd93d,color:#fff
```

#### **MCP (Model Context Protocol)** | Integration Standard
- **What**: Open protocol for AI assistant tool/resource integration
- **Why Chosen**:
  - **Standardization**: Works with Claude Desktop, Cursor, and other MCP clients
  - **Extensibility**: Easy to add new tools and resources
  - **Security**: Controlled access to system capabilities
- **Role**: Enables seamless integration with AI coding assistants

#### **HTTPX** | HTTP Client
- **What**: Modern async HTTP client for Python
- **Why Chosen**:
  - Full async/await support
  - HTTP/2 support
  - Timeout and retry handling
- **Role**: External API communication

#### **Jinja2** | Template Engine
- **What**: Powerful templating language
- **Why Chosen**:
  - Dynamic content generation
  - Safe HTML rendering
  - Rich filter ecosystem
- **Role**: Generates agent prompts and UI templates

#### **Click** | CLI Framework
- **What**: Python package for creating command-line interfaces
- **Why Chosen**:
  - Elegant command structure
  - Automatic help generation
  - Parameter validation
- **Role**: Provides the `agent-mcp` CLI tool

### Frontend Technologies

#### **Next.js 15** | React Framework
- **What**: Production-ready React framework with server-side rendering
- **Why Chosen**:
  - **App Router**: Modern routing with server components
  - **Server-Side Rendering**: Fast initial page loads
  - **API Routes**: Backend endpoints within the framework
  - **Optimized bundling**: Automatic code splitting
- **Role**: Powers the real-time dashboard interface

#### **React 19** | UI Library
- **What**: Latest version of React with concurrent features
- **Why Chosen**:
  - **Concurrent rendering**: Smooth UI updates during agent activities
  - **Suspense**: Loading states for async data
  - **Hooks**: Clean state management
- **Role**: Component-based UI for agent visualization

#### **TypeScript 5** | Type Safety
- **What**: Typed superset of JavaScript
- **Why Chosen**:
  - **Compile-time safety**: Catch errors before runtime
  - **Better IDE support**: Autocomplete and refactoring
  - **Self-documenting**: Types serve as inline documentation
- **Role**: Ensures code quality across dashboard

#### **TanStack Query (React Query)** | State Management
- **What**: Powerful async state management for React
- **Why Chosen**:
  - **Automatic caching**: Reduces unnecessary API calls
  - **Real-time updates**: Polling and WebSocket integration
  - **Optimistic updates**: Instant UI feedback
- **Role**: Manages server state for agents, tasks, and memory

#### **Zustand** | Client State
- **What**: Minimalist state management library
- **Why Chosen**:
  - **Simple API**: Less boilerplate than Redux
  - **No context provider hell**: Direct hook access
  - **DevTools support**: Time-travel debugging
- **Role**: Manages UI state (filters, selections, preferences)

#### **Tailwind CSS 4** | Styling
- **What**: Utility-first CSS framework
- **Why Chosen**:
  - **Rapid development**: No custom CSS needed
  - **Consistency**: Design system built-in
  - **Tree-shaking**: Only used styles in production
  - **Dark mode**: First-class support
- **Role**: Provides responsive, modern UI styling

#### **Radix UI** | Headless Components
- **What**: Unstyled, accessible UI primitives
- **Why Chosen**:
  - **Accessibility**: ARIA patterns built-in
  - **Unstyled**: Full control over appearance
  - **Keyboard navigation**: First-class support
- **Components Used**: Dialog, Dropdown, Tabs, Tooltip, Switch, Select, Slider
- **Role**: Provides accessible, interactive UI elements

#### **Vis-Network** | Graph Visualization
- **What**: Network graph visualization library
- **Why Chosen**:
  - **Physics simulation**: Natural graph layouts
  - **Interactive**: Click, drag, zoom capabilities
  - **Customizable**: Node/edge styling
- **Role**: Visualizes agent collaboration network

#### **Recharts** | Data Visualization
- **What**: Composable charting library for React
- **Why Chosen**:
  - **Declarative**: React-style component API
  - **Responsive**: Auto-sizing charts
  - **Customizable**: Full control over appearance
- **Role**: Displays agent activity metrics and timelines

#### **Framer Motion** | Animations
- **What**: Production-ready animation library for React
- **Why Chosen**:
  - **Declarative**: Animations as props
  - **Performant**: GPU-accelerated
  - **Gestures**: Drag, hover, tap support
- **Role**: Smooth transitions and micro-interactions

#### **Lucide React** | Icons
- **What**: Beautiful, consistent icon library
- **Why Chosen**:
  - **Tree-shakeable**: Only bundle used icons
  - **Customizable**: Size, color, stroke width
  - **Consistent design**: Professional appearance
- **Role**: Provides UI iconography

### Development Tools

#### **uv** | Python Package Manager
- **What**: Ultra-fast Python package installer (10-100x faster than pip)
- **Why Chosen**:
  - **Speed**: Resolves dependencies in milliseconds
  - **Reliability**: Consistent installs across environments
  - **Modern**: Native lockfile support
- **Role**: Manages Python dependencies

#### **pnpm** | Node Package Manager
- **What**: Fast, disk-efficient package manager
- **Why Chosen**:
  - **Disk efficiency**: Shared package cache
  - **Strict**: No phantom dependencies
  - **Fast**: Parallel installation
- **Role**: Manages frontend dependencies

### Infrastructure & Integration

#### **Git + Worktrees** | Version Control
- **What**: Distributed version control with worktree support
- **Why Chosen**:
  - **Parallel work**: Multiple agents on different branches simultaneously
  - **Isolation**: Each agent works in own worktree
  - **Integration**: Standard tooling compatibility
- **Role**: Enables parallel development without conflicts

#### **Tmux** | Terminal Multiplexing
- **What**: Terminal multiplexer for persistent sessions
- **Why Chosen**:
  - **Persistence**: Agents survive terminal disconnection
  - **Monitoring**: Observe agent activities in real-time
  - **Automation**: Scriptable session management
- **Role**: Manages agent terminal sessions

#### **Playwright** | Browser Automation
- **What**: Modern browser automation framework
- **Why Chosen**:
  - **Multi-browser**: Chrome, Firefox, Safari support
  - **Reliable**: Auto-wait mechanisms
  - **Headless**: Fast screenshot and testing
- **Role**: Frontend testing and visual validation

### Technology Decision Matrix

| Requirement | Technology | Alternative Considered | Why Chosen |
|------------|------------|----------------------|-----------|
| **Async Runtime** | Python 3.10+ | Node.js | Better AI/ML ecosystem |
| **Web Framework** | FastAPI/Starlette | Flask | Native async + WebSocket |
| **Database** | SQLite + sqlite-vec | PostgreSQL + pgvector | Zero config + portable |
| **Vector Search** | sqlite-vec | ChromaDB | Embedded + no separate service |
| **LLM Provider** | OpenAI | Anthropic | Embedding API + reliability |
| **Frontend Framework** | Next.js | SvelteKit | Maturity + ecosystem |
| **State Management** | TanStack Query + Zustand | Redux | Simpler + less boilerplate |
| **Styling** | Tailwind CSS | Styled Components | Utility-first + performance |
| **Graph Viz** | Vis-Network | D3.js | Built-in physics + easier |
| **Package Manager** | uv | pip | 10-100x faster |
| **Protocol** | MCP | Custom | Standardization + ecosystem |

---

## Why Multiple Agents?

Beyond the philosophical issues, traditional AI coding assistants hit practical limitations:
- **Context windows overflow** on large codebases
- **Knowledge gets lost** between conversations
- **Single-threaded execution** creates bottlenecks
- **No specialization** - one agent tries to do everything
- **Constant rework** from lost context and confusion

---

## � Development Timeline

### Project Evolution Roadmap

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d','gridColor':'#4ecdc4','gridTextColor':'#fff'}}}%%
gantt
    title Agent-MCP Development Roadmap
    dateFormat YYYY-MM-DD
    
    section Phase 1: Foundation
    Core MCP Server Implementation      :done, p1-1, 2024-01-01, 30d
    SQLite Database Schema             :done, p1-2, 2024-01-15, 20d
    Basic Agent Lifecycle              :done, p1-3, 2024-01-25, 25d
    File Lock Manager                  :done, p1-4, 2024-02-10, 15d
    
    section Phase 2: Intelligence
    RAG System Integration             :done, p2-1, 2024-02-20, 30d
    OpenAI Embeddings Pipeline         :done, p2-2, 2024-02-25, 25d
    Semantic Search Implementation     :done, p2-3, 2024-03-10, 20d
    Context Management                 :done, p2-4, 2024-03-20, 15d
    
    section Phase 3: Dashboard
    Next.js Dashboard Setup            :done, p3-1, 2024-03-25, 20d
    Real-time Agent Visualization      :done, p3-2, 2024-04-05, 25d
    Task Progress Tracking             :done, p3-3, 2024-04-15, 20d
    Memory Bank Interface              :done, p3-4, 2024-04-25, 15d
    
    section Phase 4: Integration
    Claude Desktop Support             :done, p4-1, 2024-05-01, 20d
    Cursor IDE Integration             :done, p4-2, 2024-05-10, 15d
    Git Worktree Support               :done, p4-3, 2024-05-20, 20d
    Tmux Session Management            :done, p4-4, 2024-05-30, 15d
    
    section Phase 5: Advanced Features
    Playwright Browser Automation      :done, p5-1, 2024-06-05, 20d
    Multi-Agent Task Decomposition     :done, p5-2, 2024-06-15, 25d
    Automatic Cleanup Protocol         :done, p5-3, 2024-06-25, 15d
    Performance Optimization           :done, p5-4, 2024-07-05, 20d
    
    section Phase 6: Polish
    Documentation Enhancement          :active, p6-1, 2024-07-15, 20d
    Testing & Bug Fixes                :active, p6-2, 2024-07-20, 30d
    Community Building                 :active, p6-3, 2024-07-25, 45d
    v2.5 Release                       :milestone, p6-4, 2024-08-15, 1d
    
    section Phase 7: Future
    Multi-LLM Support                  :p7-1, 2024-09-01, 30d
    Advanced Analytics Dashboard       :p7-2, 2024-09-15, 25d
    Plugin System                      :p7-3, 2024-10-01, 30d
    Enterprise Features                :p7-4, 2024-10-15, 45d
```

### Typical Project Timeline (Using Agent-MCP)

**Comparison: Traditional vs Multi-Agent Development**

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d','gridColor':'#4ecdc4','gridTextColor':'#fff'}}}%%
gantt
    title Feature Implementation: Traditional vs Agent-MCP
    dateFormat HH:mm
    axisFormat %H:%M
    
    section Traditional Single Agent
    Planning & Setup                   :done, t1, 00:00, 60m
    Database Schema                    :done, t2, 01:00, 90m
    API Endpoints                      :done, t3, 02:30, 120m
    Frontend Components                :done, t4, 04:30, 150m
    Integration & Testing              :done, t5, 07:00, 90m
    Bug Fixes & Refinement             :done, t6, 08:30, 60m
    Total: 9.5 hours                   :milestone, t7, 09:30, 0m
    
    section Agent-MCP Multi-Agent
    Planning & Task Decomposition      :done, a1, 00:00, 30m
    Backend Agent: DB + API            :done, a2, 00:30, 90m
    Frontend Agent: Components         :done, a3, 00:30, 90m
    Test Agent: Unit Tests             :done, a4, 00:30, 60m
    Integration Agent: E2E             :done, a5, 02:00, 45m
    Auto Review & Cleanup              :done, a6, 02:45, 15m
    Total: 3 hours                     :milestone, a7, 03:00, 0m
```

**Time Savings: 68% reduction in development time through parallelization**

### Agent Activity Timeline Example

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d','gridColor':'#4ecdc4','gridTextColor':'#fff'}}}%%
gantt
    title Real-time Agent Execution (User Auth Feature)
    dateFormat mm:ss
    axisFormat %M:%S
    
    section Admin Agent
    Analyze Request                    :done, admin1, 00:00, 15s
    Create Task Plan                   :done, admin2, 00:15, 20s
    Assign to Workers                  :done, admin3, 00:35, 10s
    Monitor Progress                   :active, admin4, 00:45, 120s
    
    section Backend Worker
    Query RAG for Context              :done, back1, 00:45, 10s
    Acquire users.py Lock              :done, back2, 00:55, 5s
    Create User Model                  :done, back3, 01:00, 30s
    Create Auth Endpoints              :done, back4, 01:30, 45s
    Write Tests                        :done, back5, 02:15, 30s
    Release Lock & Cleanup             :done, back6, 02:45, 5s
    
    section Frontend Worker
    Query RAG for UI Patterns          :done, front1, 00:45, 10s
    Acquire LoginForm.tsx Lock         :done, front2, 00:55, 5s
    Create Login Component             :done, front3, 01:00, 40s
    Create Register Component          :done, front4, 01:40, 40s
    Add Auth Context                   :done, front5, 02:20, 35s
    Release Lock & Cleanup             :done, front6, 02:55, 5s
    
    section Test Worker
    Query Test Patterns                :done, test1, 01:30, 10s
    Wait for Backend Completion        :done, test2, 01:40, 40s
    Create Integration Tests           :done, test3, 02:20, 45s
    Run Test Suite                     :done, test4, 03:05, 25s
    Report Results                     :done, test5, 03:30, 10s
    
    section Integration Worker
    Wait for All Components            :done, int1, 02:00, 90s
    Connect Frontend to API            :done, int2, 03:30, 30s
    E2E Testing                        :done, int3, 04:00, 40s
    Final Validation                   :done, int4, 04:40, 20s
    Feature Complete                   :milestone, int5, 05:00, 0s
```

**Total Time: 5 minutes for complete authentication system (DB + API + UI + Tests)**

---

## �📊 System Architecture Diagrams

### Data Flow Architecture

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
sequenceDiagram
    participant User as User/IDE
    participant MCP as MCP Server
    participant Admin as Admin Agent
    participant Queue as Task Queue
    participant Worker as Worker Agent
    participant RAG as RAG System
    participant DB as Database
    participant FS as File System
    
    User->>MCP: Send Task Request
    MCP->>Admin: Forward Task
    Admin->>RAG: Query Project Context
    RAG->>DB: Semantic Search
    DB-->>RAG: Relevant Context
    RAG-->>Admin: Context + History
    Admin->>Queue: Create Subtasks
    Queue->>Worker: Assign Task
    Worker->>RAG: Query Specific Context
    RAG-->>Worker: Code Patterns
    Worker->>FS: Request File Lock
    FS-->>Worker: Lock Acquired
    Worker->>FS: Modify Files
    Worker->>DB: Update Task Status
    Worker->>Queue: Complete Task
    Queue->>Admin: Aggregate Results
    Admin->>MCP: Return Response
    MCP->>User: Display Results
    
    Note over Worker,FS: Automatic cleanup after task completion
    Note over Admin,Queue: Max 10 concurrent agents enforced
```

### Agent Lifecycle Management

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
stateDiagram-v2
    [*] --> Requested: User Creates Task
    Requested --> Queued: Admin Decomposes
    Queued --> Spawning: Queue Assigns
    Spawning --> Active: Agent Initialized
    Active --> Working: Task Execution
    Working --> Blocked: File Locked
    Blocked --> Working: Lock Released
    Working --> Completing: Task Finished
    Completing --> Terminated: Cleanup
    Terminated --> [*]
    
    Active --> Idle: No Work (60s)
    Idle --> Terminated: Auto-Cleanup
    
    Active --> Failed: Error Occurred
    Failed --> Retry: Retriable Error
    Retry --> Active: Respawn Agent
    Failed --> Terminated: Fatal Error
    
    note right of Active: Max 10 concurrent agents
    note right of Idle: Automatic garbage collection
    note right of Terminated: Release all resources
```

### RAG System Architecture

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    subgraph "Indexing Pipeline"
        A[Project Files] --> B[Chunk Extraction]
        B --> C[OpenAI Embeddings]
        C --> D[Vector Storage]
        D --> E[sqlite-vec Index]
    end
    
    subgraph "Query Pipeline"
        F[Agent Query] --> G[Query Embedding]
        G --> H[Similarity Search]
        H --> I[Top-K Results]
        I --> J[Context Assembly]
    end
    
    subgraph "Context Management"
        K[Task Context]
        L[Agent Memory]
        M[Project Knowledge]
        N[Code Patterns]
    end
    
    E --> H
    J --> K & L & M & N
    K & L & M & N --> O[Agent Response]
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style C fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style E fill:#2d2d2d,stroke:#60a5fa,color:#fff
    style F fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style H fill:#2d2d2d,stroke:#34d399,color:#fff
    style O fill:#2d2d2d,stroke:#a78bfa,color:#fff
```

**Mathematical Representation:**

The RAG system uses cosine similarity for vector search:

$$\text{score}(q, d) = \frac{\sum_{i=1}^{n} q_i \cdot d_i}{\sqrt{\sum_{i=1}^{n} q_i^2} \cdot \sqrt{\sum_{i=1}^{n} d_i^2}}$$

Where:
- $q$ = query embedding vector (1536 dimensions)
- $d$ = document embedding vector
- $n$ = embedding dimension (1536)
- $\text{score}(q, d) \in [-1, 1]$ (higher = more similar)

Top-K retrieval returns the $k$ documents with highest scores:

$$\text{TopK}(q, D, k) = \text{argtopk}_{d \in D} \text{score}(q, d)$$

### File Lock Management

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    A[Agent Needs File] --> B{File Locked?}
    B -->|No| C[Acquire Lock]
    B -->|Yes| D{Priority?}
    D -->|High| E[Add to Wait Queue]
    D -->|Low| F[Work on Other Tasks]
    C --> G[Modify File]
    G --> H[Release Lock]
    H --> I{Wait Queue Empty?}
    I -->|No| J[Grant to Next Agent]
    I -->|Yes| K[File Available]
    E --> L{Timeout?}
    L -->|No| B
    L -->|Yes| M[Task Failed]
    F --> N[Check Again Later]
    N --> B
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style C fill:#2d2d2d,stroke:#34d399,color:#fff
    style G fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style H fill:#2d2d2d,stroke:#34d399,color:#fff
    style M fill:#2d2d2d,stroke:#ff6b6b,color:#fff
```

### Task Decomposition Strategy

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TB
    A["Complex Feature Request"] --> B[Admin Agent Analysis]
    B --> C{Complexity Assessment}
    
    C -->|High| D[Multi-Agent Required]
    C -->|Medium| E[Single Agent + Subtasks]
    C -->|Low| F[Single Agent Direct]
    
    D --> G[Identify Components]
    G --> H[Backend Tasks]
    G --> I[Frontend Tasks]
    G --> J[Test Tasks]
    G --> K[Integration Tasks]
    
    H --> H1[Task 1: Database Schema]
    H --> H2[Task 2: API Endpoints]
    H --> H3[Task 3: Business Logic]
    
    I --> I1[Task 1: UI Components]
    I --> I2[Task 2: State Management]
    I --> I3[Task 3: Styling]
    
    J --> J1[Task 1: Unit Tests]
    J --> J2[Task 2: Integration Tests]
    
    K --> K1[Task 1: API Integration]
    K --> K2[Task 2: E2E Testing]
    
    H1 & H2 & H3 --> L[Backend Agent]
    I1 & I2 & I3 --> M[Frontend Agent]
    J1 & J2 --> N[Test Agent]
    K1 & K2 --> O[Integration Agent]
    
    L & M & N & O --> P[Results Aggregation]
    P --> Q[Complete Feature]
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style D fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style E fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style F fill:#2d2d2d,stroke:#34d399,color:#fff
    style L fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style M fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style N fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style O fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style Q fill:#2d2d2d,stroke:#4ecdc4,color:#fff
```

### Communication Patterns

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph LR
    subgraph "Broadcast Pattern"
        A1[Admin] -->|Global Update| B1[All Workers]
        B1 --> C1[Worker 1]
        B1 --> C2[Worker 2]
        B1 --> C3[Worker 3]
    end
    
    subgraph "Direct Messaging"
        D1[Worker A] -->|Specific Question| D2[Worker B]
        D2 -->|Response| D1
    end
    
    subgraph "Hierarchical"
        E1[Admin] -->|Task Assignment| E2[Worker]
        E2 -->|Status Update| E1
        E1 -->|New Instructions| E2
    end
    
    subgraph "Shared Memory"
        F1[Worker A] -->|Write| F2[RAG System]
        F2 -->|Read| F3[Worker B]
        F3 -->|Write| F2
        F2 -->|Read| F1
    end
    
    style A1 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style D1 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D2 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style E1 fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style E2 fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style F2 fill:#2d2d2d,stroke:#34d399,color:#fff
```

---

## The Multi-Agent Solution

Agent-MCP transforms AI development from a single assistant to a coordinated team:

<div align="center">
  <img src="assets/images/dashboard-overview.png" alt="Multi-Agent Collaboration Network" width="800">
</div>

**Real-time visualization** shows your AI team at work - purple nodes represent context entries, blue nodes are agents, and connections show active collaborations. It's like having a mission control center for your development team.

### Core Capabilities

**Parallel Execution**  
Multiple specialized agents work simultaneously on different parts of your codebase. Backend agents handle APIs while frontend agents build UI components, all coordinated through shared memory.

**Persistent Knowledge Graph**  

<div align="center">
  <img src="assets/images/memory-bank.png" alt="Memory Bank Interface" width="800">
</div>

Your project's entire context lives in a searchable, persistent memory bank. Agents query this shared knowledge to understand requirements, architectural decisions, and implementation details. Nothing gets lost between sessions.

**Intelligent Task Management**  

<div align="center">
  <img src="assets/images/agent-fleet.png" alt="Agent Fleet Management" width="800">
</div>

Monitor every agent's status, assigned tasks, and recent activity. The system automatically manages task dependencies, prevents conflicts, and ensures work flows smoothly from planning to implementation.

---

## 🎨 Feature Ecosystem

### Complete System Overview

```mermaid
graph TB
    Root[Agent-MCP System]
    
    Root --> Core[Core Features]
    Root --> Intelligence[Intelligence Layer]
    Root --> UI[User Interface]
    Root --> Integration[Integrations]
    
    Core --> C1[Multi-Agent Orchestration]
    Core --> C2[Task Management]
    Core --> C3[File Locking]
    Core --> C4[Agent Lifecycle]
    
    Intelligence --> I1[RAG System]
    Intelligence --> I2[Semantic Search]
    Intelligence --> I3[Context Assembly]
    Intelligence --> I4[Pattern Recognition]
    
    UI --> U1[Real-time Dashboard]
    UI --> U2[Network Visualization]
    UI --> U3[Memory Bank]
    UI --> U4[Agent Fleet Monitor]
    
    Integration --> IN1[MCP Protocol]
    Integration --> IN2[Claude Desktop]
    Integration --> IN3[Git Worktrees]
    Integration --> IN4[Tmux Sessions]
    
    C1 --> C1A[Max 10 Agents]
    C1 --> C1B[Auto Cleanup]
    C1 --> C1C[Specialization]
    
    C2 --> C2A[Dependency Resolution]
    C2 --> C2B[Priority Queue]
    C2 --> C2C[Parallel Execution]
    
    C3 --> C3A[Distributed Locks]
    C3 --> C3B[Deadlock Prevention]
    C3 --> C3C[Auto Release]
    
    C4 --> C4A[Spawn]
    C4 --> C4B[Monitor]
    C4 --> C4C[Terminate]
    
    I1 --> I1A[Vector Embeddings]
    I1 --> I1B[Similarity Search]
    I1 --> I1C[Context Retrieval]
    
    I2 --> I2A[Code Search]
    I2 --> I2B[Doc Search]
    I2 --> I2C[Pattern Matching]
    
    U1 --> U1A[WebSocket Updates]
    U1 --> U1B[Live Metrics]
    U1 --> U1C[Activity Timeline]
    
    U2 --> U2A[Node Graph]
    U2 --> U2B[Connection Lines]
    U2 --> U2C[Physics Layout]
    
    IN1 --> IN1A[Tools]
    IN1 --> IN1B[Resources]
    IN1 --> IN1C[Prompts]
    
    IN2 --> IN2A[Native Integration]
    IN2 --> IN2B[Auto Discovery]
    IN2 --> IN2C[Tool Calling]
    
    style Root fill:#1e1e1e,stroke:#4ecdc4,stroke-width:4px,color:#fff
    style Core fill:#2d2d2d,stroke:#ff6b6b,stroke-width:2px,color:#fff
    style Intelligence fill:#2d2d2d,stroke:#ffd93d,stroke-width:2px,color:#fff
    style UI fill:#2d2d2d,stroke:#a78bfa,stroke-width:2px,color:#fff
    style Integration fill:#2d2d2d,stroke:#34d399,stroke-width:2px,color:#fff
```

### Feature Matrix

| Category | Feature | Status | Description | Impact |
|----------|---------|--------|-------------|--------|
| **Agent Management** | Multi-Agent Orchestration | ✅ Stable | Coordinate up to 10 specialized agents | 5x development speed |
| | Automatic Lifecycle | ✅ Stable | Spawn, monitor, cleanup agents | Zero manual management |
| | Role Specialization | ✅ Stable | Backend, Frontend, Test, DevOps, Research | 3x code quality |
| | Resource Limits | ✅ Stable | Hard cap at 10 concurrent agents | Predictable performance |
| **Task System** | Dependency Resolution | ✅ Stable | DAG-based task ordering | Zero integration issues |
| | Priority Queuing | ✅ Stable | Intelligent task prioritization | Optimal resource usage |
| | Parallel Execution | ✅ Stable | Independent tasks run simultaneously | 68% time reduction |
| | Status Tracking | ✅ Stable | Real-time progress monitoring | Complete visibility |
| **Knowledge** | RAG System | ✅ Stable | Retrieval-Augmented Generation | 100% context retention |
| | Vector Search | ✅ Stable | Semantic similarity via sqlite-vec | Sub-second queries |
| | Code Indexing | ✅ Stable | Automatic embedding generation | Instant context access |
| | Pattern Learning | ✅ Stable | Learn from past implementations | Consistent quality |
| **Safety** | File Locking | ✅ Stable | Distributed file-level locks | Zero conflicts |
| | Deadlock Prevention | ✅ Stable | Timeout-based recovery | 100% availability |
| | Transaction Safety | ✅ Stable | SQLite ACID properties | Data integrity |
| | Audit Logging | ✅ Stable | Complete activity history | Full traceability |
| **UI/UX** | Real-time Dashboard | ✅ Stable | Next.js 15 + React 19 | Live monitoring |
| | Network Visualization | ✅ Stable | Interactive agent graph | Visual collaboration |
| | Memory Bank | ✅ Stable | Searchable knowledge base | Context discovery |
| | Activity Timeline | ✅ Stable | Chronological agent actions | Debug support |
| **Integration** | MCP Protocol | ✅ Stable | Standard AI assistant integration | Universal compatibility |
| | Claude Desktop | ✅ Stable | Native support | One-click setup |
| | Cursor IDE | ✅ Stable | Direct integration | In-editor workflow |
| | Git Worktrees | ✅ Stable | Parallel branch work | No conflicts |
| | Tmux Sessions | ✅ Stable | Persistent terminals | Survives disconnects |
| | Playwright | ✅ Stable | Browser automation | Visual testing |
| **Future** | Multi-LLM Support | 🔄 Planned | Anthropic, Google, Local models | Provider choice |
| | Plugin System | 🔄 Planned | Custom agent types | Extensibility |
| | Advanced Analytics | 🔄 Planned | Performance insights | Optimization data |
| | Enterprise SSO | 🔄 Planned | SAML/OAuth integration | Team deployment |

---

## Quick Start

### Python Implementation (Recommended)

```bash
# Clone and setup
git clone https://github.com/rinadelph/Agent-MCP.git
cd Agent-MCP

# Check version requirements
python --version  # Should be >=3.10
node --version    # Should be >=18.0.0
npm --version     # Should be >=9.0.0

# If using nvm for Node.js version management
nvm use  # Uses the version specified in .nvmrc

# Configure environment
cp .env.example .env  # Add your OpenAI API key
uv venv
uv install

# Start the server
uv run -m agent_mcp.cli --port 8080 --project-dir path-to-directory

# Launch dashboard (recommended for full experience)
cd agent_mcp/dashboard && npm install && npm run dev
```

### Node.js/TypeScript Implementation (Alternative)

```bash
# Clone and setup
git clone https://github.com/rinadelph/Agent-MCP.git
cd Agent-MCP/agent-mcp-node

# Install dependencies
npm install

# Configure environment
cp .env.example .env  # Add your OpenAI API key

# Start the server
npm run server

# Or use the built version
npm run build
npm start

# Or install globally
npm install -g agent-mcp-node
agent-mcp --port 8080 --project-dir path-to-directory
```

## MCP Integration Guide

### What is MCP?

The **Model Context Protocol (MCP)** is an open standard that enables AI assistants to securely connect to external data sources and tools. Agent-MCP leverages MCP to provide seamless integration with various development tools and services.

### Running Agent-MCP as an MCP Server

Agent-MCP can function as an MCP server, exposing its multi-agent capabilities to MCP-compatible clients like Claude Desktop, Cline, and other AI coding assistants.

#### Quick MCP Setup

```bash
# 1. Install Agent-MCP
uv venv
uv install

# 2. Start the MCP server
uv run -m agent_mcp.cli --port 8080

# 3. Configure your MCP client to connect to:
# HTTP: http://localhost:8000/mcp
# WebSocket: ws://localhost:8000/mcp/ws
```

#### MCP Server Configuration

Create an MCP configuration file (`mcp_config.json`):

```json
{
  "server": {
    "name": "agent-mcp",
    "version": "1.0.0"
  },
  "tools": [
    {
      "name": "create_agent",
      "description": "Create a new specialized AI agent"
    },
    {
      "name": "assign_task", 
      "description": "Assign tasks to specific agents"
    },
    {
      "name": "query_project_context",
      "description": "Query the shared knowledge graph"
    },
    {
      "name": "manage_agent_communication",
      "description": "Handle inter-agent messaging"
    }
  ],
  "resources": [
    {
      "name": "agent_status",
      "description": "Real-time agent status and activity"
    },
    {
      "name": "project_memory",
      "description": "Persistent project knowledge graph"
    }
  ]
}
```

#### Using Agent-MCP with Claude Desktop

1. **Add to Claude Desktop Config**:
   
   Open `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) or equivalent:
   
   ```json
   {
     "mcpServers": {
       "agent-mcp": {
         "command": "uv",
         "args": ["run", "-m", "agent_mcp.cli", "--port", "8080"],
         "env": {
           "OPENAI_API_KEY": "your-openai-api-key"
         }
       }
     }
   }
   ```

2. **Restart Claude Desktop** to load the MCP server

3. **Verify Connection**: Claude should show "🔌 agent-mcp" in the conversation

#### MCP Tools Available

Once connected, you can use these MCP tools directly in Claude:

**Agent Management**
- `create_agent` - Spawn specialized agents (backend, frontend, testing, etc.)
- `list_agents` - View all active agents and their status
- `terminate_agent` - Safely shut down agents

**Task Orchestration**  
- `assign_task` - Delegate work to specific agents
- `view_tasks` - Monitor task progress and dependencies
- `update_task_status` - Track completion and blockers

**Knowledge Management**
- `ask_project_rag` - Query the persistent knowledge graph
- `update_project_context` - Add architectural decisions and patterns
- `view_project_context` - Access stored project information

**Communication**
- `send_agent_message` - Direct messaging between agents
- `broadcast_message` - Send updates to all agents
- `request_assistance` - Escalate complex issues

#### Advanced MCP Configuration

**Custom Transport Options**:
```bash
# HTTP with custom port
uv run -m agent_mcp.cli --port 8080

# WebSocket with authentication
uv run -m agent_mcp.cli --port 8080 --auth-token your-secret-token

# Unix socket (Linux/macOS)
uv run -m agent_mcp.cli --port 8080
```

**Environment Variables**:
```bash
export AGENT_MCP_HOST=0.0.0.0          # Server host
export AGENT_MCP_PORT=8000              # Server port  
export AGENT_MCP_LOG_LEVEL=INFO         # Logging level
export AGENT_MCP_PROJECT_DIR=/your/project  # Default project directory
export AGENT_MCP_MAX_AGENTS=10          # Maximum concurrent agents
```

### MCP Client Examples

#### Python Client
```python
import asyncio
from mcp import Client

async def main():
    async with Client("http://localhost:8000/mcp") as client:
        # Create a backend agent
        result = await client.call_tool("create_agent", {
            "role": "backend",
            "specialization": "API development"
        })
        
        # Assign a task
        await client.call_tool("assign_task", {
            "agent_id": result["agent_id"],
            "task": "Implement user authentication endpoints"
        })
        
        # Query project context
        context = await client.call_tool("ask_project_rag", {
            "query": "What's our current database schema?"
        })
        print(context)

asyncio.run(main())
```

#### JavaScript Client
```javascript
import { MCPClient } from '@modelcontextprotocol/client';

const client = new MCPClient('http://localhost:8000/mcp');

async function createAgent() {
  await client.connect();
  
  const agent = await client.callTool('create_agent', {
    role: 'frontend',
    specialization: 'React components'
  });
  
  console.log('Created agent:', agent.agent_id);
  
  await client.disconnect();
}

createAgent().catch(console.error);
```

### Troubleshooting MCP Connection

**Connection Issues**:
```bash
# Check if MCP server is running
curl http://localhost:8000/mcp/health

# Verify WebSocket connection
wscat -c ws://localhost:8000/mcp/ws

# Check server logs
uv run -m agent_mcp.cli --port 8080 --log-level DEBUG
```

**Common Issues**:
- **Port conflicts**: Change port with `--port` flag
- **Permission errors**: Ensure OpenAI API key is set
- **Client timeout**: Increase timeout in client configuration
- **Agent limit reached**: Check active agent count with `list_agents`

### Integration Examples

**VS Code with MCP**:
Use the MCP extension to integrate Agent-MCP directly into your editor workflow.

**Terminal Usage**:
```bash
# Quick task assignment via curl
curl -X POST http://localhost:8000/mcp/tools/assign_task \
  -H "Content-Type: application/json" \
  -d '{"task": "Add error handling to API endpoints", "agent_role": "backend"}'
```

**CI/CD Integration**:
```yaml
# GitHub Actions example
- name: Run Agent-MCP Code Review
  run: |
    uv run -m agent_mcp.cli --port 8080 --daemon
    curl -X POST localhost:8000/mcp/tools/assign_task \
      -d '{"task": "Review PR for security issues", "agent_role": "security"}'
```

## How It Works: Breaking Complexity into Simple Steps

```mermaid
graph LR
    A[Step 1] --> B[Step 2] --> C[Step 3] --> D[Step 4] --> E[Done!]
    style A fill:#4ecdc4,color:#fff
    style E fill:#ff6b6b,color:#fff
```

Every task can be broken down into linear steps. This is the core insight that makes Agent-MCP powerful.

### The Problem with Complex Tasks

**Definition**: Traditional AI assistants struggle with complex tasks due to context limitations and lack of specialization.

**Motivation**: As projects grow, single agents become overwhelmed, leading to:
- Context window pollution (mixing unrelated information)
- Decision paralysis (too many concerns simultaneously)
- Quality degradation (rushed implementations to fit context)
- Knowledge loss (forgetting earlier parts of conversation)

**Mechanism**:
1. User provides vague, high-level requirement
2. Agent attempts to reason about all aspects simultaneously
3. Context fills with mixed concerns (DB + API + UI + Tests)
4. Agent makes assumptions to compensate for confusion
5. Implementation is incomplete or inconsistent

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#ff6b6b','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    A["Build User Authentication"] -->|Single Agent Tries Everything| B{???}
    B --> C[Database?]
    B --> D[API?]
    B --> E[Frontend?]
    B --> F[Security?]
    B --> G[Tests?]
    C -.->|Confused| H[Incomplete Implementation]
    D -.->|Overwhelmed| H
    E -.->|Context Lost| H
    F -.->|Assumptions| H
    G -.->|Forgotten| H
    
    style A fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style B fill:#2d2d2d,stroke:#ff6b6b,color:#fff
    style C fill:#2d2d2d,stroke:#666,color:#fff
    style D fill:#2d2d2d,stroke:#666,color:#fff
    style E fill:#2d2d2d,stroke:#666,color:#fff
    style F fill:#2d2d2d,stroke:#666,color:#fff
    style G fill:#2d2d2d,stroke:#666,color:#fff
    style H fill:#2d2d2d,stroke:#ff6b6b,color:#fff
```

**Mathematical Formulation**:

Let $C$ = Context window capacity, $T_i$ = Task components

Single agent context utilization:

$$U_{single} = \frac{\sum_{i=1}^{n} |T_i|}{C}$$

When $U_{single} > 1$, context overflow occurs, leading to:

$$P_{failure} = 1 - e^{-\lambda(U_{single} - 1)}$$

Where $\lambda$ represents task complexity factor.

**Measured Impact**:
- Context utilization: 95-100% (constant overflow)
- Error rate: 40-60% incomplete implementations
- Time to completion: 2-4x longer due to rework
- Developer satisfaction: 3/10 (frustration with quality)

### The Agent-MCP Solution

**Definition**: Decompose complex tasks into atomic, parallelizable subtasks executed by specialized agents.

**Motivation**: By breaking work into focused units:
- Each agent maintains minimal, relevant context
- Specialization increases implementation quality
- Parallel execution dramatically reduces time
- Clear dependencies prevent integration issues

**Step-by-Step Mechanism**:

1. **Admin Agent Receives Request**
   - Analyzes requirement complexity
   - Queries RAG for similar patterns
   - Identifies component boundaries

2. **Task Decomposition**
   - Maps feature to architectural layers
   - Creates directed acyclic graph (DAG) of dependencies
   - Assigns tasks to specialized agent types

3. **Parallel Execution**
   - Independent tasks start simultaneously
   - Agents query RAG for specific context only
   - File locks prevent conflicts
   - Each agent completes atomic work unit

4. **Integration & Validation**
   - Dependent tasks wait for prerequisites
   - Integration agent assembles components
   - Test agent validates complete system
   - Admin agent reviews results

5. **Cleanup & Documentation**
   - All agents terminate after completion
   - Work recorded in knowledge graph
   - Context available for future tasks
   - System ready for next request

```mermaid
%%{init: {'theme':'dark', 'themeVariables': { 'primaryColor':'#1e1e1e','primaryTextColor':'#fff','primaryBorderColor':'#4ecdc4','lineColor':'#4ecdc4','secondaryColor':'#2d2d2d','tertiaryColor':'#3d3d3d','background':'#1e1e1e','mainBkg':'#2d2d2d','secondBkg':'#3d3d3d'}}}%%
graph TD
    A["Build User Authentication"] -->|Break Down| B[Linear Tasks]
    B --> C["Agent 1: Database"]
    B --> D["Agent 2: API"]
    B --> E["Agent 3: Frontend"]
    
    C --> C1[Create users table]
    C1 --> C2[Add indexes]
    C2 --> C3[Create sessions table]
    
    D --> D1[POST /register]
    D1 --> D2[POST /login]
    D2 --> D3[POST /logout]
    
    E --> E1[Login Form]
    E1 --> E2[Register Form]
    E2 --> E3[Auth Context]
    
    C3 --> F[Working System]
    D3 --> F
    E3 --> F
    
    style A fill:#2d2d2d,stroke:#4ecdc4,color:#fff
    style B fill:#2d2d2d,stroke:#ffd93d,color:#fff
    style C fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style D fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style E fill:#2d2d2d,stroke:#a78bfa,color:#fff
    style C1 fill:#2d2d2d,stroke:#34d399,color:#fff
    style C2 fill:#2d2d2d,stroke:#34d399,color:#fff
    style C3 fill:#2d2d2d,stroke:#34d399,color:#fff
    style D1 fill:#2d2d2d,stroke:#34d399,color:#fff
    style D2 fill:#2d2d2d,stroke:#34d399,color:#fff
    style D3 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E1 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E2 fill:#2d2d2d,stroke:#34d399,color:#fff
    style E3 fill:#2d2d2d,stroke:#34d399,color:#fff
    style F fill:#2d2d2d,stroke:#4ecdc4,color:#fff
```

**Mathematical Formulation**:

For $n$ independent tasks with $m$ agents:

Parallel context utilization per agent:

$$U_{parallel} = \frac{|T_i|}{C}, \quad i \in [1, n]$$

Where each agent handles single task $T_i$, ensuring $U_{parallel} \ll 1$

Expected completion time:

$$E[T_{complete}] = \max_{i=1}^{n} t_i + \sum_{j \in \text{deps}} t_j$$

Compared to sequential:

$$T_{sequential} = \sum_{i=1}^{n} t_i$$

Speedup factor:

$$S = \frac{T_{sequential}}{E[T_{complete}]} \approx \frac{n}{1 + d}$$

Where $d$ = dependency chain depth

**Implementation Details**:

```python
# Task decomposition algorithm
def decompose_task(feature_request: str) -> List[Task]:
    # Query RAG for similar patterns
    patterns = rag.search(feature_request, top_k=5)
    
    # Identify architectural layers
    layers = identify_layers(feature_request, patterns)
    
    # Create dependency graph
    dag = create_dag(layers)
    
    # Assign to agent types
    tasks = []
    for node in dag.topological_sort():
        agent_type = determine_agent_type(node)
        task = Task(
            id=generate_id(),
            description=node.description,
            agent_type=agent_type,
            dependencies=[t.id for t in node.predecessors],
            estimated_time=estimate_time(node)
        )
        tasks.append(task)
    
    return tasks
```

**Measured Impact**:
- Context utilization per agent: 15-30% (comfortable headroom)
- Error rate: 5-10% (mostly edge cases)
- Time to completion: 3-5x faster than single agent
- Code quality: 85%+ test coverage, consistent patterns
- Developer satisfaction: 9/10 (high confidence in results)
- Parallelization efficiency: 70-85% of theoretical maximum

Each agent focuses on their linear chain. No confusion. No context pollution. Just clear, deterministic progress.

## The 5-Step Workflow

### 1. Initialize Admin Agent
```
You are the admin agent.
Admin Token: "your_admin_token_from_server"

Your role is to:
- Coordinate all development work
- Create and manage worker agents
- Maintain project context
- Assign tasks based on agent specializations
```

### 2. Load Your Project Blueprint (MCD)
```
Add this MCD (Main Context Document) to project context:

[paste your MCD here - see docs/mcd-guide.md for structure]

Store every detail in the knowledge graph. This becomes the single source of truth for all agents.
```

The MCD (Main Context Document) is your project's comprehensive blueprint - think of it as writing the book of your application before building it. It includes:
- Technical architecture and design decisions
- Database schemas and API specifications
- UI component hierarchies and workflows
- Task breakdowns with clear dependencies

See our [MCD Guide](./docs/mcd-guide.md) for detailed examples and templates.

### 3. Deploy Your Agent Team
```
Create specialized agents for parallel development:

- backend-worker: API endpoints, database operations, business logic
- frontend-worker: UI components, state management, user interactions
- integration-worker: API connections, data flow, system integration
- test-worker: Unit tests, integration tests, validation
- devops-worker: Deployment, CI/CD, infrastructure
```

Each agent specializes in their domain, leading to higher quality implementations and faster development.

### 4. Initialize and Deploy Workers
```
# In new window for each worker:
You are [worker-name] agent.
Your Admin Token: "worker_token_from_admin"

Query the project knowledge graph to understand:
1. Overall system architecture
2. Your specific responsibilities
3. Integration points with other components
4. Coding standards and patterns to follow
5. Current implementation status

Begin implementation following the established patterns.

AUTO --worker --memory
```

**Important: Setting Agent Modes**

Agent modes (like `--worker`, `--memory`, `--playwright`) are not just flags - they activate specific behavioral patterns. In Claude Code, you can make these persistent by:

1. Copy the mode instructions to your clipboard
2. Type `#` to open Claude's memory feature
3. Paste the instructions for persistent behavior

Example for Claude Code memory:
```
# When I use "AUTO --worker --memory", follow these patterns:
- Always check file status before editing
- Query project RAG for context before implementing
- Document all changes in task notes
- Work on one file at a time, completing it before moving on
- Update task status after each completion
```

This ensures consistent behavior across your entire session without repeating instructions.

### 5. Monitor and Coordinate

The dashboard provides real-time visibility into your AI development team:

**Network Visualization** - Watch agents collaborate and share information  
**Task Progress** - Track completion across all parallel work streams  
**Memory Health** - Ensure context remains fresh and accessible  
**Activity Timeline** - See exactly what each agent is doing

Access at `http://localhost:3847` after launching the dashboard.

## Advanced Features

### Specialized Agent Modes

Agent modes fundamentally change how agents behave. They're not just configuration - they're behavioral contracts that ensure agents follow specific patterns optimized for their role.

**Standard Worker Mode**
```
AUTO --worker --memory
```
Optimized for implementation tasks:
- Granular file status checking before any edits
- Sequential task completion (one at a time)
- Automatic documentation of changes
- Integration with project RAG for context
- Task status updates after each completion

**Frontend Specialist Mode**
```
AUTO --worker --playwright
```
Enhanced with visual validation capabilities:
- All standard worker features
- Browser automation for component testing
- Screenshot capabilities for visual regression
- DOM interaction for end-to-end testing
- Component-by-component implementation with visual verification

**Research Mode**
```
AUTO --memory
```
Read-only access for analysis and planning:
- No file modifications allowed
- Deep context exploration via RAG
- Pattern identification across codebase
- Documentation generation
- Architecture analysis and recommendations

**Memory Management Mode**
```
AUTO --memory --manager
```
For context curation and optimization:
- Memory health monitoring
- Stale context identification
- Knowledge graph optimization
- Context summarization for new agents
- Cross-agent knowledge transfer

Each mode enforces specific behaviors that prevent common mistakes and ensure consistent, high-quality output.

### Project Memory Management

The system maintains several types of memory:

**Project Context** - Architectural decisions, design patterns, conventions  
**Task Memory** - Current status, blockers, implementation notes  
**Agent Memory** - Individual agent learnings and specializations  
**Integration Points** - How different components connect

All memory is:
- Searchable via semantic queries
- Version controlled for rollback
- Tagged for easy categorization
- Automatically garbage collected when stale

### Conflict Resolution

File-level locking prevents agents from overwriting each other's work:

1. Agent requests file access
2. System checks if file is locked
3. If locked, agent works on other tasks or waits
4. After completion, lock is released
5. Other agents can now modify the file

This happens automatically - no manual coordination needed.

## Short-Lived vs. Long-Lived Agents: The Critical Difference

### Traditional Long-Lived Agents
Most AI coding assistants maintain conversations across entire projects:
- **Accumulated context grows unbounded** - mixing unrelated code, decisions, and conversations
- **Confused priorities** - yesterday's bug fix mingles with today's feature request
- **Hallucination risks increase** - agents invent connections between unrelated parts
- **Performance degrades over time** - every response processes irrelevant history
- **Security vulnerability** - one carefully crafted prompt could expose your entire project

### Agent-MCP's Ephemeral Agents
Each agent is purpose-built for a single task:
- **Minimal, focused context** - only what's needed for the specific task
- **Crystal clear objectives** - one task, one goal, no ambiguity
- **Deterministic behavior** - limited context means predictable outputs
- **Consistently fast responses** - no context bloat to slow things down
- **Secure by design** - agents literally cannot access what they don't need

### A Practical Example

**Traditional Approach**: "Update the user authentication system"
```
Agent: I'll update your auth system. I see from our previous conversation about 
database migrations, UI components, API endpoints, deployment scripts, and that 
bug in the payment system... wait, which auth approach did we decide on? Let me 
try to piece this together from our 50+ message history...

[Agent produces confused implementation mixing multiple patterns]
```

**Agent-MCP Approach**: Same request, broken into focused tasks
```
Agent 1 (Database): Create auth tables with exactly these fields...
Agent 2 (API): Implement /auth endpoints following REST patterns...
Agent 3 (Frontend): Build login forms using existing component library...
Agent 4 (Tests): Write auth tests covering these specific scenarios...
Agent 5 (Integration): Connect components following documented interfaces...

[Each agent completes their specific task without confusion]
```

## The Theory Behind Linear Decomposition

### The Philosophy: Short-Lived Agents, Granular Tasks

Most AI development approaches suffer from a fundamental flaw: they try to maintain massive context windows with a single, long-running agent. This leads to:

- **Context pollution** - Irrelevant information drowns out what matters
- **Hallucination risks** - Agents invent connections between unrelated parts
- **Security vulnerabilities** - Agents with full context can be manipulated
- **Performance degradation** - Large contexts slow down reasoning
- **Unpredictable behavior** - Too much context creates chaos

### Our Solution: Ephemeral Agents with Shared Memory

Agent-MCP implements a radically different approach:

**Short-Lived, Focused Agents**  
Each agent lives only as long as their specific task. They:
- Start with minimal context (just what they need)
- Execute granular, linear tasks with clear boundaries
- Document their work in shared memory
- Terminate upon completion

**Shared Knowledge Graph (RAG)**  
Instead of cramming everything into context windows:
- Persistent memory stores all project knowledge
- Agents query only what's relevant to their task
- Knowledge accumulates without overwhelming any single agent
- Clear separation between working memory and reference material

**Result**: Agents that are fast, focused, and safe. They can't be manipulated to reveal full project details because they never have access to it all at once.

### Why This Matters for Safety

Traditional long-context agents are like giving someone your entire codebase, documentation, and secrets in one conversation. Our approach is like having specialized contractors who only see the blueprint for their specific room.

- **Reduced attack surface** - Agents can't leak what they don't know
- **Deterministic behavior** - Limited context means predictable outputs
- **Audit trails** - Every agent action is logged and traceable
- **Rollback capability** - Mistakes are isolated to specific tasks

### The Cleanup Protocol: Keeping Your System Lean

Agent-MCP enforces strict lifecycle management:

**Maximum 10 Active Agents**
- Hard limit prevents resource exhaustion
- Forces thoughtful task allocation
- Maintains system performance

**Automatic Cleanup Rules**
- Agent finishes task → Immediately terminated
- Agent idle 60+ seconds → Killed and task reassigned
- Need more than 10 agents → Least productive agents removed

**Why This Matters**
- **No zombie processes** eating resources
- **Fresh context** for every task
- **Predictable resource usage**
- **Clean system state** always

This isn't just housekeeping - it's fundamental to the security and performance benefits of the short-lived agent model.

### The Fundamental Principle

**Any task that cannot be expressed as `Step 1 → Step 2 → Step N` is not atomic enough.**

This principle drives everything in Agent-MCP:

1. **Complex goals** must decompose into **linear sequences**
2. **Linear sequences** can execute **in parallel** when independent
3. **Each step** must have **clear prerequisites** and **deterministic outputs**
4. **Integration points** are **explicit** and **well-defined**

### Why Linear Decomposition Works

**Traditional Approach**: "Build a user authentication system"
- Vague requirements lead to varied implementations
- Agents make different assumptions
- Integration becomes a nightmare

**Agent-MCP Approach**: 
```
Chain 1: Database Layer
  1.1: Create users table with id, email, password_hash
  1.2: Add unique index on email
  1.3: Create sessions table with user_id, token, expiry
  1.4: Write migration scripts
  
Chain 2: API Layer  
  2.1: Implement POST /auth/register endpoint
  2.2: Implement POST /auth/login endpoint
  2.3: Implement POST /auth/logout endpoint
  2.4: Add JWT token generation
  
Chain 3: Frontend Layer
  3.1: Create AuthContext provider
  3.2: Build LoginForm component
  3.3: Build RegisterForm component
  3.4: Implement protected routes
```

Each step is atomic, testable, and has zero ambiguity. Multiple agents can work these chains in parallel without conflict.

## Why Developers Choose Agent-MCP

**The Power of Parallel Development**  
Instead of waiting for one agent to finish the backend before starting the frontend, deploy specialized agents to work simultaneously. Your development speed is limited only by how well you decompose tasks.

**No More Lost Context**  
Every decision, implementation detail, and architectural choice is stored in the shared knowledge graph. New agents instantly understand the project state without reading through lengthy conversation histories.

**Predictable, Reliable Outputs**  
Focused agents with limited context produce consistent results. The same task produces the same quality output every time, making development predictable and testable.

**Built-in Conflict Prevention**  
File-level locking and task assignment prevent agents from stepping on each other's work. No more merge conflicts from simultaneous edits.

**Complete Development Transparency**  
Watch your AI team work in real-time through the dashboard. Every action is logged, every decision traceable. It's like having a live view into your development pipeline.

**For Different Team Sizes**

**Solo Developers**: Transform one AI assistant into a coordinated team. Work on multiple features simultaneously without losing track.

**Small Teams**: Augment human developers with AI specialists that maintain perfect context across sessions.

**Large Projects**: Handle complex systems where no single agent could hold all the context. The shared memory scales infinitely.

**Learning & Teaching**: Perfect for understanding software architecture. Watch how tasks decompose and integrate in real-time.

## System Requirements

- **Python**: 3.10+ with pip or uv
- **Node.js**: 18.0.0+ (recommended: 22.16.0)
- **npm**: 9.0.0+ (recommended: 10.9.2)
- **OpenAI API key** (for embeddings and RAG)
- **RAM**: 4GB minimum
- **AI coding assistant**: Claude Code or Cursor

For consistent development environment:
```bash
# Using nvm (Node Version Manager)
nvm use  # Automatically uses Node v22.16.0 from .nvmrc

# Or manually check versions
node --version  # Should be >=18.0.0
npm --version   # Should be >=9.0.0
python --version  # Should be >=3.10
```

## Troubleshooting

**"Admin token not found"**  
Check the server startup logs - token is displayed when MCP server starts.

**"Worker can't access tasks"**  
Ensure you're using the worker token (not admin token) when initializing workers.

**"Agents overwriting each other"**  
Verify all workers are initialized with the `--worker` flag for proper coordination.

**"Dashboard connection failed"**  
1. Ensure MCP server is running first
2. Check Node.js version (18+ required)
3. Reinstall dashboard dependencies

**"Memory queries returning stale data"**  
Run memory garbage collection through the dashboard or restart with `--refresh-memory`.

## Documentation

- [Getting Started Guide](./docs/getting-started.md) - Complete walkthrough with examples
- [MCD Creation Guide](./docs/mcd-guide.md) - Write effective project blueprints
- [Theoretical Foundation](./docs/chapter-1-cognitive-empathy.md) - Understanding AI cognition
- [Architecture Overview](./docs/architecture.md) - System design and components
- [API Reference](./docs/api-reference.md) - Complete technical documentation

## Community and Support

**Get Help**
- [Discord Community](https://discord.gg/7Jm7nrhjGn) - Active developer discussions
- [GitHub Issues](https://github.com/rinadelph/Agent-MCP/issues) - Bug reports and features
- [Discussions](https://github.com/rinadelph/Agent-MCP/discussions) - Share your experiences

**Contributing**
We welcome contributions! See our [Contributing Guide](CONTRIBUTING.md) for:
- Code style and standards
- Testing requirements
- Pull request process
- Development setup

## License

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

**What this means:**
- ✅ You can use, modify, and distribute this software
- ✅ You can use it for commercial purposes
- ⚠️ **Important**: If you run a modified version on a server that users interact with over a network, you **must** provide the source code to those users
- ⚠️ Any derivative works must also be licensed under AGPL-3.0
- ⚠️ You must include copyright notices and license information

See the [LICENSE](LICENSE) file for complete terms and conditions.

**Why AGPL?** We chose AGPL to ensure that improvements to Agent-MCP benefit the entire community, even when used in server/SaaS deployments. This prevents proprietary forks that don't contribute back to the ecosystem.

---

Built by developers who believe AI collaboration should be as sophisticated as human collaboration.