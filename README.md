# 🚀 Cryptocurrency Transaction & Blockchain Audit System

A **Database Management System (DBMS) project** that simulates cryptocurrency transactions and implements a **blockchain-inspired audit mechanism** to ensure transaction integrity and detect tampering.

This project demonstrates how **relational databases and blockchain concepts** can be combined to build a transparent and auditable financial transaction system.

---

# 📌 Project Overview

Cryptocurrency systems rely on **immutable ledgers and cryptographic hashes** to maintain data integrity.
This project simulates that behavior using a **relational database**, where transactions are grouped into blocks and linked together through hashes to form a blockchain-like structure.

The system allows:

* Recording cryptocurrency transactions
* Grouping transactions into blocks
* Linking blocks using cryptographic hashes
* Running audit queries to detect tampering
* Maintaining a transparent transaction history

---

# 👨‍💻 Team Members

| Name              | Role                                                        |
| ----------------- | ----------------------------------------------------------- |
| **Harshil Patel** | Database architecture, schema design, repository management |
| **Sujal Bathani** | Transaction logic and wallet management                     |
| **Krishiv Patel** | Blockchain validation and audit queries                     |

---

# ⚙️ Technologies Used

| Technology                   | Purpose                               |
| ---------------------------- | ------------------------------------- |
| **SQL (MySQL / PostgreSQL)** | Database design and queries           |
| **DBMS Concepts**            | Normalization, transactions, indexing |
| **Blockchain Concepts**      | Hash chaining, block verification     |
| **Git & GitHub**             | Version control and collaboration     |
| **LaTeX**                    | Project documentation                 |

---

# 🧠 System Architecture

The system consists of three main components:

### 1️⃣ Database Layer

Stores all data including:

* Users
* Wallets
* Transactions
* Blocks
* Audit logs

### 2️⃣ Blockchain Logic Layer

Handles:

* Block creation
* Hash generation
* Transaction grouping
* Chain verification

### 3️⃣ Audit Layer

Runs verification queries to detect:

* Block tampering
* Transaction inconsistencies
* Chain breaks

---

# 🗂️ Project Structure

```
crypto-transaction-blockchain-audit-system
│
├── README.md
│
├── database
│   ├── schema.sql
│   ├── tables.sql
│   └── sample_data.sql
│
├── queries
│   └── audit_queries.sql
│
├── blockchain_logic
│   └── block_validation.sql
│
├── docs
│   ├── er_diagram.png
│   ├── system_architecture.png
│   └── project_report.pdf
│
└── frontend
    └── dashboard_mockup.png
```

---

# 🗄️ Database Schema

The system includes the following main tables:

| Table                  | Description                                   |
| ---------------------- | --------------------------------------------- |
| **Users**              | Stores registered system users                |
| **Wallets**            | Contains wallet addresses and balances        |
| **Transactions**       | Records all cryptocurrency transfers          |
| **Blocks**             | Groups transactions into blockchain blocks    |
| **Block_Transactions** | Maps transactions to blocks                   |
| **Audit_Log**          | Stores results of blockchain integrity checks |

---

# 🔗 Blockchain Simulation

Each block contains:

* Previous block hash
* Merkle root / transaction hash summary
* Block timestamp
* Block index
* Number of transactions

Blocks are linked like this:

```
Block 1 → Hash → Block 2 → Hash → Block 3
```

If any transaction is modified, the **hash changes**, and the audit system detects the inconsistency.

---

# 🔍 Audit System

The audit module verifies:

✔ Block hash integrity
✔ Previous hash chain validity
✔ Transaction hash consistency

Example audit query:

```sql
SELECT b.block_index, b.previous_hash, p.block_hash AS prev_block_hash
FROM blocks b
LEFT JOIN blocks p ON p.block_index = b.block_index - 1
WHERE b.previous_hash <> p.block_hash;
```

This query detects **broken blockchain links**.

---

# 🧪 Example Workflow

1️⃣ Create users and wallets

2️⃣ Record cryptocurrency transactions

3️⃣ Store pending transactions

4️⃣ Generate blocks containing transactions

5️⃣ Compute block hashes

6️⃣ Run audit queries to verify integrity

---

# ▶️ How to Run the Project

### 1️⃣ Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/crypto-transaction-blockchain-audit-system.git
```

---

### 2️⃣ Navigate into the project

```bash
cd crypto-transaction-blockchain-audit-system
```

---

### 3️⃣ Create database

```sql
CREATE DATABASE crypto_audit;
```

---

### 4️⃣ Import schema

```bash
source database/schema.sql
```

---

### 5️⃣ Insert sample data

```bash
source database/sample_data.sql
```

---

### 6️⃣ Run audit queries

```bash
source queries/audit_queries.sql
```

---

# 📊 Example Features

✔ Wallet balance management
✔ Transaction logging
✔ Block creation and linking
✔ Blockchain verification queries
✔ Fraud / tampering detection

---

# 🔒 Security Considerations

* Transaction hashes protect data integrity
* Blockchain chaining prevents silent modification
* Database constraints enforce relational consistency
* Audit queries detect suspicious activity

---

# 🚀 Future Improvements

* Implement **Merkle Tree hashing**
* Build a **web dashboard for blockchain visualization**
* Add **API layer using Node.js / Python**
* Implement **cryptographic signatures for transactions**
* Real-time blockchain monitoring

---

# 📷 Future Demo (Optional)

You can add screenshots here once UI or dashboards are built.

---

# 📜 License

This project is developed for **educational purposes** as part of a DBMS course.

---

# ⭐ Support

If you find this project interesting:

⭐ Star the repository
🍴 Fork it
📢 Share it with others

---

# 📬 Contact

**Harshil Patel**
CSE Student – IIIT Vadodara International Campus Diu

GitHub: https://github.com/Marshmellow31
