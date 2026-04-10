<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Claude Code — Architecture Deep Dive</title>
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
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
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
    }
    header h1 { font-size: 2.4rem; font-weight: 700; }
    header p { color: var(--muted); margin-top: .5rem; font-size: 1.1rem; }
</style>
  <style>
    .container { max-width: 1400px; margin: 0 auto; padding: 2rem 1.5rem; }
    section { margin-bottom: 3rem; }
    section h2 {
      font-size: 1.5rem;
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
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.5rem;
    }
    .card h3 { color: var(--accent2); font-size: 1.1rem; margin-bottom: .5rem; }
    .card p { color: var(--muted); font-size: .95rem; }
    .card ul { color: var(--muted); font-size: .95rem; padding-left: 1.2rem; }
    .card ul li { margin-bottom: .25rem; }
    .badge {
      display: inline-block;
      font-size: .75rem;
      padding: 2px 8px;
      border-radius: 999px;
      font-weight: 600;
      margin-right: .4rem;
    }
    .badge-blue { background: #ddf4ff; color: var(--accent); }
    .badge-green { background: #dafbe1; color: var(--accent2); }
    .badge-purple { background: #fbefff; color: var(--accent3); }
    .badge-orange { background: #fff1e5; color: var(--accent4); }
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
  <h1>Claude Code — Architecture Deep Dive</h1>
  <p>System design, scalability patterns, and engineering tricks of the trade</p>
</header>
<div class="container">
<!-- ============================================================ -->
<!-- 1. HIGH-LEVEL SYSTEM OVERVIEW -->
<!-- ============================================================ -->
<section>
  <h2>1. High-Level System Overview</h2>
  <p class="desc">
    The application is a CLI-first AI coding assistant built with Bun/TypeScript and Ink (React for terminals).
    It supports interactive REPL, headless SDK, and remote bridge modes — all sharing a single QueryEngine core.
  </p>
  <div class="mermaid">
graph TB
    subgraph Entrypoints["🚀 Entrypoints"]
        CLI["cli.tsx<br/>Bootstrap + Fast Paths"]
        SDK["SDK Entrypoint<br/>Headless / --print"]
        MCP_EP["MCP Entrypoint<br/>Server Mode"]
        BRIDGE_EP["Bridge Entrypoint<br/>Remote Control"]
        DAEMON["Daemon<br/>Long-running Supervisor"]
    end

    CLI -->|"dynamic import"| MAIN["main.tsx<br/>Commander CLI Parser<br/>4600+ lines"]
    SDK --> QE
    MCP_EP --> MCP_SRV["MCP Server"]

    MAIN -->|interactive| REPL["REPL Screen<br/>Ink TUI"]
    MAIN -->|"--print"| QE["QueryEngine<br/>Core Query Loop"]

    REPL --> QE
    BRIDGE_EP --> BRIDGE_MAIN["bridgeMain.ts<br/>Multi-Session Poll Loop"]

    subgraph Core["⚙️ Core Engine"]
        QE -->|"async generator"| QUERY["query.ts<br/>API Call + Tool Loop"]
        QUERY --> CLAUDE_API["Anthropic API<br/>Claude Models"]
        QUERY --> TOOLS["Tool System<br/>30+ Built-in Tools"]
        QUERY --> PERMS["Permission System<br/>allow / deny / ask"]
    end

    subgraph State["📦 State Management"]
        STORE["Zustand-like Store<br/>Immutable Updates"]
        APP_STATE["AppState<br/>Session + UI State"]
        BOOTSTRAP["Bootstrap State<br/>Global Singletons"]
    end

    subgraph Services["🔌 Services Layer"]
        MCP_CLIENT["MCP Clients<br/>stdio / SSE / HTTP / WS"]
        PLUGINS["Plugin System<br/>Versioned + Bundled"]
        SKILLS["Skills System<br/>Bundled + User"]
        ANALYTICS["Analytics<br/>GrowthBook + Telemetry"]
        POLICY["Policy Limits<br/>Enterprise Controls"]
    end

    QE --> STORE
    QE --> MCP_CLIENT
    QE --> PLUGINS
    QE --> SKILLS
    REPL --> APP_STATE

    style Entrypoints fill:#ddf4ff,stroke:#0969da,stroke-width:2px,color:#1f2328
    style Core fill:#dafbe1,stroke:#1a7f37,stroke-width:2px,color:#1f2328
    style State fill:#fbefff,stroke:#8250df,stroke-width:2px,color:#1f2328
    style Services fill:#fff1e5,stroke:#bc4c00,stroke-width:2px,color:#1f2328
  </div>
</section>
<!-- ============================================================ -->
<!-- 2. QUERY ENGINE & CONVERSATION LIFECYCLE -->
<!-- ============================================================ -->
<section>
  <h2>2. QueryEngine & Conversation Lifecycle</h2>
  <p class="desc">
    QueryEngine owns the full query lifecycle per conversation. Each submitMessage() call is an async generator
    that yields SDK messages. It manages tool execution, permission checks, transcript persistence, and usage tracking.
  </p>
  <div class="mermaid">
sequenceDiagram
    participant User
    participant QE as QueryEngine
    participant PUI as processUserInput
    participant API as Anthropic API
    participant Tool as Tool System
    participant Perm as Permission System
    participant FS as Session Storage

    User->>QE: submitMessage(prompt)
    QE->>PUI: processUserInput(input)
    PUI-->>QE: messages, shouldQuery, allowedTools

    QE->>FS: recordTranscript(messages)
    Note over QE: yield system_init message

    loop Query Loop (max turns)
        QE->>API: query(messages, systemPrompt, tools)
        API-->>QE: stream assistant response

        alt Tool Use Requested
            QE->>Perm: canUseTool(tool, input)
            alt Permission Granted
                Perm-->>QE: allow
                QE->>Tool: tool.call(args, context)
                Tool-->>QE: ToolResult + newMessages
                QE->>FS: recordTranscript(updated)
                Note over QE: yield tool_result
            else Permission Denied
                Perm-->>QE: deny
                Note over QE: Track denial, yield rejection
            end
        else Text Response (end_turn)
            Note over QE: yield result{success}
        end

        QE->>QE: Track usage, update state
    end

    QE-->>User: yield final result
  </div>
</section>
<!-- ============================================================ -->
<!-- 3. BRIDGE / REMOTE CONTROL — MULTI-SESSION SCALABILITY -->
<!-- ============================================================ -->
<section>
  <h2>3. Bridge / Remote Control — Multi-Session Scalability</h2>
  <p class="desc">
    The bridge system enables remote control of Claude Code sessions. It supports multiple concurrent sessions
    per environment with configurable spawn modes (single-session, worktree isolation, same-dir).
    Scalability is achieved through poll-based work distribution, heartbeat liveness, and capacity-wake signaling.
  </p>
  <div class="mermaid">
graph TB
    subgraph WebUI["🌐 claude.ai / Web Client"]
        USER_A["User A"]
        USER_B["User B"]
        USER_C["User C"]
    end

    subgraph Server["☁️ Backend API"]
        WORK_QUEUE["Work Queue<br/>(Redis PEL)"]
        SESSION_INGRESS["Session Ingress<br/>WebSocket + HTTP"]
        ENV_API["Environments API<br/>Register / Poll / Ack"]
    end

    subgraph Bridge["🖥️ Bridge Process (bridgeMain.ts)"]
        POLL_LOOP["Poll Loop<br/>Exponential Backoff"]
        CAP_WAKE["Capacity Wake<br/>Signal Primitive"]
        HB["Heartbeat Loop<br/>JWT Liveness"]
        TOKEN_REFRESH["Token Refresh<br/>Scheduler"]

        subgraph Sessions["Active Sessions (max N)"]
            S1["Session 1<br/>Child Process"]
            S2["Session 2<br/>Child Process"]
            S3["Session 3<br/>Child Process"]
        end

        subgraph SpawnModes["Spawn Modes"]
            SM1["single-session<br/>1:1 lifecycle"]
            SM2["worktree<br/>Git worktree isolation"]
            SM3["same-dir<br/>Shared CWD"]
        end
    end

    USER_A -->|"create session"| WORK_QUEUE
    USER_B -->|"create session"| WORK_QUEUE
    USER_C -->|"create session"| WORK_QUEUE

    POLL_LOOP -->|"pollForWork()"| ENV_API
    ENV_API -->|"WorkResponse"| POLL_LOOP
    POLL_LOOP -->|"spawn child"| Sessions
    HB -->|"heartbeatWork()"| ENV_API
    TOKEN_REFRESH -->|"reconnectSession()"| ENV_API

    S1 <-->|"NDJSON stdio"| SESSION_INGRESS
    S2 <-->|"NDJSON stdio"| SESSION_INGRESS
    S3 <-->|"NDJSON stdio"| SESSION_INGRESS

    Sessions -->|"session done"| CAP_WAKE
    CAP_WAKE -->|"wake signal"| POLL_LOOP

    style WebUI fill:#ddf4ff,stroke:#0969da
    style Server fill:#ffebe9,stroke:#cf222e
    style Bridge fill:#dafbe1,stroke:#1a7f37
    style Sessions fill:#ddf4ff,stroke:#0969da
    style SpawnModes fill:#fff1e5,stroke:#bc4c00
  </div>
</section>
<!-- ============================================================ -->
<!-- 4. TRANSPORT LAYER — HYBRID READ/WRITE ARCHITECTURE -->
<!-- ============================================================ -->
<section>
  <h2>4. Transport Layer — Hybrid Read/Write Architecture</h2>
  <p class="desc">
    The transport layer uses a split-protocol design: WebSocket for low-latency reads, HTTP POST for reliable writes.
    The SerialBatchEventUploader serializes all writes through a single queue with backpressure, retry, and batching.
    SSE transport adds sequence-number-based resumption for CCR v2.
  </p>
  <div class="mermaid">
graph LR
    subgraph Client["Claude Code Process"]
        WRITE["write(msg)"]
        BATCH["writeBatch(msgs)"]
        STREAM_BUF["Stream Event Buffer<br/>100ms delay"]

        subgraph Uploader["SerialBatchEventUploader"]
            QUEUE["Pending Queue<br/>maxQueueSize: 100K"]
            DRAIN["Drain Loop<br/>Serial, 1 POST in-flight"]
            RETRY["Retry Logic<br/>Exp. Backoff + Jitter"]
            BP["Backpressure<br/>enqueue() blocks"]
        end
    end

    subgraph Transports["Transport Variants"]
        HT["HybridTransport<br/>WS reads + POST writes"]
        SSE["SSETransport<br/>SSE reads + POST writes"]
        WS["WebSocketTransport<br/>WS bidirectional"]
    end

    subgraph Server["Session Ingress"]
        WS_EP["WebSocket Endpoint<br/>/ws/{session_id}"]
        SSE_EP["SSE Endpoint<br/>/events/stream"]
        POST_EP["POST Endpoint<br/>/events"]
    end

    WRITE --> STREAM_BUF
    STREAM_BUF -->|"flush timer"| QUEUE
    WRITE -->|"non-stream"| QUEUE
    BATCH --> QUEUE
    QUEUE --> DRAIN
    DRAIN -->|"success"| BP
    DRAIN -->|"failure"| RETRY
    RETRY -->|"re-queue front"| QUEUE

    HT -->|"reads"| WS_EP
    HT -->|"writes"| POST_EP
    SSE -->|"reads + Last-Event-ID"| SSE_EP
    SSE -->|"writes"| POST_EP
    WS <-->|"bidirectional"| WS_EP

    style Client fill:#dafbe1,stroke:#1a7f37
    style Uploader fill:#ddf4ff,stroke:#0969da
    style Transports fill:#fbefff,stroke:#8250df
    style Server fill:#fff1e5,stroke:#bc4c00
  </div>
</section>
<!-- ============================================================ -->
<!-- 5. TOOL SYSTEM ARCHITECTURE -->
<!-- ============================================================ -->
<section>
  <h2>5. Tool System Architecture</h2>
  <p class="desc">
    Tools are the primary way Claude interacts with the user's environment. Each tool implements a strict interface
    with permission checks, input validation, concurrency safety flags, and structured result rendering.
    The buildTool() factory provides fail-closed defaults.
  </p>
  <div class="mermaid">
graph TB
    subgraph ToolInterface["🔧 Tool Interface (Tool.ts)"]
        SCHEMA["inputSchema<br/>Zod validation"]
        CALL["call()<br/>Execute tool"]
        PERMS["checkPermissions()<br/>Tool-specific rules"]
        VALIDATE["validateInput()<br/>Pre-execution check"]
        DESC["description()<br/>Dynamic prompt"]
        RENDER["renderToolUseMessage()<br/>UI rendering"]
        FLAGS["Flags: isReadOnly, isDestructive,<br/>isConcurrencySafe, shouldDefer"]
    end

    subgraph BuiltinTools["Built-in Tools (30+)"]
        direction LR
        FS_TOOLS["File Tools<br/>Read / Write / Edit"]
        BASH["BashTool<br/>Shell execution"]
        SEARCH["Search Tools<br/>Glob / Grep"]
        WEB["Web Tools<br/>Fetch / Search"]
        AGENT["AgentTool<br/>Sub-agent spawning"]
        TASK_TOOLS["Task Tools<br/>Create / List / Stop"]
        MCP_TOOL["MCPTool<br/>Dynamic MCP proxy"]
        LSP_TOOL["LSPTool<br/>Language Server"]
    end

    subgraph PermissionFlow["Permission Flow"]
        AUTO["Auto Mode<br/>Classifier-based"]
        DEFAULT["Default Mode<br/>Ask user"]
        BYPASS["Bypass Mode<br/>Allow all"]
        PLAN["Plan Mode<br/>Read-only"]
        HOOKS["Pre/Post Tool Hooks<br/>Custom gates"]
    end

    subgraph Concurrency["Concurrency Model"]
        SAFE["Concurrency Safe<br/>Read, Glob, Grep"]
        UNSAFE["Not Safe<br/>Write, Edit, Bash"]
        POOL["Tool Pool<br/>Parallel safe tools"]
    end

    CALL --> VALIDATE
    VALIDATE --> PERMS
    PERMS --> PermissionFlow
    PermissionFlow -->|"allowed"| CALL
    CALL --> RENDER

    BuiltinTools --> ToolInterface
    FLAGS --> Concurrency

    style ToolInterface fill:#dafbe1,stroke:#1a7f37
    style BuiltinTools fill:#ddf4ff,stroke:#0969da
    style PermissionFlow fill:#ffebe9,stroke:#cf222e
    style Concurrency fill:#fff1e5,stroke:#bc4c00
  </div>
</section>
<!-- ============================================================ -->
<!-- 6. TASK SYSTEM — BACKGROUND WORK MANAGEMENT -->
<!-- ============================================================ -->
<section>
  <h2>6. Task System — Background Work Management</h2>
  <p class="desc">
    Tasks represent background work units (shell commands, sub-agents, remote agents, workflows).
    Each task type has its own lifecycle, output capture, and cleanup logic. Tasks are tracked in AppState
    and can be foregrounded, backgrounded, or killed.
  </p>
  <div class="mermaid">
stateDiagram-v2
    [*] --> pending: generateTaskId()
    pending --> running: spawn / start
    running --> completed: exit 0
    running --> failed: exit non-zero
    running --> killed: user kill / timeout

    completed --> [*]
    failed --> [*]
    killed --> [*]

    state running {
        [*] --> foreground
        foreground --> background: user backgrounds
        background --> foreground: user foregrounds
    }

    note right of pending
        Task Types:
        • local_bash — Shell commands
        • local_agent — Sub-agent processes
        • remote_agent — Remote CCR agents
        • in_process_teammate — In-process swarm
        • local_workflow — Multi-step workflows
        • monitor_mcp — MCP server monitors
        • dream — Background analysis
    end note
  </div>
</section>

<!-- ============================================================ -->
<!-- 7. SESSION & STATE MANAGEMENT -->
<!-- ============================================================ -->
<section>
  <h2>7. Session & State Management</h2>
  <p class="desc">
    State is managed through a minimal Zustand-like store with immutable updates and listener subscriptions.
    Session persistence uses NDJSON transcript files with lazy JSON serialization and write queuing.
    Bootstrap state holds process-wide singletons (session ID, CWD, model, flags).
  </p>
  <div class="mermaid">
graph TB
    subgraph Store["Store (store.ts)"]
        GET["getState()"]
        SET["setState(updater)"]
        SUB["subscribe(listener)"]
        ONCHANGE["onChange callback"]
    end

    subgraph AppState["AppState Shape"]
        TOOL_PERM["toolPermissionContext<br/>mode, rules, directories"]
        FAST_MODE["fastMode<br/>speed vs quality"]
        FILE_HIST["fileHistory<br/>snapshot tracking"]
        ATTRIBUTION["attribution<br/>commit tracking"]
        TASKS_STATE["tasks<br/>Map&lt;id, TaskState&gt;"]
        PLUGINS_STATE["plugins<br/>enabled, errors"]
    end

    subgraph Bootstrap["Bootstrap State (singletons)"]
        SESSION_ID["sessionId"]
        CWD_STATE["cwd"]
        MODEL["mainLoopModel"]
        CLIENT_TYPE["clientType"]
        SDK_BETAS["sdkBetas"]
        FLAGS["isInteractive, isKairosActive,<br/>sessionPersistenceDisabled"]
    end

    subgraph Persistence["Session Persistence"]
        TRANSCRIPT["NDJSON Transcript<br/>~/.claude/sessions/"]
        WRITE_QUEUE["Write Queue<br/>100ms lazy stringify"]
        FLUSH["flushSessionStorage()<br/>Eager flush for cowork"]
    end

    SET --> ONCHANGE
    ONCHANGE --> SUB
    Store --> AppState
    AppState --> Persistence
    TRANSCRIPT --> WRITE_QUEUE

    style Store fill:#fbefff,stroke:#8250df
    style AppState fill:#dafbe1,stroke:#1a7f37
    style Bootstrap fill:#ddf4ff,stroke:#0969da
    style Persistence fill:#fff1e5,stroke:#bc4c00
  </div>
</section>
<!-- ============================================================ -->
<!-- 8. MCP & PLUGIN EXTENSIBILITY -->
<!-- ============================================================ -->
<section>
  <h2>8. MCP & Plugin Extensibility</h2>
  <p class="desc">
    The Model Context Protocol (MCP) system supports multiple transport types and scoped configurations.
    Plugins are versioned, cache-managed, and can provide tools, commands, and resources.
    Both systems support hot-reload via file change detectors.
  </p>
  <div class="mermaid">
graph TB
    subgraph MCPConfig["MCP Configuration Scopes"]
        LOCAL["local<br/>.claude/mcp.json"]
        USER_CFG["user<br/>~/.claude/mcp.json"]
        PROJECT["project<br/>CLAUDE.md refs"]
        ENTERPRISE["enterprise<br/>MDM / policy"]
        CLAUDEAI["claude.ai<br/>proxy servers"]
        MANAGED["managed<br/>remote settings"]
    end

    subgraph MCPTransports["MCP Transports"]
        STDIO["stdio<br/>Subprocess"]
        SSE_MCP["sse<br/>Server-Sent Events"]
        HTTP_MCP["http<br/>Streamable HTTP"]
        WS_MCP["ws<br/>WebSocket"]
        SDK_MCP["sdk<br/>In-process"]
        IDE_MCP["sse-ide / ws-ide<br/>IDE Extensions"]
    end

    subgraph MCPLifecycle["Server Lifecycle"]
        PENDING_S["pending"]
        CONNECTED_S["connected"]
        FAILED_S["failed"]
        NEEDS_AUTH["needs-auth<br/>OAuth / XAA"]
        DISABLED_S["disabled"]
    end

    subgraph Plugins["Plugin System"]
        BUNDLED["Bundled Plugins<br/>Built-in"]
        VERSIONED["Versioned Plugins<br/>Cache-managed"]
        MANAGED_P["Managed Plugins<br/>Enterprise-pushed"]
        CACHE["Plugin Cache<br/>Orphan cleanup"]
    end

    MCPConfig -->|"merge precedence"| MCPTransports
    MCPTransports --> MCPLifecycle
    CONNECTED_S -->|"provides"| TOOLS_MCP["Tools + Commands + Resources"]

    Plugins -->|"provides"| TOOLS_MCP

    style MCPConfig fill:#ddf4ff,stroke:#0969da
    style MCPTransports fill:#fbefff,stroke:#8250df
    style MCPLifecycle fill:#dafbe1,stroke:#1a7f37
    style Plugins fill:#fff1e5,stroke:#bc4c00
  </div>
</section>

<!-- ============================================================ -->
<!-- 9. AUTHENTICATION & SECURITY -->
<!-- ============================================================ -->
<section>
  <h2>9. Authentication & Security</h2>
  <p class="desc">
    Multi-layered auth: OAuth tokens for claude.ai, API keys for direct access, JWT for session ingress,
    trusted device tokens for bridge environments. Sandbox mode restricts file system and network access.
    Policy limits enforce enterprise controls.
  </p>
  <div class="mermaid">
graph TB
    subgraph Auth["Authentication Layers"]
        OAUTH["OAuth 2.0<br/>claude.ai subscription"]
        API_KEY["API Key<br/>Direct Anthropic API"]
        JWT["JWT Tokens<br/>Session Ingress Auth"]
        TRUSTED["Trusted Device<br/>Bridge registration"]
        AWS_AUTH["AWS Bedrock<br/>IAM credentials"]
        GCP_AUTH["GCP Vertex<br/>Service account"]
    end

    subgraph Security["Security Controls"]
        SANDBOX["Sandbox Manager<br/>File + Network restrictions"]
        PERM_MODE["Permission Modes<br/>default / auto / bypass / plan"]
        POLICY["Policy Limits<br/>Enterprise MDM"]
        TRUST["Trust Dialog<br/>First-run acceptance"]
        DENIAL["Denial Tracking<br/>Fallback to prompting"]
    end

    subgraph TokenMgmt["Token Management"]
        KEYCHAIN["macOS Keychain<br/>Prefetch at startup"]
        REFRESH["Token Refresh<br/>5min before expiry"]
        INGRESS["Session Ingress Token<br/>Per-session JWT"]
        WORK_SECRET["Work Secret<br/>Base64url JSON"]
    end

    Auth --> Security
    Auth --> TokenMgmt
    JWT --> REFRESH
    OAUTH --> KEYCHAIN
    TRUSTED --> WORK_SECRET

    style Auth fill:#ffebe9,stroke:#cf222e
    style Security fill:#dafbe1,stroke:#1a7f37
    style TokenMgmt fill:#ddf4ff,stroke:#0969da
  </div>
</section>
<!-- ============================================================ -->
<!-- 10. STARTUP OPTIMIZATION & PERFORMANCE TRICKS -->
<!-- ============================================================ -->
<section>
  <h2>10. Startup Optimization & Performance Tricks</h2>
  <p class="desc">
    The codebase employs aggressive startup optimization: parallel prefetching, deferred imports,
    dead code elimination via feature flags, and a profiling checkpoint system.
    The goal is sub-200ms time-to-first-render.
  </p>
  <div class="mermaid">
graph LR
    subgraph Phase1["Phase 1: Entry (0ms)"]
        PROFILE["profileCheckpoint<br/>Mark entry"]
        MDM["startMdmRawRead<br/>Parallel subprocess"]
        KEYCHAIN_PF["startKeychainPrefetch<br/>Parallel keychain reads"]
    end

    subgraph Phase2["Phase 2: Fast Paths"]
        VERSION["--version<br/>Zero imports, instant"]
        BRIDGE_FP["remote-control<br/>Minimal imports"]
        DAEMON_FP["daemon<br/>Lean worker"]
        BG_FP["ps/logs/attach/kill<br/>Session management"]
    end

    subgraph Phase3["Phase 3: Full CLI"]
        EARLY_INPUT["Capture early input"]
        LAUNCH_SCREEN["Launch screen animation"]
        MAIN_IMPORT["Import main.tsx<br/>~135ms module eval"]
        INIT["init()<br/>Configs + Auth"]
    end

    subgraph Phase4["Phase 4: Deferred"]
        USER_INIT["initUser()"]
        SYS_CTX["getSystemContext()"]
        TIPS["getRelevantTips()"]
        FILE_COUNT["countFilesRoundedRg()"]
        MODEL_CAP["refreshModelCapabilities()"]
        CHANGE_DET["Settings/Skill detectors"]
    end

    Phase1 -->|"parallel"| Phase2
    Phase2 -->|"no match"| Phase3
    Phase3 -->|"after first render"| Phase4

    style Phase1 fill:#ffebe9,stroke:#cf222e
    style Phase2 fill:#ddf4ff,stroke:#0969da
    style Phase3 fill:#dafbe1,stroke:#1a7f37
    style Phase4 fill:#fff1e5,stroke:#bc4c00
  </div>
</section>

<!-- ============================================================ -->
<!-- 11. COMMAND SYSTEM -->
<!-- ============================================================ -->
<section>
  <h2>11. Command System — Slash Commands & Subcommands</h2>
  <p class="desc">
    80+ slash commands organized in individual directories. Each command exports a registration function
    with metadata (name, description, aliases). Commands can be local (client-side) or trigger API queries.
    The system supports plugin-provided commands and migration of commands to plugins.
  </p>
  <div class="mermaid">
graph TB
    subgraph CommandCategories["Command Categories"]
        direction LR
        SESSION_CMD["Session<br/>/resume, /session,<br/>/clear, /compact"]
        CONFIG_CMD["Config<br/>/config, /model,<br/>/permissions, /theme"]
        DEV_CMD["Development<br/>/commit, /review,<br/>/branch, /diff"]
        TOOL_CMD["Tools<br/>/mcp, /plugin,<br/>/skills, /agents"]
        NAV_CMD["Navigation<br/>/files, /context,<br/>/memory, /help"]
        REMOTE_CMD["Remote<br/>/bridge, /teleport,<br/>/share, /export"]
    end

    subgraph CommandFlow["Command Processing"]
        PARSE["parseSlashCommand()"]
        MATCH["Match command name"]
        EXEC["Execute handler"]
        LOCAL["Local result<br/>(no API call)"]
        QUERY_CMD["Trigger query<br/>(API call)"]
    end

    CommandCategories --> PARSE
    PARSE --> MATCH
    MATCH --> EXEC
    EXEC --> LOCAL
    EXEC --> QUERY_CMD

    style CommandCategories fill:#ddf4ff,stroke:#0969da
    style CommandFlow fill:#dafbe1,stroke:#1a7f37
  </div>
</section>
<!-- ============================================================ -->
<!-- 12. SCALABILITY & MULTI-USER PATTERNS -->
<!-- ============================================================ -->
<section>
  <h2>12. Scalability & Multi-User Patterns</h2>
  <div class="grid">
    <div class="card">
      <h3><span class="badge badge-blue">Bridge</span> Multi-Session Polling</h3>
      <p>The bridge poll loop supports N concurrent sessions per environment. GrowthBook-gated
         <code>tengu_ccr_bridge_multi_session</code> controls rollout. Poll intervals are
         server-configurable via <code>tengu_bridge_poll_interval_config</code> with separate
         rates for idle, partial-capacity, and at-capacity states.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-green">Transport</span> Capacity Wake</h3>
      <p>When at capacity, the bridge sleeps but can be woken instantly via <code>CapacityWake</code> —
         a shared abort-controller primitive. When a session completes, it fires <code>wake()</code>,
         aborting the sleep so the poll loop immediately checks for new work. No wasted polling cycles.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-purple">Heartbeat</span> Non-Exclusive Liveness</h3>
      <p>Heartbeats run alongside polling (not instead of). JWT-authenticated heartbeats extend work leases
         without hitting the DB-backed poll path. On JWT expiry, <code>reconnectSession()</code> re-queues
         work server-side so the next poll delivers fresh credentials.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-orange">Isolation</span> Git Worktree Mode</h3>
      <p>Each session can get its own git worktree — full filesystem isolation without cloning.
         Worktrees are created at spawn and cleaned up on session completion. Prevents concurrent
         sessions from stomping each other's file changes.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-blue">Writes</span> Serial Batch Uploader</h3>
      <p>All writes go through <code>SerialBatchEventUploader</code> — at most 1 POST in-flight.
         Events batch during in-flight requests. Exponential backoff with jitter on failure.
         Backpressure via blocking <code>enqueue()</code> at 100K queue depth. Prevents Firestore
         write collisions that caused retry storms.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-green">Reads</span> SSE Sequence Resumption</h3>
      <p>SSE transport tracks <code>lastSequenceNum</code> and sends <code>Last-Event-ID</code>
         on reconnect. Server resumes from that point — no full history replay. Duplicate detection
         via <code>seenSequenceNums</code> set with automatic pruning at 1000 entries.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-purple">State</span> Immutable Store</h3>
      <p>Zustand-like store with <code>Object.is()</code> equality check — no-op on identity-equal updates.
         Listeners fire synchronously on change. <code>DeepImmutable&lt;T&gt;</code> type wrapper prevents
         accidental mutation of permission contexts and tool rules.</p>
    </div>
    <div class="card">
      <h3><span class="badge badge-orange">Startup</span> Deferred Prefetches</h3>
      <p>Heavy prefetches (user init, system context, git status, file counting, model capabilities)
         are deferred until after first render. In <code>--bare</code> mode, ALL prefetches are skipped.
         Keychain reads and MDM subprocess reads start in parallel before any imports.</p>
    </div>
  </div>
</section>
<!-- ============================================================ -->
<!-- 13. TRICKS OF THE TRADE -->
<!-- ============================================================ -->
<section>
  <h2>13. Tricks of the Trade</h2>
  <div class="grid">
    <div class="card">
      <h3>🔥 Dead Code Elimination</h3>
      <p><code>feature('FLAG')</code> from <code>bun:bundle</code> enables build-time DCE.
         Entire modules (coordinator, assistant, ablation) are tree-shaken from external builds.
         Conditional <code>require()</code> inside feature gates ensures zero runtime cost.</p>
    </div>
    <div class="card">
      <h3>🧠 Prompt Cache Preservation</h3>
      <p>Settings paths use content-hash-based temp files instead of random UUIDs.
         This prevents busting the Anthropic API prompt cache — identical settings produce
         the same path across process boundaries, avoiding a 12x input token cost penalty.</p>
    </div>
    <div class="card">
      <h3>⚡ Lazy Module Loading</h3>
      <p>Heavy modules (React components, MessageSelector, coordinator) use lazy <code>require()</code>
         to avoid circular dependencies and defer evaluation. The CLI entrypoint uses dynamic
         <code>import()</code> for every fast-path to minimize module evaluation.</p>
    </div>
    <div class="card">
      <h3>🔄 FlushGate Pattern</h3>
      <p>During initial history flush, new messages queue via <code>FlushGate</code> to prevent
         interleaving with historical messages. State machine: <code>start() → enqueue() → end()</code>.
         Supports transport replacement without dropping queued items.</p>
    </div>
    <div class="card">
      <h3>📊 Ring Buffer Patterns</h3>
      <p>Activities, stderr lines, and error logs use fixed-size ring buffers (shift on overflow).
         In-memory error log uses a 100-entry ring with reference-based watermarks instead of
         index-based (which break when the buffer shifts during a turn).</p>
    </div>
    <div class="card">
      <h3>🔐 Fail-Closed Defaults</h3>
      <p><code>buildTool()</code> provides safe defaults: <code>isConcurrencySafe → false</code>,
         <code>isReadOnly → false</code>, <code>isDestructive → false</code>.
         Tools must explicitly opt into dangerous capabilities. Permission system denies by default.</p>
    </div>
    <div class="card">
      <h3>🌊 Stream Event Batching</h3>
      <p>High-frequency <code>stream_event</code> messages accumulate in a 100ms delay buffer
         before being enqueued. Non-stream writes flush the buffer first to preserve ordering.
         Reduces POST count dramatically during content streaming.</p>
    </div>
    <div class="card">
      <h3>🏗️ Content-Hash Dedup</h3>
      <p>Nested memory attachments (CLAUDE.md) track loaded paths in a <code>Set&lt;string&gt;</code>
         separate from the LRU file cache. The LRU evicts entries in busy sessions, causing
         re-injection — the Set provides stable dedup across the session lifetime.</p>
    </div>
    <div class="card">
      <h3>🔌 GrowthBook Feature Flags</h3>
      <p>Runtime feature gates via GrowthBook with 5-minute refresh. Poll intervals, spawn modes,
         transport selection, and model capabilities are all server-configurable.
         Blocking gate checks for critical paths, cached checks for hot paths.</p>
    </div>
    <div class="card">
      <h3>📝 Fire-and-Forget Transcripts</h3>
      <p>Assistant message transcripts use fire-and-forget writes (not awaited) because
         <code>claude.ts</code> yields one message per content block then mutates usage on
         <code>message_delta</code>. The write queue's 100ms lazy stringify captures the mutation.
         User messages are awaited for resumability.</p>
    </div>
    <div class="card">
      <h3>🧩 Snip Compaction</h3>
      <p>Long conversations use snip-boundary compaction — feature-gated via <code>HISTORY_SNIP</code>.
         The QueryEngine truncates in-place for SDK (no UI), while the REPL projects a snipped view
         on demand (preserving full history for scrollback).</p>
    </div>
    <div class="card">
      <h3>🔀 Abort Controller Composition</h3>
      <p>Multiple abort signals are merged via <code>combinedAbortSignal</code> and
         <code>CapacityWake</code>. Cleanup functions remove listeners to prevent memory leaks.
         The pattern: create merged controller, listen on both sources, return cleanup.</p>
    </div>
  </div>
</section>
<!-- ============================================================ -->
<!-- 14. DATA FLOW — END TO END -->
<!-- ============================================================ -->
<section>
  <h2>14. End-to-End Data Flow</h2>
  <p class="desc">
    Complete flow from user input through the system, showing how a remote session processes
    a message through the bridge, transport, query engine, and back.
  </p>
  <div class="mermaid">
sequenceDiagram
    participant Web as Web Client
    participant SI as Session Ingress
    participant Bridge as Bridge Process
    participant Child as Child CLI Process
    participant QE as QueryEngine
    participant API as Claude API
    participant Tool as Tool (e.g. BashTool)
    participant FS as File System

    Web->>SI: User sends message
    SI->>Bridge: WebSocket frame
    Bridge->>Child: stdin NDJSON

    Child->>QE: submitMessage(prompt)
    QE->>QE: processUserInput()
    QE->>FS: recordTranscript()

    QE->>API: POST /messages (streaming)
    API-->>QE: content_block_start
    API-->>QE: content_block_delta (text)
    QE-->>Child: yield assistant message
    Child-->>Bridge: stdout NDJSON
    Bridge-->>SI: HTTP POST /events (batched)
    SI-->>Web: WebSocket push

    API-->>QE: content_block_start (tool_use)
    QE->>QE: checkPermissions()
    QE->>Tool: tool.call(args)
    Tool->>FS: Execute operation
    FS-->>Tool: Result
    Tool-->>QE: ToolResult

    QE->>API: POST /messages (tool_result)
    API-->>QE: Final text response
    QE-->>Child: yield result
    Child-->>Bridge: stdout NDJSON
    Bridge-->>SI: HTTP POST /events
    SI-->>Web: WebSocket push
  </div>
</section>

</div>

<footer>
  Architecture analysis generated from source code — Claude Code codebase
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
