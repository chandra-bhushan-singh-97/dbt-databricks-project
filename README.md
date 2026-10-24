# dbt Databricks Project

A hands-on data engineering project demonstrating how to build, test, and manage data transformations using **dbt Core and Databricks SQL**.

## 📌 Project Overview

This project demonstrates a dbt workflow for transforming raw data into analytics-ready datasets using a layered data architecture. It includes SQL models, reusable Jinja macros, data quality tests, seeds, snapshots, and separate development and production environments.

## 🛠️ Tech Stack

- **dbt Core** – Data transformation and project orchestration
- **Databricks SQL** – Data warehouse and query execution
- **SQL** – Data transformation logic
- **Jinja** – Dynamic SQL generation and reusable macros
- **Git & GitHub** – Version control
- **Python** – Development environment and supporting tools

## 🏗️ Project Structure

```text
dbt/
├── chandu_dbt/
│   ├── analyses/
│   ├── macros/
│   ├── models/
│   │   ├── bronze/
│   │   ├── silver/
│   │   └── gold/
│   ├── seeds/
│   ├── snapshots/
│   ├── tests/
│   ├── dbt_project.yml
│   └── packages.yml
├── .gitignore
└── README.md
```

*Note: The structure above is illustrative. Adjust it to match the actual folders in your repository.*

## ✨ Key Features

- **Layered data modeling:** Organizes transformations into Bronze, Silver, and Gold layers.
- **Reusable macros:** Uses Jinja macros to reduce repetitive SQL code.
- **Data quality testing:** Implements dbt tests to validate data quality and consistency.
- **Snapshots:** Tracks changes in records over time using dbt snapshots.
- **Seeds:** Loads reference data from CSV files.
- **Environment management:** Configures separate development and production targets.
- **Version control:** Tracks project changes using Git and GitHub.

## ⚙️ Prerequisites

- Python installed
- dbt Core installed with the Databricks adapter
- Access to a Databricks workspace and SQL warehouse
- Git installed
- A configured dbt profile

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/chandra-bhushan-singh-97/dbt-databricks-project.git
cd dbt-databricks-project/chandu_dbt
```

### 2. Install dependencies

Activate your Python virtual environment, then install the project's dependencies. If the project uses `requirements.txt`, run:

```bash
pip install -r requirements.txt
```

If dependencies are managed another way, follow the project's existing setup.

### 3. Configure your Databricks connection

Configure your dbt profile in `~/.dbt/profiles.yml`. Set up the appropriate Databricks host, SQL warehouse HTTP path, catalog, schema, and authentication.

**Security:** Never commit access tokens, passwords, or other secrets to GitHub.

### 4. Validate the connection

```bash
dbt debug
```

### 5. Install dbt packages

```bash
dbt deps
```

### 6. Run the project

Build using the development target:

```bash
dbt build --target dev
```

To use the production target, only do so when you have verified the production configuration and are authorized to deploy:

```bash
dbt build --target prod
```

## 🧪 Testing and Validation

Run data tests:

```bash
dbt test
```

Compile models without executing them:

```bash
dbt compile
```

## 🔐 Security

- Keep `profiles.yml` outside the repository.
- Never commit Databricks credentials, access tokens, or `.env` files.
- Exclude generated logs and build artifacts using `.gitignore`.
- Use appropriate access controls for production resources.

## 🎯 Learning Objectives

This project supports practical learning in:

- dbt project configuration and model materialization
- Jinja templating and macros
- Data testing and validation
- Snapshot strategies and historical tracking
- Development and production target configuration
- Git branching, commits, and GitHub workflows

## 👨‍💻 Author

**Chandra Bhushan Singh**

Junior Data Engineer | SQL | Python | dbt | Databricks | Snowflake

---

*This project is intended for learning and portfolio development. Review all configurations and data access permissions before running workloads against production environments.*
