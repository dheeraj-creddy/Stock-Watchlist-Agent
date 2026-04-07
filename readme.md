stock-watchlist-agent/
│
├── .env                          # API keys (never commit this)
├── config.py                     # Central configuration
├── requirements.txt              # All dependencies
├── app.py                        # Gradio web interface
│
├── agent/                        # The PAHF agent brain
│   ├── __init__.py
│   ├── state.py                  # Agent state definition
│   ├── prompts.py                # All prompt templates
│   ├── nodes.py                  # Each step the agent can take
│   └── graph.py                  # Wires nodes into a LangGraph
│
├── memory/                       # Persistent per-user memory
│   ├── __init__.py
│   └── manager.py                # Mem0 wrapper with 3 scopes
│
├── tools/                        # External capabilities
│   ├── __init__.py
│   ├── market_data.py            # Stock prices via yfinance
│   └── news.py                   # Financial news via RSS
│
├── personas/                     # Simulated users for testing
│   ├── __init__.py
│   ├── profiles.py               # User persona definitions
│   └── simulator.py              # LLM-simulated human
│
├── evaluation/                   # PAHF 4-phase testing
│   ├── __init__.py
│   ├── scenarios.py              # Test queries
│   ├── metrics.py                # SR, FF, ACPE calculations
│   └── run_eval.py               # Full evaluation runner
│
└── notebooks/                    # Jupyter notebooks for development
    └── 01_quickstart.ipynb       # Start here