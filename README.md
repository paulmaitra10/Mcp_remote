# ExpenseTracker Remote MCP Server

A **Remote MCP (Model Context Protocol) Expense Tracking Server** built with **FastMCP**, enabling AI agents and automation systems to manage, query, and analyze financial expenses through standardized MCP tools.

This project exposes expense management as **MCP tools + resources**, making it directly usable by AI agents, Claude Desktop, automation pipelines, and intelligent workflows.

---

## 🚀 Project Overview

**ExpenseTracker Remote MCP** is a server-side AI-integrated expense management system that allows:

* AI agents to add expenses
* Query expenses by date range
* Generate summaries and analytics
* Access structured financial data
* Provide category metadata as MCP resources

It is designed as a **remote MCP server**, meaning it can be accessed over HTTP and integrated into:

* AI agent frameworks
* Claude Desktop MCP
* Automation workflows
* Intelligent personal finance systems

---

## 🧠 Architecture

```
AI Agent / Claude Desktop / Automation
            │
            │ MCP Protocol (HTTP)
            ▼
    FastMCP Remote Server
            │
            │ Async DB Access (aiosqlite)
            ▼
        SQLite Database
```

---

## ✨ Features

### 🔹 MCP Tools

* `add_expense()` → Add new expense records
* `list_expenses()` → Query expenses by date range
* `summarize()` → Generate category-wise financial summaries

### 🔹 MCP Resources

* `expense:///categories` → Dynamic category resource provider

### 🔹 System Capabilities

* Async database operations
* WAL-mode SQLite
* Temporary-directory safe storage
* Remote HTTP transport
* AI-native interface
* Agent-compatible design

---

## 🛠 Tech Stack

* **Python 3.10+**
* **FastMCP** (MCP Server Framework)
* **MCP Protocol**
* **SQLite**
* **aiosqlite** (Async DB access)
* **uv** (Runtime & environment)
* **HTTP Transport**

---

## 📦 Installation

```bash
# Clone repository
git clone <your-repo-url>
cd expensetracker-remote_mcp

# Create virtual env
python -m venv test-mcp
source test-mcp/bin/activate  # Linux/Mac
test-mcp\Scripts\activate     # Windows

# Install dependencies
pip install fastmcp aiosqlite
```

---

## ▶️ Run Server

### Local Run

```bash
python main.py
```

### FastMCP CLI

```bash
fastmcp run main.py
```

Server starts at:

```
http://0.0.0.0:8000
```

---

## 🔌 MCP Integration

### Example MCP Tool Calls

#### Add Expense

```json
{
  "tool": "add_expense",
  "args": {
    "date": "2026-02-09",
    "amount": 250,
    "category": "Food & Dining",
    "subcategory": "Lunch",
    "note": "Office lunch"
  }
}
```

#### List Expenses

```json
{
  "tool": "list_expenses",
  "args": {
    "start_date": "2026-02-01",
    "end_date": "2026-02-09"
  }
}
```

#### Summarize Expenses

```json
{
  "tool": "summarize",
  "args": {
    "start_date": "2026-02-01",
    "end_date": "2026-02-09"
  }
}
```

---

## 📚 MCP Resource

### Categories Resource

```
GET expense:///categories
```

Provides structured JSON categories for agents and UIs.

---

## 🎯 Use Cases

* AI-powered personal finance assistants
* Autonomous budgeting agents
* Expense analytics bots
* Claude Desktop finance integration
* Agent-based accounting systems
* Automated expense classification
* Intelligent financial dashboards

---

## 🧩 Resume-Grade Project Description

**ExpenseTracker Remote MCP Server** is an AI-integrated financial automation system built using FastMCP and MCP Protocol, enabling AI agents to manage and analyze financial data through standardized MCP tools and resources. The system exposes expense management as remote services, supports asynchronous database operations, and is designed for agent-based automation, intelligent workflows, and AI-native financial systems.

---

## 🧠 Skills Demonstrated

* AI Agent Architecture
* MCP Protocol Implementation
* Remote AI Services
* Async Python Programming
* Database Engineering
* API Design
* System Architecture
* Automation Systems
* AI Tooling Infrastructure

---

## 📈 Project Impact

* Converts traditional CRUD apps into **AI-native services**
* Demonstrates **agent-oriented system design**
* Shows real-world **MCP protocol usage**
* Bridges **AI agents and real databases**
* Builds foundation for autonomous finance systems

---

## 🔮 Future Roadmap

* Authentication & user isolation
* Multi-user support
* AI-based auto-categorization
* Budget prediction models
* Expense anomaly detection
* Dashboard integration
* Vector search for notes
* Natural language queries
* Multi-agent coordination

---

## 📜 License

MIT License

---

## 👤 Author

**Paulastha Maitra**
AI/ML | Agent AI | MCP Systems | Intelligent Automation

---

## ⭐ Why This Project Matters

This is not a normal expense tracker.

It is an **AI-native financial infrastructure system** that demonstrates how MCP can be used to expose real-world systems to AI agents — enabling the future of autonomous digital systems, agent-based workflows, and AI-first software architecture.
