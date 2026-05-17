# ADK Samples

A collection of sample agents and applications built with [Google Agent Development Kit (ADK)](https://google.github.io/adk-docs/).

> **Note:** This is a fork of [google/adk-samples](https://github.com/google/adk-samples).

## Overview

This repository contains ready-to-use sample agents demonstrating various capabilities of the Agent Development Kit (ADK). Each sample is self-contained and includes setup instructions, configuration, and source code.

## Prerequisites

- Python 3.11+
- [Google ADK](https://pypi.org/project/google-adk/) (`pip install google-adk`)
- A Google Cloud project with the required APIs enabled
- Appropriate credentials configured (see [Authentication](#authentication))

## Repository Structure

```
adk-samples/
├── agents/                  # Individual agent samples
│   ├── hello-world/         # Minimal starter agent
│   ├── customer-service/    # Customer service agent example
│   └── data-analysis/       # Data analysis agent example
├── .github/                 # GitHub Actions workflows and templates
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/adk-samples.git
cd adk-samples
```

### 2. Set Up a Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Dependencies

Each agent sample has its own `requirements.txt`. Navigate to the desired agent directory and install:

```bash
cd agents/hello-world
pip install -r requirements.txt
```

### 4. Authentication

Configure Google Cloud credentials:

```bash
gcloud auth application-default login
```

Or set the `GOOGLE_APPLICATION_CREDENTIALS` environment variable to point to a service account key file.

### 5. Run a Sample Agent

```bash
adk run agents/hello-world
```

To launch the ADK web UI for interactive testing:

```bash
adk web
```

## Available Samples

| Sample | Description | Complexity |
|--------|-------------|------------|
| `hello-world` | Minimal agent demonstrating basic ADK setup | Beginner |
| `customer-service` | Multi-turn customer service agent with tool use | Intermediate |
| `data-analysis` | Agent that queries and analyzes structured data | Intermediate |

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/my-new-sample`)
3. Commit your changes following [Conventional Commits](https://www.conventionalcommits.org/)
4. Open a pull request

## Reporting Issues

Please use the [GitHub Issues](../../issues) page and select the appropriate template:
- **Bug Report** — for bugs in existing samples
- **Sample Request** — to request a new sample agent

## License

This project is licensed under the Apache 2.0 License. See [LICENSE](LICENSE) for details.
