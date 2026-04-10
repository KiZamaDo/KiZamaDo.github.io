<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grievance Automation Platform — Architecture & Plan</title>
  <script src="https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.min.js"></script>
  <style>
    :root {
      --bg: #ffffff;
      --surface: #f6f8fa;
      --border: #d1d9e0;
      --text: #1f2328;
      --muted: #59636e;
      --accent: #0969da;
      --accent2: #1a7f37;
      --accent3: #8250df;
      --accent4: #bc4c00;
      --danger: #cf222e;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
</style>
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    header {
      text-align: center;
      padding: 3rem 1rem 2rem;
      border-bottom: 1px solid var(--border);
      background: linear-gradient(135deg, #f0f7ff 0%, #f6f0ff 50%, #fff5f0 100%);
    }
    header h1 { font-size: 2.2rem; font-weight: 700; }
    header p { color: var(--muted); margin-top: .5rem; font-size: 1.05rem; max-width: 700px; margin-left: auto; margin-right: auto; }
    .container { max-width: 1400px; margin: 0 auto; padding: 2rem 1.5rem; }
    section { margin-bottom: 3rem; }
    section h2 {
      font-size: 1.45rem;
      color: var(--accent);
      margin-bottom: .5rem;
      padding-bottom: .5rem;
      border-bottom: 1px solid var(--border);
    }
    section p.desc {
      color: var(--muted);
      margin-bottom: 1.5rem;
      max-width: 900px;
    }
    .mermaid {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 2rem 1rem;
      overflow-x: auto;
      margin-bottom: 1rem;
    }
    .mermaid svg { max-width: 100%; height: auto; }
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 1.5rem; }
    .grid-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.2rem; }
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.5rem;
    }
    .card h3 { font-size: 1.05rem; margin-bottom: .5rem; }
    .card p, .card ul { color: var(--muted); font-size: .93rem; }
    .card ul { padding-left: 1.2rem; }
    .card ul li { margin-bottom: .25rem; }
    .card code { background: #eff1f3; padding: 1px 5px; border-radius: 4px; font-size: .85rem; }
    .badge {
      display: inline-block;
      font-size: .72rem;
      padding: 2px 8px;
      border-radius: 999px;
      font-weight: 600;
      margin-right: .4rem;
      vertical-align: middle;
    }
    .badge-blue { background: #ddf4ff; color: var(--accent); }
    .badge-green { background: #dafbe1; color: var(--accent2); }
    .badge-purple { background: #fbefff; color: var(--accent3); }
    .badge-orange { background: #fff1e5; color: var(--accent4); }
    .badge-red { background: #ffebe9; color: var(--danger); }
    .phase-tag {
      display: inline-block;
      font-size: .7rem;
      padding: 2px 10px;
      border-radius: 999px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: .5px;
      margin-left: .5rem;
      vertical-align: middle;
    }
    .phase-tag.p1 { background: #ddf4ff; color: var(--accent); }
    .phase-tag.p2 { background: #dafbe1; color: var(--accent2); }
    .phase-tag.p3 { background: #fbefff; color: var(--accent3); }
    .phase-tag.p4 { background: #fff1e5; color: var(--accent4); }
    table {
      width: 100%;
      border-collapse: collapse;
      font-size: .93rem;
      margin-top: 1rem;
    }
    th, td {
      text-align: left;
      padding: .6rem .8rem;
      border: 1px solid var(--border);
    }
    th { background: var(--surface); font-weight: 600; }
    td { color: var(--muted); }
    footer {
      text-align: center;
      padding: 2rem;
      color: var(--muted);
      border-top: 1px solid var(--border);
      font-size: .9rem;
    }
  </style>
</head>
<body>
<header>
  <h1>Grievance Automation Platform</h1>
  <p>SOP-driven, LLM-powered code generation for automating repetitive CRM grievance tickets — from upload to ServiceNow deployment</p>
</header>
<div class="container">
<!-- ============================================================ -->
<!-- 1. PLATFORM OVERVIEW -->
<!-- ============================================================ -->
<section>
  <h2>1. Platform Overview — End-to-End Flow</h2>
  <p class="desc">
    A user uploads an SOP document describing how a grievance type is resolved, along with sample input/output pairs.
    The platform parses the SOP, generates executable code via AWS Bedrock, tests it against the samples,
    and on success deploys it as a ServiceNow Automation Record.
  </p>
  <div class="mermaid">
graph TB
    subgraph Upload["① Upload & Parse"]
        USER["CRM Analyst"]
        SOP["SOP Document<br/>(PDF / DOCX / Markdown)"]
        SAMPLES["Sample I/O Pairs<br/>(CSV / JSON / Excel)"]
        PARSER["SOP Parser<br/>Extract steps, rules,<br/>DB queries, conditions"]
    end

    subgraph Generate["② LLM Code Generation"]
        BEDROCK["AWS Bedrock<br/>Claude / Titan"]
        PROMPT_ENG["Prompt Engine<br/>SOP → structured prompt"]
        CODE_GEN["Generated Code<br/>Python / JS runbook"]
        SCHEMA_DISC["Schema Discovery<br/>DB introspection"]
    end

    subgraph Test["③ Automated Testing"]
        SANDBOX["Sandbox Environment<br/>Isolated DB replica"]
        RUNNER["Test Runner<br/>Sample I/O validation"]
        DIFF["Output Diff Engine<br/>Expected vs Actual"]
        RETRY["Retry Loop<br/>Fix code via LLM"]
    end

    subgraph Deploy["④ Deploy & Register"]
        STAGING["Staging Validation<br/>Dry-run on live data"]
        SNOW["ServiceNow API<br/>Create Automation Record"]
        MONITOR["Monitoring<br/>Execution logs + alerts"]
        ROLLBACK["Rollback<br/>Version control"]
    end

    USER -->|"uploads"| SOP
    USER -->|"uploads"| SAMPLES
    SOP --> PARSER
    SAMPLES --> PARSER

    PARSER -->|"structured SOP"| PROMPT_ENG
    PROMPT_ENG --> BEDROCK
    SCHEMA_DISC -->|"table schemas"| PROMPT_ENG
    BEDROCK -->|"generated code"| CODE_GEN

    CODE_GEN --> SANDBOX
    SAMPLES -->|"test cases"| RUNNER
    SANDBOX --> RUNNER
    RUNNER --> DIFF
    DIFF -->|"failures"| RETRY
    RETRY -->|"fix prompt"| BEDROCK
    DIFF -->|"all pass"| STAGING

    STAGING -->|"approved"| SNOW
    SNOW --> MONITOR
    MONITOR -->|"failure spike"| ROLLBACK

    style Upload fill:#ddf4ff,stroke:#0969da,stroke-width:2px,color:#1f2328
    style Generate fill:#fbefff,stroke:#8250df,stroke-width:2px,color:#1f2328
    style Test fill:#dafbe1,stroke:#1a7f37,stroke-width:2px,color:#1f2328
    style Deploy fill:#fff1e5,stroke:#bc4c00,stroke-width:2px,color:#1f2328
  </div>
</section>
<!-- ============================================================ -->
<!-- 2. SYSTEM ARCHITECTURE -->
<!-- ============================================================ -->
<section>
  <h2>2. System Architecture — Component Map</h2>
  <p class="desc">
    Inspired by the Claude Code codebase patterns: a core engine with pluggable tools, immutable state management,
    transport-agnostic I/O, and a permission/validation layer before any destructive operation.
  </p>
  <div class="mermaid">
graph TB
    subgraph Frontend["🖥️ Web Portal (React)"]
        UPLOAD_UI["SOP Upload UI<br/>Drag-drop + form"]
        DASH["Dashboard<br/>Automation status"]
        TEST_VIEW["Test Results Viewer<br/>Diff + logs"]
        APPROVAL["Approval Workflow<br/>Human-in-the-loop"]
    end

    subgraph API["⚡ API Layer (FastAPI / Node)"]
        REST["REST API<br/>CRUD + webhooks"]
        AUTH["Auth Middleware<br/>SSO / RBAC"]
        QUEUE["Task Queue<br/>SQS / Celery"]
        WS_API["WebSocket<br/>Live progress"]
    end

    subgraph Core["⚙️ Core Engine"]
        SOP_PARSER["SOP Parser<br/>PDF/DOCX → structured JSON"]
        PROMPT_BUILD["Prompt Builder<br/>SOP + schema → prompt"]
        CODE_ENGINE["Code Generation Engine<br/>Bedrock API calls"]
        TEST_ENGINE["Test Engine<br/>Sandbox execution"]
        DEPLOY_ENGINE["Deploy Engine<br/>ServiceNow integration"]
    end

    subgraph Infra["☁️ AWS Infrastructure"]
        BEDROCK_SVC["AWS Bedrock<br/>Claude 3.5 / Titan"]
        S3["S3<br/>SOP docs + artifacts"]
        RDS["RDS / Aurora<br/>Platform metadata"]
        SANDBOX_DB["Sandbox DB<br/>Isolated replica"]
        SECRETS["Secrets Manager<br/>DB creds + API keys"]
        LAMBDA["Lambda<br/>Async code execution"]
    end

    subgraph External["🔗 External Systems"]
        CRM_DB["CRM Database<br/>Production"]
        SNOW_API["ServiceNow API<br/>Automation Records"]
        SLACK_INT["Slack / Teams<br/>Notifications"]
    end

    Frontend --> API
    API --> Core
    Core --> Infra
    Core --> External

    UPLOAD_UI --> REST
    REST --> SOP_PARSER
    SOP_PARSER --> PROMPT_BUILD
    PROMPT_BUILD --> CODE_ENGINE
    CODE_ENGINE --> BEDROCK_SVC
    CODE_ENGINE --> TEST_ENGINE
    TEST_ENGINE --> SANDBOX_DB
    TEST_ENGINE -->|"pass"| DEPLOY_ENGINE
    DEPLOY_ENGINE --> SNOW_API
    DEPLOY_ENGINE --> CRM_DB

    QUEUE --> CODE_ENGINE
    QUEUE --> TEST_ENGINE
    WS_API --> DASH

    style Frontend fill:#ddf4ff,stroke:#0969da,stroke-width:2px,color:#1f2328
    style API fill:#f0f7ff,stroke:#0969da,color:#1f2328
    style Core fill:#dafbe1,stroke:#1a7f37,stroke-width:2px,color:#1f2328
    style Infra fill:#fbefff,stroke:#8250df,stroke-width:2px,color:#1f2328
    style External fill:#fff1e5,stroke:#bc4c00,stroke-width:2px,color:#1f2328
  </div>
</section>
<!-- ============================================================ -->
<!-- 3. SOP PARSING PIPELINE -->
<!-- ============================================================ -->
<section>
  <h2>3. SOP Parsing Pipeline — Document to Structured Intent</h2>
  <p class="desc">
    The SOP document is the source of truth. The parser extracts a structured representation:
    steps, decision branches, DB operations, validation rules, and expected outcomes.
    This structured SOP becomes the prompt context for code generation.
  </p>
  <div class="mermaid">
graph LR
    subgraph Input["Raw Input"]
        PDF["PDF / DOCX"]
        MD["Markdown"]
        FORM["Structured Form<br/>(manual entry)"]
    end

    subgraph Extract["Extraction Layer"]
        OCR["Text Extraction<br/>PyPDF2 / python-docx"]
        LLM_PARSE["LLM Parsing<br/>Bedrock: extract structure"]
        VALIDATE_SOP["Schema Validation<br/>Required fields check"]
    end

    subgraph StructuredSOP["Structured SOP (JSON)"]
        META["Metadata<br/>name, category, priority"]
        STEPS["Ordered Steps<br/>1. Fetch ticket<br/>2. Query customer<br/>3. Check policy<br/>4. Apply resolution"]
        DECISIONS["Decision Trees<br/>if amount > X → escalate<br/>if status == Y → close"]
        DB_OPS["DB Operations<br/>SELECT, UPDATE, INSERT<br/>table names, joins"]
        VALIDATIONS["Validation Rules<br/>required fields,<br/>value ranges, formats"]
        OUTPUTS["Expected Outputs<br/>status changes,<br/>notifications, logs"]
    end

    subgraph Enrichment["Schema Enrichment"]
        DB_INTRO["DB Introspection<br/>INFORMATION_SCHEMA"]
        FK_MAP["FK Relationship Map"]
        ENUM_VALS["Enum / Lookup Values"]
    end

    Input --> Extract
    Extract --> StructuredSOP
    Enrichment -->|"augment"| StructuredSOP

    PDF --> OCR
    MD --> OCR
    FORM --> VALIDATE_SOP
    OCR --> LLM_PARSE
    LLM_PARSE --> VALIDATE_SOP

    DB_INTRO --> FK_MAP
    DB_INTRO --> ENUM_VALS

    style Input fill:#fff1e5,stroke:#bc4c00,color:#1f2328
    style Extract fill:#fbefff,stroke:#8250df,color:#1f2328
    style StructuredSOP fill:#dafbe1,stroke:#1a7f37,color:#1f2328
    style Enrichment fill:#ddf4ff,stroke:#0969da,color:#1f2328
  </div>
</section>

<!-- ============================================================ -->
<!-- 4. CODE GENERATION ENGINE -->
<!-- ============================================================ -->
<section>
  <h2>4. Code Generation Engine — LLM-Powered Runbook Builder</h2>
  <p class="desc">
    Inspired by Claude Code's QueryEngine pattern: an iterative loop where the LLM generates code,
    the system validates it, and failures feed back as context for the next generation attempt.
    The prompt includes the structured SOP, DB schema, and a code template with guardrails.
  </p>
  <div class="mermaid">
sequenceDiagram
    participant PB as Prompt Builder
    participant BR as AWS Bedrock
    participant VAL as Code Validator
    participant SB as Sandbox
    participant STORE as Artifact Store

    PB->>PB: Assemble prompt:<br/>structured SOP + DB schema<br/>+ code template + guardrails

    loop Generation Loop (max 5 attempts)
        PB->>BR: Generate code (streaming)
        BR-->>PB: Python/JS runbook

        PB->>VAL: Static analysis<br/>(AST parse, lint, type check)

        alt Syntax/Lint errors
            VAL-->>PB: Error details
            PB->>PB: Append errors to prompt context
        else Valid code
            VAL-->>PB: Pass

            PB->>SB: Execute against sandbox DB
            SB-->>PB: Runtime result

            alt Runtime error
                PB->>PB: Append traceback to prompt
            else Success
                PB->>STORE: Save versioned artifact
                Note over STORE: code + metadata + SOP ref
            end
        end
    end

    PB-->>PB: Max attempts → flag for human review
  </div>
</section>
<!-- ============================================================ -->
<!-- 5. PROMPT ENGINEERING STRATEGY -->
<!-- ============================================================ -->
<section>
  <h2>5. Prompt Engineering Strategy</h2>
  <p class="desc">
    The prompt is the most critical piece. It must produce safe, correct, idempotent code
    that handles edge cases. The strategy uses a layered prompt with system instructions,
    SOP context, schema context, and output constraints.
  </p>
  <div class="mermaid">
graph TB
    subgraph PromptLayers["Prompt Assembly (layered)"]
        L1["Layer 1: System Instructions<br/>You are a code generator for CRM automation.<br/>Generate safe, idempotent Python code.<br/>Always use parameterized queries.<br/>Never DELETE without WHERE clause.<br/>Always wrap in transactions."]
        L2["Layer 2: SOP Context<br/>Structured SOP JSON<br/>(steps, decisions, DB ops)"]
        L3["Layer 3: DB Schema<br/>Table definitions, FKs,<br/>column types, enums,<br/>sample rows"]
        L4["Layer 4: Code Template<br/>Function signature,<br/>logging pattern,<br/>error handling skeleton,<br/>rollback pattern"]
        L5["Layer 5: Output Constraints<br/>Return format,<br/>status codes,<br/>audit trail fields"]
        L6["Layer 6: Sample I/O<br/>Input ticket → expected output<br/>(few-shot examples)"]
    end

    subgraph Guardrails["Safety Guardrails"]
        G1["No raw SQL — ORM or parameterized only"]
        G2["Transaction wrapping mandatory"]
        G3["Idempotency check at entry"]
        G4["Audit log every mutation"]
        G5["Rate limiting on external calls"]
        G6["Timeout on all DB operations"]
    end

    L1 --> L2 --> L3 --> L4 --> L5 --> L6
    PromptLayers --> Guardrails

    style PromptLayers fill:#fbefff,stroke:#8250df,color:#1f2328
    style Guardrails fill:#ffebe9,stroke:#cf222e,color:#1f2328
  </div>
</section>

<!-- ============================================================ -->
<!-- 6. TESTING PIPELINE -->
<!-- ============================================================ -->
<section>
  <h2>6. Testing Pipeline — Rigorous Validation Before Deploy</h2>
  <p class="desc">
    Inspired by the Claude Code codebase's permission system and sandbox patterns:
    every generated runbook goes through multiple validation gates before it touches production.
    The test pipeline uses the uploaded sample I/O as ground truth.
  </p>
  <div class="mermaid">
graph TB
    subgraph Gate1["Gate 1: Static Analysis"]
        AST["AST Parse<br/>Valid syntax?"]
        LINT["Linter<br/>Style + safety rules"]
        TYPE["Type Check<br/>mypy / pyright"]
        SEC["Security Scan<br/>SQL injection patterns,<br/>hardcoded creds,<br/>unsafe operations"]
    end

    subgraph Gate2["Gate 2: Unit Tests (Sandbox)"]
        SEED["Seed sandbox DB<br/>from sample inputs"]
        EXEC["Execute runbook<br/>against each sample"]
        COMPARE["Compare output<br/>vs expected output"]
        COVERAGE["Coverage check<br/>all SOP branches hit?"]
    end

    subgraph Gate3["Gate 3: Integration Tests"]
        EDGE["Edge cases<br/>null fields, duplicates,<br/>concurrent execution"]
        IDEM["Idempotency test<br/>run twice, same result"]
        ROLLBACK_T["Rollback test<br/>force error mid-run,<br/>verify clean state"]
        PERF["Performance test<br/>execution time < threshold"]
    end

    subgraph Gate4["Gate 4: Staging Dry-Run"]
        LIVE_DATA["Run against staging<br/>with real data snapshot"]
        HUMAN["Human review<br/>of output diff"]
        APPROVE["Approval gate<br/>manager sign-off"]
    end

    Gate1 -->|"pass"| Gate2
    Gate2 -->|"pass"| Gate3
    Gate3 -->|"pass"| Gate4
    Gate4 -->|"approved"| DEPLOY["Deploy to Production"]

    Gate1 -->|"fail"| FIX1["Feed errors to LLM<br/>regenerate code"]
    Gate2 -->|"fail"| FIX2["Feed diff to LLM<br/>fix logic"]
    Gate3 -->|"fail"| FIX3["Feed failure to LLM<br/>add handling"]

    style Gate1 fill:#ddf4ff,stroke:#0969da,color:#1f2328
    style Gate2 fill:#dafbe1,stroke:#1a7f37,color:#1f2328
    style Gate3 fill:#fbefff,stroke:#8250df,color:#1f2328
    style Gate4 fill:#fff1e5,stroke:#bc4c00,color:#1f2328
  </div>
</section>
<!-- ============================================================ -->
<!-- 7. SERVICENOW DEPLOYMENT -->
<!-- ============================================================ -->
<section>
  <h2>7. ServiceNow Deployment — Automation Record Lifecycle</h2>
  <p class="desc">
    Once code passes all gates, the platform creates an Automation Record in ServiceNow
    via the Table API. The record links the runbook, SOP reference, test results, and
    execution configuration. ServiceNow's Flow Designer triggers the runbook on matching tickets.
  </p>
  <div class="mermaid">
sequenceDiagram
    participant Platform as Automation Platform
    participant S3 as S3 Artifact Store
    participant SNOW as ServiceNow API
    participant FD as Flow Designer
    participant CRM as CRM Database

    Platform->>S3: Upload runbook artifact<br/>(versioned, signed)
    Platform->>SNOW: POST /api/now/table/x_auto_record<br/>Create Automation Record

    Note over SNOW: Record contains:<br/>• SOP reference ID<br/>• Runbook S3 URI<br/>• Trigger conditions<br/>• Test result summary<br/>• Rollback version<br/>• Owner / approver

    SNOW->>FD: Register trigger rule<br/>(grievance_type == X<br/>AND status == new)

    Note over FD: When matching ticket arrives:

    FD->>Platform: Webhook: execute runbook
    Platform->>S3: Fetch runbook
    Platform->>CRM: Execute runbook<br/>(parameterized queries)
    CRM-->>Platform: Result
    Platform->>SNOW: Update ticket<br/>+ attach execution log
    Platform->>SNOW: Update Automation Record<br/>(last_run, success_count)
  </div>
</section>

<!-- ============================================================ -->
<!-- 8. DATA MODEL -->
<!-- ============================================================ -->
<section>
  <h2>8. Data Model — Platform Entities</h2>
  <p class="desc">
    The platform's own metadata store tracks SOPs, generated runbooks, test runs, deployments,
    and execution history. This is separate from the CRM database the runbooks operate on.
  </p>
  <div class="mermaid">
erDiagram
    SOP {
        uuid id PK
        string name
        string category
        text raw_content
        json structured_content
        string status "draft|active|archived"
        timestamp created_at
        string uploaded_by
    }

    SAMPLE_IO {
        uuid id PK
        uuid sop_id FK
        json input_data
        json expected_output
        string source "historical|manual"
    }

    RUNBOOK {
        uuid id PK
        uuid sop_id FK
        int version
        text code
        string language "python|javascript"
        string status "generated|testing|passed|failed|deployed"
        json generation_metadata
        timestamp created_at
    }

    TEST_RUN {
        uuid id PK
        uuid runbook_id FK
        string gate "static|unit|integration|staging"
        string result "pass|fail"
        json details
        float duration_ms
        timestamp run_at
    }

    DEPLOYMENT {
        uuid id PK
        uuid runbook_id FK
        string snow_record_id
        string environment "staging|production"
        string status "active|rolled_back|disabled"
        timestamp deployed_at
        string deployed_by
    }

    EXECUTION_LOG {
        uuid id PK
        uuid deployment_id FK
        string ticket_id
        string result "success|failure|timeout"
        json input_snapshot
        json output_snapshot
        float duration_ms
        timestamp executed_at
    }

    SOP ||--o{ SAMPLE_IO : "has samples"
    SOP ||--o{ RUNBOOK : "generates"
    RUNBOOK ||--o{ TEST_RUN : "tested by"
    RUNBOOK ||--o{ DEPLOYMENT : "deployed as"
    DEPLOYMENT ||--o{ EXECUTION_LOG : "produces"
  </div>
</section>
<!-- ============================================================ -->
<!-- 9. SECURITY & SAFETY MODEL -->
<!-- ============================================================ -->
<section>
  <h2>9. Security & Safety Model</h2>
  <p class="desc">
    Borrowing from Claude Code's fail-closed permission system: every generated operation
    must pass through multiple safety layers. No code runs against production without
    explicit human approval and passing all automated gates.
  </p>
  <div class="mermaid">
graph TB
    subgraph CodeSafety["Code Safety (build time)"]
        PARAM["Parameterized queries only<br/>No string concatenation in SQL"]
        TRANS["Transaction wrapping<br/>Auto-rollback on error"]
        IDEM_C["Idempotency guard<br/>Check-before-write pattern"]
        AUDIT["Audit trail<br/>Log every mutation with before/after"]
        TIMEOUT["Timeout enforcement<br/>Max 30s per operation"]
    end

    subgraph AccessControl["Access Control (runtime)"]
        RBAC["RBAC<br/>Analyst → upload<br/>Reviewer → approve<br/>Admin → deploy"]
        DB_PERMS["DB Permissions<br/>Runbook user has<br/>SELECT + UPDATE only<br/>No DROP, TRUNCATE, DELETE*"]
        SNOW_SCOPE["ServiceNow Scope<br/>Scoped app, limited tables"]
        SECRETS_MGR["Secrets Manager<br/>No creds in code"]
    end

    subgraph RuntimeSafety["Runtime Safety"]
        SANDBOX_ISO["Sandbox Isolation<br/>Separate DB, no prod access"]
        RATE_LIMIT["Rate Limiting<br/>Max executions per minute"]
        CIRCUIT["Circuit Breaker<br/>Disable on failure spike"]
        ROLLBACK_AUTO["Auto-Rollback<br/>Revert on error rate > 5%"]
    end

    subgraph Observability["Observability"]
        LOGS["Structured Logs<br/>CloudWatch / ELK"]
        METRICS["Metrics<br/>Success rate, latency, errors"]
        ALERTS["Alerts<br/>PagerDuty / Slack"]
        DRIFT["Drift Detection<br/>Schema changes → disable"]
    end

    CodeSafety --> AccessControl
    AccessControl --> RuntimeSafety
    RuntimeSafety --> Observability

    style CodeSafety fill:#ffebe9,stroke:#cf222e,color:#1f2328
    style AccessControl fill:#ddf4ff,stroke:#0969da,color:#1f2328
    style RuntimeSafety fill:#fff1e5,stroke:#bc4c00,color:#1f2328
    style Observability fill:#dafbe1,stroke:#1a7f37,color:#1f2328
  </div>
</section>
<!-- ============================================================ -->
<!-- 10. SCALABILITY ARCHITECTURE -->
<!-- ============================================================ -->
<section>
  <h2>10. Scalability Architecture — Handling Volume</h2>
  <p class="desc">
    Inspired by the bridge's multi-session polling and capacity-wake patterns:
    the platform uses queue-based decoupling, async execution, and horizontal scaling
    to handle many SOPs and high-volume ticket automation simultaneously.
  </p>
  <div class="mermaid">
graph TB
    subgraph Ingestion["Ingestion (fan-in)"]
        UPLOAD_Q["Upload Queue<br/>SQS FIFO"]
        PARSE_WORKERS["Parser Workers<br/>Lambda / ECS<br/>Auto-scaling"]
    end

    subgraph Generation["Generation (CPU-bound)"]
        GEN_Q["Generation Queue<br/>SQS Standard"]
        GEN_WORKERS["Code Gen Workers<br/>ECS Fargate<br/>Bedrock API calls"]
        BEDROCK_POOL["Bedrock Connection Pool<br/>Rate-limited, retry"]
    end

    subgraph Testing["Testing (I/O-bound)"]
        TEST_Q["Test Queue<br/>SQS Standard"]
        TEST_WORKERS["Test Workers<br/>ECS Fargate<br/>Sandbox DB per worker"]
        DB_POOL["Sandbox DB Pool<br/>Pre-provisioned replicas"]
    end

    subgraph Execution["Execution (high-volume)"]
        TRIGGER_Q["Trigger Queue<br/>SQS / SNS"]
        EXEC_WORKERS["Execution Workers<br/>Lambda<br/>Concurrency: 1000"]
        CRM_POOL["CRM DB Pool<br/>Connection pooling<br/>Read replicas"]
    end

    UPLOAD_Q --> PARSE_WORKERS
    PARSE_WORKERS --> GEN_Q
    GEN_Q --> GEN_WORKERS
    GEN_WORKERS --> BEDROCK_POOL
    GEN_WORKERS --> TEST_Q
    TEST_Q --> TEST_WORKERS
    TEST_WORKERS --> DB_POOL

    TRIGGER_Q --> EXEC_WORKERS
    EXEC_WORKERS --> CRM_POOL

    style Ingestion fill:#ddf4ff,stroke:#0969da,color:#1f2328
    style Generation fill:#fbefff,stroke:#8250df,color:#1f2328
    style Testing fill:#dafbe1,stroke:#1a7f37,color:#1f2328
    style Execution fill:#fff1e5,stroke:#bc4c00,color:#1f2328
  </div>
</section>

<!-- ============================================================ -->
<!-- 11. PATTERNS BORROWED FROM CLAUDE CODE -->
<!-- ============================================================ -->
<section>
  <h2>11. Patterns Borrowed from the Claude Code Codebase</h2>
  <div class="grid">
    <div class="card">
      <h3><span class="badge badge-blue">Pattern</span> QueryEngine → Generation Engine</h3>
      <p>Claude Code's <code>QueryEngine</code> is an async generator that yields messages and retries on failure.
         Our Code Generation Engine follows the same pattern: iterate with the LLM, yield intermediate results,
         and feed failures back as context. Max 5 attempts before human escalation.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-green">Pattern</span> Tool Permission System → Safety Gates</h3>
      <p>Claude Code checks <code>canUseTool()</code> before every tool execution with allow/deny/ask modes.
         Our platform checks every generated DB operation against a safety policy:
         parameterized queries, transaction wrapping, no destructive DDL. Same fail-closed default.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-purple">Pattern</span> buildTool() Defaults → Runbook Template</h3>
      <p>Claude Code's <code>buildTool()</code> provides safe defaults (<code>isConcurrencySafe: false</code>,
         <code>isReadOnly: false</code>). Our runbook template provides safe defaults: transaction wrapping,
         timeout enforcement, audit logging. The LLM fills in the business logic; the skeleton handles safety.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-orange">Pattern</span> SerialBatchUploader → Execution Queue</h3>
      <p>Claude Code serializes all writes through one queue with backpressure and retry.
         Our execution pipeline does the same: one queue per CRM database, serial execution
         to prevent write conflicts, exponential backoff on transient failures.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-red">Pattern</span> Sandbox Isolation → Test Sandbox</h3>
      <p>Claude Code's <code>SandboxManager</code> restricts file and network access.
         Our test sandbox is an isolated DB replica where generated code runs without
         touching production. Schema-identical, data-anonymized, disposable per test run.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-blue">Pattern</span> FlushGate → Deploy Gate</h3>
      <p>Claude Code's <code>FlushGate</code> queues messages during initial flush to prevent interleaving.
         Our deploy gate queues new ticket triggers while a runbook version is being swapped,
         preventing partial execution during deployment. Same state machine: start → enqueue → end.</p>
    </div>
  </div>
</section>
<!-- ============================================================ -->
<!-- 12. IMPLEMENTATION PHASES -->
<!-- ============================================================ -->
<section>
  <h2>12. Implementation Phases — Roadmap</h2>
  <div class="mermaid">
gantt
    title Implementation Roadmap
    dateFormat YYYY-MM-DD
    axisFormat %b %Y

    section Phase 1 — Foundation
    AWS infra setup (VPC, RDS, S3, IAM)       :p1a, 2026-05-01, 14d
    Platform DB schema + API skeleton          :p1b, after p1a, 14d
    SOP upload UI + parser (PDF/DOCX)          :p1c, after p1a, 21d
    Bedrock integration + basic prompt         :p1d, after p1b, 14d

    section Phase 2 — Core Engine
    Schema discovery + prompt builder          :p2a, after p1d, 14d
    Code generation loop (retry logic)         :p2b, after p2a, 21d
    Sandbox DB provisioning                    :p2c, after p1d, 14d
    Test runner (sample I/O validation)        :p2d, after p2b, 14d

    section Phase 3 — Quality & Safety
    Static analysis gate                       :p3a, after p2d, 10d
    Integration test suite                     :p3b, after p3a, 14d
    Security scan + guardrail enforcement      :p3c, after p3a, 10d
    Human approval workflow UI                 :p3d, after p3b, 10d

    section Phase 4 — Deploy & Operate
    ServiceNow API integration                 :p4a, after p3d, 14d
    Automation Record creation                 :p4b, after p4a, 10d
    Monitoring + alerting + rollback           :p4c, after p4b, 14d
    Dashboard + execution analytics            :p4d, after p4b, 14d
  </div>
</section>

<!-- ============================================================ -->
<!-- 13. PHASE DETAILS -->
<!-- ============================================================ -->
<section>
  <h2>13. Phase Deliverables</h2>
  <div class="grid">
    <div class="card">
      <h3>Phase 1 — Foundation <span class="phase-tag p1">Weeks 1–6</span></h3>
      <ul>
        <li>AWS VPC with private subnets for DB access</li>
        <li>RDS PostgreSQL for platform metadata</li>
        <li>S3 bucket for SOP docs + runbook artifacts</li>
        <li>FastAPI service with SSO auth (your company IdP)</li>
        <li>SOP upload endpoint + PDF/DOCX text extraction</li>
        <li>LLM-based SOP structuring via Bedrock (Claude 3.5 Sonnet)</li>
        <li>React upload UI with drag-drop + preview</li>
        <li>Basic prompt template for code generation</li>
      </ul>
    </div>
    <div class="card">
      <h3>Phase 2 — Core Engine <span class="phase-tag p2">Weeks 5–10</span></h3>
      <ul>
        <li>DB schema introspection (INFORMATION_SCHEMA queries)</li>
        <li>Prompt builder: SOP + schema + template → full prompt</li>
        <li>Code generation loop with retry (max 5 attempts)</li>
        <li>Sandbox DB provisioning (RDS snapshot + restore)</li>
        <li>Test runner: seed data → execute → compare output</li>
        <li>Output diff engine (JSON deep-compare with tolerance)</li>
        <li>WebSocket progress updates to UI</li>
        <li>Artifact versioning in S3</li>
      </ul>
    </div>
    <div class="card">
      <h3>Phase 3 — Quality & Safety <span class="phase-tag p3">Weeks 9–13</span></h3>
      <ul>
        <li>AST-based static analysis (no raw SQL, no hardcoded creds)</li>
        <li>Idempotency + rollback integration tests</li>
        <li>Edge case generation (nulls, duplicates, concurrency)</li>
        <li>Performance benchmarking (< 30s per execution)</li>
        <li>Security scan (SQL injection patterns, unsafe ops)</li>
        <li>Human approval workflow with diff view</li>
        <li>Staging dry-run against anonymized prod snapshot</li>
        <li>RBAC: analyst / reviewer / admin roles</li>
      </ul>
    </div>
    <div class="card">
      <h3>Phase 4 — Deploy & Operate <span class="phase-tag p4">Weeks 12–17</span></h3>
      <ul>
        <li>ServiceNow Table API integration</li>
        <li>Automation Record creation with trigger rules</li>
        <li>Flow Designer webhook registration</li>
        <li>Execution worker (Lambda, connection-pooled)</li>
        <li>CloudWatch metrics + alarms</li>
        <li>Circuit breaker (auto-disable on failure spike)</li>
        <li>Rollback mechanism (revert to previous version)</li>
        <li>Dashboard: success rates, latency, cost per automation</li>
      </ul>
    </div>
  </div>
</section>
<!-- ============================================================ -->
<!-- 14. TECH STACK -->
<!-- ============================================================ -->
<section>
  <h2>14. Recommended Tech Stack</h2>
  <table>
    <thead>
      <tr><th>Layer</th><th>Technology</th><th>Rationale</th></tr>
    </thead>
    <tbody>
      <tr><td>LLM</td><td>AWS Bedrock — Claude 3.5 Sonnet</td><td>Best code generation quality; native AWS integration; no data leaves your VPC</td></tr>
      <tr><td>Backend API</td><td>Python FastAPI on ECS Fargate</td><td>Async-native, great for streaming Bedrock responses; type-safe with Pydantic</td></tr>
      <tr><td>Task Queue</td><td>Amazon SQS + Celery</td><td>Decouples generation/testing from API; FIFO for ordered SOP processing</td></tr>
      <tr><td>Frontend</td><td>React + Vite</td><td>Fast dev cycle; rich diff viewer components available (react-diff-viewer)</td></tr>
      <tr><td>Platform DB</td><td>Amazon RDS PostgreSQL</td><td>JSONB for structured SOPs; strong typing; mature ecosystem</td></tr>
      <tr><td>Sandbox DB</td><td>RDS Snapshot + Restore</td><td>Schema-identical replicas; disposable; automated provisioning</td></tr>
      <tr><td>Artifact Store</td><td>Amazon S3 + versioning</td><td>Immutable runbook versions; signed URLs for ServiceNow fetch</td></tr>
      <tr><td>Secrets</td><td>AWS Secrets Manager</td><td>Rotate DB creds without code changes; IAM-based access</td></tr>
      <tr><td>Execution</td><td>AWS Lambda</td><td>Per-ticket execution; scales to 1000 concurrent; pay-per-use</td></tr>
      <tr><td>Monitoring</td><td>CloudWatch + Grafana</td><td>Native AWS metrics; Grafana for dashboards your team already uses</td></tr>
      <tr><td>ServiceNow</td><td>Table API + Flow Designer</td><td>Standard ITSM integration; webhook triggers; scoped app isolation</td></tr>
      <tr><td>Auth</td><td>Company SSO (SAML/OIDC)</td><td>Single sign-on; RBAC via group claims</td></tr>
      <tr><td>IaC</td><td>Terraform / CDK</td><td>Reproducible infra; PR-based changes; drift detection</td></tr>
    </tbody>
  </table>
</section>

<!-- ============================================================ -->
<!-- 15. RISK MATRIX -->
<!-- ============================================================ -->
<section>
  <h2>15. Risk Matrix & Mitigations</h2>
  <table>
    <thead>
      <tr><th>Risk</th><th>Impact</th><th>Likelihood</th><th>Mitigation</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>LLM generates incorrect SQL logic</td>
        <td><span class="badge badge-red">High</span></td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td>4-gate testing pipeline; sample I/O validation; human approval before deploy</td>
      </tr>
      <tr>
        <td>CRM schema changes break deployed runbooks</td>
        <td><span class="badge badge-red">High</span></td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td>Schema drift detection; auto-disable on column mismatch; alert + re-generate</td>
      </tr>
      <tr>
        <td>Bedrock rate limits during bulk generation</td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td><span class="badge badge-green">Low</span></td>
        <td>Queue-based decoupling; exponential backoff; provisioned throughput</td>
      </tr>
      <tr>
        <td>Runbook causes data corruption in production</td>
        <td><span class="badge badge-red">Critical</span></td>
        <td><span class="badge badge-green">Low</span></td>
        <td>Transaction wrapping; idempotency guards; auto-rollback on error rate > 5%</td>
      </tr>
      <tr>
        <td>ServiceNow API changes break deployment</td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td><span class="badge badge-green">Low</span></td>
        <td>Version-pinned API calls; integration test suite; abstraction layer</td>
      </tr>
      <tr>
        <td>SOP ambiguity leads to wrong code</td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td><span class="badge badge-red">High</span></td>
        <td>Structured SOP form as alternative to free-text; LLM asks clarifying questions; sample I/O as ground truth</td>
      </tr>
      <tr>
        <td>Sandbox DB diverges from production schema</td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td><span class="badge badge-orange">Medium</span></td>
        <td>Nightly snapshot refresh; schema comparison on test start; fail-fast on mismatch</td>
      </tr>
    </tbody>
  </table>
</section>
<!-- ============================================================ -->
<!-- 16. FULL LIFECYCLE SEQUENCE -->
<!-- ============================================================ -->
<section>
  <h2>16. Full Lifecycle — End-to-End Sequence</h2>
  <p class="desc">
    The complete journey of an SOP from upload to automated ticket resolution,
    showing every system interaction.
  </p>
  <div class="mermaid">
sequenceDiagram
    participant Analyst as CRM Analyst
    participant Portal as Web Portal
    participant API as Platform API
    participant Parser as SOP Parser
    participant Bedrock as AWS Bedrock
    participant Sandbox as Sandbox DB
    participant Reviewer as Reviewer
    participant SNOW as ServiceNow
    participant Lambda as Lambda Worker
    participant CRM as CRM Database

    Analyst->>Portal: Upload SOP + sample I/O
    Portal->>API: POST /sop (multipart)
    API->>Parser: Parse document
    Parser->>Bedrock: Extract structure
    Bedrock-->>Parser: Structured SOP JSON
    Parser->>API: Schema-validated SOP
    API-->>Portal: SOP created ✓

    API->>API: Enqueue generation job
    API->>Bedrock: Generate runbook code<br/>(SOP + DB schema + template)
    Bedrock-->>API: Python runbook v1

    API->>API: Static analysis (AST + lint)
    API->>Sandbox: Seed test data
    API->>Sandbox: Execute runbook
    Sandbox-->>API: Output

    alt Output matches expected
        API->>API: Run integration tests<br/>(idempotency, rollback, edge cases)
        API-->>Portal: All tests passed ✓
        Portal->>Reviewer: Request approval
        Reviewer->>Portal: Approved ✓

        API->>SNOW: Create Automation Record
        SNOW-->>API: Record ID
        API->>SNOW: Register Flow Designer trigger
        API-->>Portal: Deployed ✓
    else Output mismatch
        API->>Bedrock: Fix code (diff as context)
        Note over API,Bedrock: Retry loop (max 5)
    end

    Note over SNOW,CRM: Later — ticket arrives

    SNOW->>Lambda: Trigger: matching ticket
    Lambda->>CRM: Execute runbook
    CRM-->>Lambda: Result
    Lambda->>SNOW: Update ticket + log
    Lambda->>API: Record execution metrics
  </div>
</section>

<!-- ============================================================ -->
<!-- 17. KEY METRICS -->
<!-- ============================================================ -->
<section>
  <h2>17. Success Metrics</h2>
  <div class="grid-3">
    <div class="card">
      <h3>📊 Automation Rate</h3>
      <p>% of grievance tickets resolved without human intervention. Target: 60% of repetitive ticket types within 6 months.</p>
    </div>
    <div class="card">
      <h3>⏱️ Resolution Time</h3>
      <p>Average time from ticket creation to resolution. Target: < 5 minutes for automated tickets (vs hours/days manual).</p>
    </div>
    <div class="card">
      <h3>✅ Accuracy Rate</h3>
      <p>% of automated resolutions that are correct (no re-open). Target: > 95% accuracy before scaling.</p>
    </div>
    <div class="card">
      <h3>🔄 Generation Success</h3>
      <p>% of SOPs that produce passing code within 5 LLM attempts. Target: > 80% first-pass success.</p>
    </div>
    <div class="card">
      <h3>💰 Cost per Automation</h3>
      <p>Bedrock API cost + compute cost per SOP onboarded. Track to ensure ROI vs manual resolution cost.</p>
    </div>
    <div class="card">
      <h3>🛡️ Safety Record</h3>
      <p>Zero data corruption incidents. Zero unauthorized data access. 100% audit trail coverage.</p>
    </div>
  </div>
</section>

</div>

<footer>
  Grievance Automation Platform — Architecture Plan
</footer>

<script>
  mermaid.initialize({
    startOnLoad: true,
    theme: 'default',
    themeVariables: {
      primaryColor: '#ddf4ff',
      primaryTextColor: '#1f2328',
      primaryBorderColor: '#0969da',
      lineColor: '#59636e',
      secondaryColor: '#dafbe1',
      tertiaryColor: '#f6f8fa',
      noteBkgColor: '#fff8c5',
      noteTextColor: '#1f2328',
      noteBorderColor: '#d4a72c',
      actorBkg: '#ddf4ff',
      actorTextColor: '#1f2328',
      actorBorder: '#0969da',
      signalColor: '#1f2328',
      labelBoxBkgColor: '#f6f8fa',
      labelBoxBorderColor: '#d1d9e0',
      labelTextColor: '#1f2328',
    },
    flowchart: { curve: 'basis', padding: 20 },
    sequence: { mirrorActors: false, messageMargin: 40 },
  });
</script>
</body>
</html>
