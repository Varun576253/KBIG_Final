# 🚀 KBIG — Karnataka Business Identity Graph

PASSWORD- kbig-admin

> **One Unified Identity Across Government Departments**

KBIG is a full-stack government-tech platform that intelligently links business records across multiple government departments and generates a **Unified Business Identifier (UBID)** for every business entity.

The platform helps eliminate duplicate records, improve governance visibility, simplify verification workflows, and create a connected business identity ecosystem across Karnataka.

---

# 🌟 Key Features

- 🔗 Unified Business Identifier (UBID) generation
- 🧠 Multi-signal intelligent matching engine
- 📂 CSV bulk upload support
- 📝 Manual record creation
- 👨‍⚖️ Reviewer decision portal
- 📊 Real-time analytics dashboard
- 📜 Complete audit logging
- 🔄 Manual & auto sync support
- 🏢 Department-scoped access control
- 📈 Business activity tracking

---

# 🧠 Intelligent Matching Engine

KBIG compares records using multiple identity signals:

- GSTIN
- PAN
- Phone Number
- PIN Code
- Address Similarity
- Owner Name Similarity
- Business Name Similarity

## Match Outcomes

| Outcome | Description |
|---|---|
| ✅ Auto-Link | High-confidence records are automatically merged |
| ⚠️ Review Needed | Sent to reviewer for manual verification |
| ❌ Keep Separate | Weak/conflicting records remain isolated |

---

# 🏗️ Tech Stack

## Frontend
- React 18
- TypeScript
- Vite
- React Router
- Tailwind CSS

## Backend
- Node.js
- Express
- TypeScript

## Utilities
- PapaParse
- Lucide React
- Node Assert + tsx Testing

---

# 📁 Project Structure

```text
KBIG-PROJECT/
│
├── server/
│   ├── index.ts
│   ├── matchingEngine.ts
│   ├── matchingEngine.test.ts
│   └── mockData.ts
│
├── src/
│   ├── App.tsx
│   ├── components/
│   ├── context/
│   ├── hooks/
│   ├── pages/
│   └── utils/
│
├── package.json
└── vite.config.ts
```

---

# ⚙️ Installation & Setup

## 1️⃣ Clone Repository

```bash
git clone <repository-url>
cd KBIG-PROJECT
```

---

## 2️⃣ Install Dependencies

```bash
npm install
```

---

# ▶️ Running the Project

## Start Full Development Environment

```bash
npm run dev
```

This starts:

| Service | URL |
|---|---|
| Backend API | http://localhost:3001 |
| Frontend | http://localhost:5173 |

Open:

```text
http://localhost:5173
```

in the browser.

---

# 🏃 Available Scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Start frontend + backend together |
| `npm run client` | Start frontend only |
| `npm run server` | Start backend only |
| `npm run build` | Build frontend |
| `npm start` | Run production build |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | Run TypeScript checks |
| `npm test` | Run matching engine tests |

---

# 👥 Roles & Access

## 🏢 Department Views

Available Departments:
- Shop & Establishment
- Factories
- KSPCB

Department users:
- Do not require passwords
- Can only view department-specific records

---

## 🔐 Admin View

Admin users can access:
- Review Queue
- Analytics Dashboard
- Threshold Tuning
- Audit Logs
- Sync Operations

### Demo Password

```text
kbig-admin
```

---

# 🔄 Complete System Flow

```text
Department Records / CSV Upload / Sync APIs
                    ↓
         Backend Validation Layer
                    ↓
      Multi-Signal Matching Engine
                    ↓
       Confidence Score Generation
                    ↓
 ┌─────────────────────────────────┐
 │  Auto-Link / Review / Separate  │
 └─────────────────────────────────┘
                    ↓
          UBID Graph Generation
                    ↓
     Analytics + Audit Log Refresh
                    ↓
       Dashboard & Department View
```

---

# 📂 CSV Upload Support

## Required Fields

```csv
business_name,address
```

## Optional Fields

```csv
owner_name,pin_code,phone,pan,gstin,source_record_id
```

---

## Example CSV

```csv
business_name,owner_name,address,pin_code,phone,pan,gstin
Basava Precision Tools,Mahesh Gowda,18 Peenya Industrial Area Phase 1,560058,9811122233,KBGAA1001P,29KBGAA1001P1Z3
```

---

# 👨‍⚖️ Reviewer Workflow

The reviewer portal helps validate uncertain matches.

### Reviewer Actions
- ✅ Approve Merge
- ❌ Reject Match
- 🔀 Split UBID
- ⏳ Defer Review

Reviewer decisions are preserved during future matching runs.

---

# 📊 Analytics Dashboard

KBIG provides governance-level insights:

- Total UBIDs
- Match Outcomes
- Department Coverage
- Pending Reviews
- Confidence Bands
- Event Statistics
- Linked Record Counts

---

# 📜 Audit Logging

Every important system action is tracked:

- Auto-link operations
- Reviewer decisions
- CSV uploads
- Threshold updates
- Sync operations
- Record creation
- Event creation

This ensures:
- Transparency
- Accountability
- Traceability

---

# 🔌 Main API Endpoints

| Endpoint | Purpose |
|---|---|
| `POST /api/auth/admin` | Admin login |
| `GET /api/ubids` | Fetch UBIDs |
| `GET /api/ubids/:id` | UBID details |
| `POST /api/match` | Recompute matching |
| `POST /api/records` | Add record |
| `POST /api/records/bulk` | Bulk upload |
| `GET /api/review-queue` | Pending reviews |
| `POST /api/review/:pairId` | Reviewer decision |
| `GET /api/analytics` | Analytics summary |
| `POST /api/sync` | Manual sync |
| `POST /api/sync/auto` | Auto sync |
| `GET /api/audit-log` | Audit history |

---

# 🧪 Testing

Run tests using:

```bash
npm test
```

Tests validate:
- Exact GSTIN matching
- Duplicate handling
- Confidence scoring
- Reviewer approvals/rejections
- Split operations
- Review queue logic

---

# 🚀 Future Enhancements

- 🗄️ PostgreSQL / Supabase integration
- 🤖 AI/ML-based entity resolution
- ☁️ Cloud deployment
- 🔐 Secure authentication
- 📈 Historical analytics
- 🛰️ Real government API integration
- 🚨 Fraud detection system

---

# 🌍 Real-World Impact

KBIG helps:
- Reduce duplicate records
- Improve department coordination
- Speed up verification workflows
- Improve governance visibility
- Build a unified business identity layer

---

# 📌 Conclusion

KBIG transforms fragmented departmental business records into a unified, intelligent, and transparent governance identity ecosystem.

> **“From isolated records to connected governance.”**

---

# 👨‍💻 Built For

Hackathons • Government-Tech Innovation • Smart Governance Systems
