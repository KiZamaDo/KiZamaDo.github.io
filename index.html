<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System Design Interview - Comprehensive Architecture Diagrams</title>
    <script src="https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.min.js"></script>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            background: #0a0a0f;
            color: #e0e0e0;
            line-height: 1.6;
        }
        .hero {
            text-align: center;
            padding: 60px 20px 40px;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            border-bottom: 2px solid #302b63;
        }
        .hero h1 {
            font-size: 2.8rem;
            background: linear-gradient(90deg, #00d2ff, #7b2ff7, #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        .hero p { color: #aaa; font-size: 1.1rem; }
        nav {
            display: flex;
            justify-content: center;
            gap: 12px;
            padding: 20px;
            background: #111118;
            border-bottom: 1px solid #222;
            flex-wrap: wrap;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        nav a {
            padding: 10px 22px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s;
            border: 1px solid transparent;
        }
        nav a:nth-child(1) { background: #1a1a2e; color: #e50914; border-color: #e50914; }
        nav a:nth-child(2) { background: #1a1a2e; color: #00c853; border-color: #00c853; }
        nav a:nth-child(3) { background: #1a1a2e; color: #25d366; border-color: #25d366; }
        nav a:nth-child(4) { background: #1a1a2e; color: #4285f4; border-color: #4285f4; }
        nav a:nth-child(5) { background: #1a1a2e; color: #e1306c; border-color: #e1306c; }
        nav a:hover { transform: translateY(-2px); box-shadow: 0 4px 15px rgba(255,255,255,0.1); }
        .platform-section {
            max-width: 1400px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .platform-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #222;
        }
        .platform-header .icon { font-size: 2.5rem; }
        .platform-header h2 { font-size: 2rem; }
        .platform-header .subtitle { color: #888; font-size: 0.95rem; margin-top: 4px; }
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }
        .info-card {
            background: #14141f;
            border: 1px solid #252535;
            border-radius: 12px;
            padding: 18px;
            text-align: center;
        }
        .info-card .label { color: #888; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 1px; }
        .info-card .value { font-size: 1.3rem; font-weight: 700; margin-top: 5px; }
        .diagram-container {
            background: #ffffff;
            border-radius: 16px;
            padding: 30px;
            margin-bottom: 25px;
            overflow-x: auto;
            border: 1px solid #333;
        }
        .diagram-container h3 {
            color: #333;
            margin-bottom: 20px;
            font-size: 1.2rem;
            text-align: center;
            padding-bottom: 10px;
            border-bottom: 2px solid #eee;
        }
        .key-points {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            margin-top: 25px;
        }
        .key-point {
            background: #14141f;
            border-left: 3px solid #7b2ff7;
            padding: 15px 20px;
            border-radius: 0 10px 10px 0;
        }
        .key-point h4 { color: #7b2ff7; margin-bottom: 5px; font-size: 0.95rem; }
        .key-point p { color: #aaa; font-size: 0.88rem; }
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
            margin-bottom: 30px;
        }
        .tech-tag {
            padding: 5px 14px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        footer {
            text-align: center;
            padding: 40px 20px;
            color: #555;
            border-top: 1px solid #222;
            margin-top: 60px;
        }
        /* Color themes per platform */
        .netflix .platform-header h2 { color: #e50914; }
        .netflix .info-card .value { color: #e50914; }
        .netflix .key-point { border-left-color: #e50914; }
        .netflix .key-point h4 { color: #e50914; }
        .netflix .tech-tag { background: #2d0a0a; color: #e50914; }

        .jiohotstar .platform-header h2 { color: #00c853; }
        .jiohotstar .info-card .value { color: #00c853; }
        .jiohotstar .key-point { border-left-color: #00c853; }
        .jiohotstar .key-point h4 { color: #00c853; }
        .jiohotstar .tech-tag { background: #0a2d14; color: #00c853; }

        .whatsapp .platform-header h2 { color: #25d366; }
        .whatsapp .info-card .value { color: #25d366; }
        .whatsapp .key-point { border-left-color: #25d366; }
        .whatsapp .key-point h4 { color: #25d366; }
        .whatsapp .tech-tag { background: #0a2d1a; color: #25d366; }

        .google .platform-header h2 { color: #4285f4; }
        .google .info-card .value { color: #4285f4; }
        .google .key-point { border-left-color: #4285f4; }
        .google .key-point h4 { color: #4285f4; }
        .google .tech-tag { background: #0a1a2d; color: #4285f4; }

        .instagram .platform-header h2 { color: #e1306c; }
        .instagram .info-card .value { color: #e1306c; }
        .instagram .key-point { border-left-color: #e1306c; }
        .instagram .key-point h4 { color: #e1306c; }
        .instagram .tech-tag { background: #2d0a1a; color: #e1306c; }

        /* Easy Explanation Blocks */
        .easy-explanation {
            background: linear-gradient(135deg, #14141f 0%, #1a1a30 100%);
            border: 1px solid #2a2a4a;
            border-radius: 16px;
            padding: 35px 30px;
            margin-top: 35px;
            position: relative;
            overflow: hidden;
        }
        .easy-explanation::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 3px;
            background: linear-gradient(90deg, #7b2ff7, #00d2ff, #ff6b6b);
        }
        .easy-explanation h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .easy-explanation h3 .emoji { font-size: 1.5rem; }
        .easy-explanation .analogy {
            background: #1e1e35;
            border-left: 4px solid #7b2ff7;
            padding: 18px 22px;
            border-radius: 0 12px 12px 0;
            margin: 20px 0;
            font-style: italic;
            color: #ccc;
            line-height: 1.8;
        }
        .easy-explanation .analogy strong { color: #a78bfa; font-style: normal; }
        .easy-explanation .step-flow {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        .easy-explanation .step {
            background: #1a1a2e;
            border-radius: 12px;
            padding: 18px;
            position: relative;
        }
        .easy-explanation .step .step-num {
            display: inline-block;
            width: 28px;
            height: 28px;
            border-radius: 50%;
            text-align: center;
            line-height: 28px;
            font-weight: 700;
            font-size: 0.85rem;
            margin-bottom: 8px;
        }
        .easy-explanation .step h4 {
            font-size: 0.95rem;
            margin-bottom: 6px;
        }
        .easy-explanation .step p {
            color: #aaa;
            font-size: 0.88rem;
            line-height: 1.6;
        }
        .easy-explanation .summary-text {
            color: #bbb;
            font-size: 0.95rem;
            line-height: 1.8;
            margin-top: 10px;
        }
        .easy-explanation .summary-text strong { color: #e0e0e0; }
        .easy-explanation .interview-tip {
            background: #1a2a1a;
            border: 1px solid #2a4a2a;
            border-radius: 12px;
            padding: 18px 22px;
            margin-top: 20px;
        }
        .easy-explanation .interview-tip h4 {
            color: #4caf50;
            font-size: 0.9rem;
            margin-bottom: 8px;
        }
        .easy-explanation .interview-tip p {
            color: #aaa;
            font-size: 0.88rem;
            line-height: 1.7;
        }

        .netflix .easy-explanation h3 { color: #e50914; }
        .netflix .easy-explanation .step .step-num { background: #e50914; color: #fff; }
        .netflix .easy-explanation .step h4 { color: #e50914; }
        .netflix .easy-explanation .analogy { border-left-color: #e50914; }
        .netflix .easy-explanation .analogy strong { color: #ff6b6b; }

        .jiohotstar .easy-explanation h3 { color: #00c853; }
        .jiohotstar .easy-explanation .step .step-num { background: #00c853; color: #fff; }
        .jiohotstar .easy-explanation .step h4 { color: #00c853; }
        .jiohotstar .easy-explanation .analogy { border-left-color: #00c853; }
        .jiohotstar .easy-explanation .analogy strong { color: #69f0ae; }

        .whatsapp .easy-explanation h3 { color: #25d366; }
        .whatsapp .easy-explanation .step .step-num { background: #25d366; color: #fff; }
        .whatsapp .easy-explanation .step h4 { color: #25d366; }
        .whatsapp .easy-explanation .analogy { border-left-color: #25d366; }
        .whatsapp .easy-explanation .analogy strong { color: #69f0ae; }

        .google .easy-explanation h3 { color: #4285f4; }
        .google .easy-explanation .step .step-num { background: #4285f4; color: #fff; }
        .google .easy-explanation .step h4 { color: #4285f4; }
        .google .easy-explanation .analogy { border-left-color: #4285f4; }
        .google .easy-explanation .analogy strong { color: #82b1ff; }

        .instagram .easy-explanation h3 { color: #e1306c; }
        .instagram .easy-explanation .step .step-num { background: #e1306c; color: #fff; }
        .instagram .easy-explanation .step h4 { color: #e1306c; }
        .instagram .easy-explanation .analogy { border-left-color: #e1306c; }
        .instagram .easy-explanation .analogy strong { color: #f48fb1; }
    </style>
</head>
<body>

<div class="hero">
    <h1>System Design Interview Cheat Sheet</h1>
    <p>Comprehensive architecture diagrams for Netflix, JioHotstar, WhatsApp, Google Search &amp; Instagram</p>
</div>

<nav>
    <a href="#netflix">Netflix</a>
    <a href="#jiohotstar">JioHotstar</a>
    <a href="#whatsapp">WhatsApp</a>
    <a href="#google">Google Search</a>
    <a href="#instagram">Instagram</a>
</nav>

<!-- ==================== NETFLIX ==================== -->
<section id="netflix" class="platform-section netflix">
    <div class="platform-header">
        <span class="icon">🎬</span>
        <div>
            <h2>Netflix - Video Streaming Platform</h2>
            <div class="subtitle">Global streaming service with 260M+ subscribers across 190+ countries</div>
        </div>
    </div>

    <div class="info-grid">
        <div class="info-card"><div class="label">Subscribers</div><div class="value">260M+</div></div>
        <div class="info-card"><div class="label">Daily Viewing Hours</div><div class="value">500M+</div></div>
        <div class="info-card"><div class="label">Countries</div><div class="value">190+</div></div>
        <div class="info-card"><div class="label">Internet Traffic</div><div class="value">~15% Global</div></div>
    </div>

    <div class="diagram-container">
        <h3>High-Level Architecture - Netflix Streaming Platform</h3>
        <pre class="mermaid">
graph TB
    subgraph Clients["📱 Client Layer"]
        TV["Smart TV App"]
        Mobile["Mobile App<br/>iOS / Android"]
        Web["Web Browser"]
        Console["Gaming Console"]
    end

    subgraph EdgeLayer["🌐 Edge / CDN Layer - Open Connect"]
        DNS["DNS + GSLB<br/>Global Server Load Balancing"]
        OCA1["OCA Server<br/>Region: US-East"]
        OCA2["OCA Server<br/>Region: EU-West"]
        OCA3["OCA Server<br/>Region: Asia-Pacific"]
        ISP1["ISP Embedded<br/>OCA Appliances"]
    end

    subgraph APIGateway["🚪 API Gateway Layer"]
        Zuul["Zuul Gateway<br/>Dynamic Routing, Auth,<br/>Rate Limiting, Canary"]
    end

    subgraph BackendServices["⚙️ Backend Microservices - AWS"]
        direction TB
        subgraph CoreServices["Core Services"]
            UserSvc["User Service<br/>Profiles, Preferences"]
            AuthSvc["Auth Service<br/>OAuth2, SSO, MFA"]
            SubSvc["Subscription Service<br/>Plans, Billing"]
            PlaybackSvc["Playback Service<br/>Stream URLs, DRM Tokens"]
        end
        subgraph ContentServices["Content Services"]
            CatalogSvc["Catalog Service<br/>Titles, Metadata"]
            SearchSvc["Search Service<br/>Elasticsearch"]
            RecSvc["Recommendation Engine<br/>ML Models, Collaborative Filtering"]
            ABTest["A/B Testing<br/>Feature Flags"]
        end
        subgraph MediaPipeline["Media Processing Pipeline"]
            Ingest["Content Ingestion<br/>Mezzanine Files"]
            Transcode["Transcoding Service<br/>100+ Profiles per Title"]
            QC["Quality Control<br/>Automated Checks"]
            Encrypt["DRM Encryption<br/>Widevine, FairPlay, PlayReady"]
        end
    end

    subgraph DataLayer["💾 Data Layer"]
        CassDB[("Cassandra<br/>User Data, Viewing History")]
        MySQL[("MySQL<br/>Billing, Subscriptions")]
        EVCache["EVCache<br/>Session, Metadata Cache"]
        S3[("S3<br/>Video Assets, Artwork")]
        Kafka["Apache Kafka<br/>Event Streaming"]
        Spark["Apache Spark<br/>Analytics, ML Training"]
    end

    Clients -->|"HTTPS"| DNS
    DNS -->|"Route to nearest"| OCA1 & OCA2 & OCA3
    DNS --> ISP1
    Clients -->|"API Calls"| Zuul
    Zuul --> CoreServices
    Zuul --> ContentServices
    PlaybackSvc -->|"Manifest + DRM Token"| Clients
    OCA1 & OCA2 & OCA3 -->|"Video Chunks<br/>Adaptive Bitrate"| Clients
    ISP1 -->|"Video Chunks"| Clients
    Ingest --> Transcode --> QC --> Encrypt
    Encrypt -->|"Push encoded files"| S3
    S3 -->|"Proactive Cache Fill"| OCA1 & OCA2 & OCA3 & ISP1
    CoreServices --> CassDB & MySQL & EVCache
    ContentServices --> CassDB & EVCache
    RecSvc --> Spark
    CoreServices --> Kafka
    Kafka --> Spark

    style Clients fill:#1a1a2e,stroke:#e50914,color:#fff
    style EdgeLayer fill:#fff5f5,stroke:#e50914,color:#333
    style APIGateway fill:#fff0f0,stroke:#e50914,color:#333
    style BackendServices fill:#f8f8ff,stroke:#555,color:#333
    style DataLayer fill:#f0f0ff,stroke:#555,color:#333
    style CoreServices fill:#fff,stroke:#999,color:#333
    style ContentServices fill:#fff,stroke:#999,color:#333
    style MediaPipeline fill:#fff8f0,stroke:#e88,color:#333
        </pre>
    </div>

    <div class="diagram-container">
        <h3>Netflix - Video Playback Flow (Sequence Diagram)</h3>
        <pre class="mermaid">
sequenceDiagram
    participant C as Client App
    participant Z as Zuul API Gateway
    participant PS as Playback Service
    participant RS as Recommendation Svc
    participant DRM as DRM Service
    participant CDN as Open Connect CDN
    participant S3 as S3 Storage

    C->>Z: GET /api/browse (auth token)
    Z->>RS: Fetch personalized catalog
    RS-->>Z: Ranked title list
    Z-->>C: Homepage with recommendations

    C->>Z: POST /api/play/{titleId}
    Z->>PS: Request stream session
    PS->>PS: Check entitlement & region
    PS->>DRM: Generate DRM license token
    DRM-->>PS: Encrypted license
    PS->>PS: Select optimal CDN node
    PS-->>Z: Manifest URL + DRM token
    Z-->>C: Stream manifest + license

    C->>CDN: Request video chunks (adaptive bitrate)
    CDN->>CDN: Cache HIT?
    alt Cache Hit
        CDN-->>C: Serve video chunk
    else Cache Miss
        CDN->>S3: Fetch from origin
        S3-->>CDN: Video chunk
        CDN->>CDN: Cache locally
        CDN-->>C: Serve video chunk
    end

    loop Every 30 seconds
        C->>Z: Report playback health & bandwidth
        Z->>PS: Update session metrics
        PS-->>Z: Adjust bitrate recommendation
        Z-->>C: Switch to optimal quality
    end
        </pre>
    </div>

    <div class="tech-stack">
        <span class="tech-tag">Java</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Node.js</span>
        <span class="tech-tag">Cassandra</span>
        <span class="tech-tag">MySQL</span>
        <span class="tech-tag">EVCache</span>
        <span class="tech-tag">Kafka</span>
        <span class="tech-tag">Spark</span>
        <span class="tech-tag">AWS</span>
        <span class="tech-tag">Open Connect CDN</span>
        <span class="tech-tag">Zuul</span>
        <span class="tech-tag">Eureka</span>
    </div>

    <div class="key-points">
        <div class="key-point">
            <h4>Open Connect CDN</h4>
            <p>Netflix's custom CDN with OCA (Open Connect Appliances) deployed inside ISP networks. Serves ~95% of traffic from edge, reducing latency and backbone costs.</p>
        </div>
        <div class="key-point">
            <h4>Adaptive Bitrate Streaming</h4>
            <p>Each title is encoded into 100+ quality profiles. The client dynamically switches between bitrates based on real-time bandwidth measurements.</p>
        </div>
        <div class="key-point">
            <h4>Microservices on AWS</h4>
            <p>700+ microservices handle all non-streaming logic (auth, recommendations, billing). Zuul gateway handles routing, canary deployments, and rate limiting.</p>
        </div>
        <div class="key-point">
            <h4>Recommendation Engine</h4>
            <p>ML-based collaborative filtering and content-based models personalize the entire UI. A/B testing runs thousands of experiments simultaneously.</p>
        </div>
    </div>

    <!-- EASY EXPLANATION -->
    <div class="easy-explanation">
        <h3><span class="emoji">🧠</span> Explain It Like I'm 5: How Netflix Works</h3>

        <div class="analogy">
            Imagine a <strong>giant pizza delivery chain</strong>. The main kitchen (AWS) prepares all the recipes and knows what you like. But instead of delivering from one central kitchen, they've placed <strong>mini kitchens inside your neighborhood</strong> (Open Connect CDN inside ISPs). So when you order a pizza (press play), it comes from right around the corner — super fast!
        </div>

        <p class="summary-text">Here's how the whole system works, step by step:</p>

        <div class="step-flow">
            <div class="step">
                <span class="step-num">1</span>
                <h4>You Open Netflix</h4>
                <p>Your app talks to the <strong>API Gateway (Zuul)</strong> — think of it as the front desk. It checks who you are, what plan you have, and sends you to the right place.</p>
            </div>
            <div class="step">
                <span class="step-num">2</span>
                <h4>Your Homepage Loads</h4>
                <p>The <strong>Recommendation Engine</strong> (powered by machine learning) looks at what you've watched before and picks shows you'll probably like. That's why your Netflix looks different from your friend's!</p>
            </div>
            <div class="step">
                <span class="step-num">3</span>
                <h4>You Press Play</h4>
                <p>The <strong>Playback Service</strong> checks if you're allowed to watch (subscription check), gets a <strong>DRM token</strong> (a digital key so the video can't be pirated), and finds the <strong>closest CDN server</strong> to you.</p>
            </div>
            <div class="step">
                <span class="step-num">4</span>
                <h4>Video Streams to You</h4>
                <p>The video isn't sent as one big file. It's broken into <strong>tiny chunks (a few seconds each)</strong>. Your device downloads them one by one from the nearest <strong>OCA server</strong> (Netflix's mini-server near your ISP).</p>
            </div>
            <div class="step">
                <span class="step-num">5</span>
                <h4>Quality Adjusts Automatically</h4>
                <p>If your internet slows down, Netflix instantly switches to a <strong>lower quality chunk</strong>. When it speeds up, you get HD/4K again. This is called <strong>Adaptive Bitrate Streaming</strong> — you barely notice it happening.</p>
            </div>
            <div class="step">
                <span class="step-num">6</span>
                <h4>Behind the Scenes</h4>
                <p>Every movie is pre-encoded into <strong>100+ quality versions</strong>. These are pushed to CDN servers worldwide <strong>before</strong> anyone even watches. So when you press play, the video is already waiting nearby.</p>
            </div>
        </div>

        <div class="interview-tip">
            <h4>💡 Interview Tip</h4>
            <p>When discussing Netflix, always mention the <strong>separation of control plane (AWS) and data plane (Open Connect CDN)</strong>. API calls go to AWS, but actual video bytes come from edge servers inside ISPs. This is the key insight interviewers look for — it shows you understand that streaming video and serving APIs are fundamentally different problems.</p>
        </div>
    </div>
</section>

<!-- ==================== JIOHOTSTAR ==================== -->
<section id="jiohotstar" class="platform-section jiohotstar">
    <div class="platform-header">
        <span class="icon">🏏</span>
        <div>
            <h2>JioHotstar - Live Streaming &amp; OTT Platform</h2>
            <div class="subtitle">India's largest streaming platform, handling 59M+ concurrent streams during live cricket events</div>
        </div>
    </div>

    <div class="info-grid">
        <div class="info-card"><div class="label">Peak Concurrent</div><div class="value">59M+</div></div>
        <div class="info-card"><div class="label">Monthly Active Users</div><div class="value">300M+</div></div>
        <div class="info-card"><div class="label">Content Library</div><div class="value">100K+ Hours</div></div>
        <div class="info-card"><div class="label">Languages</div><div class="value">17+</div></div>
    </div>

    <div class="diagram-container">
        <h3>High-Level Architecture - JioHotstar Streaming Platform</h3>
        <pre class="mermaid">
graph TB
    subgraph Clients["📱 Client Layer"]
        MobileApp["Mobile App<br/>iOS / Android"]
        WebApp["Web App<br/>React SPA"]
        SmartTV["Smart TV / STB<br/>Fire TV, Jio STB"]
    end

    subgraph EdgeCDN["🌐 Multi-CDN &amp; Edge Layer"]
        GSLB["Global Server Load Balancer<br/>DNS-based Routing"]
        CDN1["Akamai CDN"]
        CDN2["Jio CDN<br/>ISP-level Edge"]
        CDN3["CloudFront CDN"]
        OriginShield["Origin Shield<br/>Cache Aggregation"]
    end

    subgraph Gateway["🚪 API Gateway / BFF"]
        APIGW["API Gateway<br/>Kong / Custom"]
        BFF["Backend for Frontend<br/>Device-specific APIs"]
        RateLimit["Rate Limiter<br/>Token Bucket"]
        AuthGW["Auth Middleware<br/>JWT Validation"]
    end

    subgraph K8sCluster["☸️ Kubernetes Cluster - Microservices"]
        direction TB
        subgraph UserServices["User Domain"]
            UserSvc["User Service"]
            AuthSvc["Auth &amp; Identity<br/>OTP, SSO, Jio ID"]
            SubSvc["Subscription &amp; Billing<br/>Freemium, Premium"]
        end
        subgraph ContentDomain["Content Domain"]
            CatalogSvc["Catalog Service<br/>Metadata, Seasons"]
            SearchSvc["Search Service<br/>Elasticsearch"]
            RecEngine["Recommendation Engine<br/>Personalization ML"]
            AdSvc["Ad Service<br/>SSAI, CSAI<br/>Programmatic Ads"]
        end
        subgraph StreamDomain["Streaming Domain"]
            LiveSvc["Live Stream Service<br/>Low-Latency HLS/DASH"]
            VODSvc["VOD Service<br/>On-Demand Playback"]
            DRMSvc["DRM Service<br/>Widevine, FairPlay"]
            ABRCtrl["ABR Controller<br/>Adaptive Bitrate Logic"]
        end
        subgraph MediaPipeline["Media Processing"]
            LiveIngest["Live Ingest<br/>RTMP / SRT Input"]
            Transcoder["Transcoding Farm<br/>FFmpeg, GPU-accelerated"]
            Packager["Packager<br/>HLS + DASH Manifests"]
            AdInsertion["Server-Side Ad Insertion<br/>SSAI Stitching"]
        end
    end

    subgraph DataStores["💾 Data Layer"]
        Redis["Redis Cluster<br/>Session, Hot Cache"]
        Cassandra[("Cassandra<br/>User Activity, Watch History")]
        PostgreSQL[("PostgreSQL<br/>Catalog, Subscriptions")]
        S3Store[("Object Storage<br/>S3 / Jio Cloud")]
        Kafka["Kafka<br/>Event Bus"]
        ClickHouse[("ClickHouse<br/>Real-time Analytics")]
    end

    Clients -->|"HTTPS"| GSLB
    GSLB -->|"Video Streams"| CDN1 & CDN2 & CDN3
    CDN1 & CDN2 & CDN3 --> OriginShield
    OriginShield --> S3Store
    Clients -->|"API Calls"| APIGW
    APIGW --> AuthGW --> RateLimit --> BFF
    BFF --> UserServices & ContentDomain & StreamDomain
    LiveIngest --> Transcoder --> Packager --> AdInsertion
    AdInsertion --> S3Store
    LiveSvc --> LiveIngest
    UserServices --> Redis & Cassandra & PostgreSQL
    ContentDomain --> PostgreSQL & Redis
    StreamDomain --> Redis & DRMSvc
    K8sCluster --> Kafka --> ClickHouse

    style Clients fill:#1a2e1a,stroke:#00c853,color:#fff
    style EdgeCDN fill:#f0fff0,stroke:#00c853,color:#333
    style Gateway fill:#f0fff5,stroke:#00c853,color:#333
    style K8sCluster fill:#f8fff8,stroke:#555,color:#333
    style DataStores fill:#f0f8f0,stroke:#555,color:#333
        </pre>
    </div>

    <div class="diagram-container">
        <h3>JioHotstar - Live Cricket Match Streaming Flow</h3>
        <pre class="mermaid">
sequenceDiagram
    participant Cam as 🎥 Stadium Feed
    participant Ingest as Live Ingest Server
    participant Trans as Transcoding Farm
    participant Pack as Packager + SSAI
    participant Origin as Origin Storage
    participant CDN as Multi-CDN
    participant Client as 📱 Client App
    participant Analytics as Analytics Pipeline

    Cam->>Ingest: RTMP/SRT live feed
    Ingest->>Trans: Raw video frames
    Trans->>Trans: Encode multiple bitrates<br/>(240p to 4K, 10+ profiles)
    Trans->>Pack: Encoded segments (2-6s chunks)
    Pack->>Pack: Generate HLS/DASH manifests
    Pack->>Pack: Stitch personalized ads (SSAI)
    Pack->>Origin: Upload chunks + manifests
    Origin->>CDN: Push to edge (proactive cache)

    Client->>CDN: Request manifest
    CDN-->>Client: Return manifest with chunk URLs
    loop Every 2-6 seconds
        Client->>CDN: GET next video chunk
        CDN-->>Client: Serve chunk (cache hit)
        Client->>Client: Decode &amp; render
        Client->>Analytics: Playback telemetry
    end

    Note over Client,CDN: ABR: Client monitors bandwidth<br/>and switches quality dynamically

    Analytics->>Analytics: Real-time aggregation<br/>59M concurrent tracking
        </pre>
    </div>

    <div class="tech-stack">
        <span class="tech-tag">Golang</span>
        <span class="tech-tag">Java</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Kubernetes</span>
        <span class="tech-tag">Kafka</span>
        <span class="tech-tag">Redis</span>
        <span class="tech-tag">Cassandra</span>
        <span class="tech-tag">PostgreSQL</span>
        <span class="tech-tag">Elasticsearch</span>
        <span class="tech-tag">FFmpeg</span>
        <span class="tech-tag">Multi-CDN</span>
        <span class="tech-tag">ClickHouse</span>
    </div>

    <div class="key-points">
        <div class="key-point">
            <h4>Multi-CDN Strategy</h4>
            <p>Uses Akamai, CloudFront, and Jio's own ISP-level CDN simultaneously. Traffic is dynamically routed based on real-time performance metrics and regional load.</p>
        </div>
        <div class="key-point">
            <h4>Project Hulk - 59M Concurrent</h4>
            <p>Redesigned architecture to handle 59M concurrent streams during Cricket World Cup 2023. Pre-provisioned capacity, load-tested at 1.5x peak, and used circuit breakers extensively.</p>
        </div>
        <div class="key-point">
            <h4>Server-Side Ad Insertion (SSAI)</h4>
            <p>Ads are stitched into the video stream server-side, making them immune to ad blockers and providing a seamless viewing experience with no buffering during ad transitions.</p>
        </div>
        <div class="key-point">
            <h4>Low-Latency Live Streaming</h4>
            <p>Uses chunked transfer encoding with 2-6 second segments and low-latency HLS/DASH to keep live stream delay under 10 seconds for cricket matches.</p>
        </div>
    </div>

    <!-- EASY EXPLANATION -->
    <div class="easy-explanation">
        <h3><span class="emoji">🧠</span> Explain It Like I'm 5: How JioHotstar Works</h3>

        <div class="analogy">
            Imagine <strong>59 million people</strong> all trying to watch the same cricket match at the same time. That's like the entire population of Italy watching one TV channel — but over the internet! JioHotstar handles this by being like a <strong>water supply system</strong>: instead of one giant pipe from one reservoir, they have <strong>multiple reservoirs (CDNs) and thousands of local taps (edge servers)</strong> spread across the country.
        </div>

        <p class="summary-text">Here's the journey of a live cricket ball, from stadium to your phone:</p>

        <div class="step-flow">
            <div class="step">
                <span class="step-num">1</span>
                <h4>Camera Captures the Action</h4>
                <p>Cameras at the stadium send a <strong>raw video feed</strong> (via RTMP/SRT protocol) to JioHotstar's <strong>Live Ingest Servers</strong>. Think of this as the raw, unprocessed footage — very high quality, very large.</p>
            </div>
            <div class="step">
                <span class="step-num">2</span>
                <h4>Transcoding (Making Copies)</h4>
                <p>The <strong>Transcoding Farm</strong> (GPU-powered machines running FFmpeg) converts this one feed into <strong>10+ different quality levels</strong> — from 240p for slow 2G connections to 4K for fiber users. Each quality is cut into <strong>2-6 second chunks</strong>.</p>
            </div>
            <div class="step">
                <span class="step-num">3</span>
                <h4>Ads Get Stitched In (SSAI)</h4>
                <p>Before the chunks are stored, <strong>personalized ads are stitched directly into the video stream</strong> on the server side. This means ad blockers can't skip them, and there's no buffering when ads play — it feels like part of the stream.</p>
            </div>
            <div class="step">
                <span class="step-num">4</span>
                <h4>Multi-CDN Delivery</h4>
                <p>The chunks are pushed to <strong>three CDNs simultaneously</strong> — Akamai, CloudFront, and Jio's own CDN. A smart load balancer picks the <strong>fastest CDN for your location</strong>. If one CDN is overloaded, traffic shifts to another automatically.</p>
            </div>
            <div class="step">
                <span class="step-num">5</span>
                <h4>Your Phone Plays It</h4>
                <p>Your app downloads a <strong>manifest file</strong> (a playlist of chunk URLs), then fetches chunks one by one. If your network slows down, it <strong>automatically switches to a lower quality</strong> — this is Adaptive Bitrate (ABR).</p>
            </div>
            <div class="step">
                <span class="step-num">6</span>
                <h4>Real-Time Monitoring</h4>
                <p>Every single playback session sends <strong>telemetry data</strong> (buffer health, bitrate, errors) to a <strong>ClickHouse analytics pipeline</strong>. Engineers watch dashboards tracking 59M streams in real-time during a match.</p>
            </div>
        </div>

        <div class="interview-tip">
            <h4>💡 Interview Tip</h4>
            <p>The killer talking point for JioHotstar is <strong>Multi-CDN failover</strong>. Explain that relying on a single CDN is a single point of failure. By using 3 CDNs with real-time health checks and DNS-based routing, they can handle CDN outages gracefully. Also mention <strong>pre-provisioning</strong> — they load-test at 1.5x expected peak before every major cricket event.</p>
        </div>
    </div>
</section>

<!-- ==================== WHATSAPP ==================== -->
<section id="whatsapp" class="platform-section whatsapp">
    <div class="platform-header">
        <span class="icon">💬</span>
        <div>
            <h2>WhatsApp - Real-Time Messaging Platform</h2>
            <div class="subtitle">World's largest messaging app with 2.5B+ users, 100B+ messages/day, built on Erlang</div>
        </div>
    </div>

    <div class="info-grid">
        <div class="info-card"><div class="label">Active Users</div><div class="value">2.5B+</div></div>
        <div class="info-card"><div class="label">Messages / Day</div><div class="value">100B+</div></div>
        <div class="info-card"><div class="label">Peak MPS</div><div class="value">~115K</div></div>
        <div class="info-card"><div class="label">Encryption</div><div class="value">E2E Default</div></div>
    </div>

    <div class="diagram-container">
        <h3>High-Level Architecture - WhatsApp Messaging System</h3>
        <pre class="mermaid">
graph TB
    subgraph Clients["📱 Client Layer"]
        iOS["iOS App"]
        Android["Android App"]
        WebClient["WhatsApp Web<br/>Linked Device"]
        Desktop["Desktop App"]
    end

    subgraph EdgeLayer["🌐 Edge &amp; Connection Layer"]
        LB["Load Balancer<br/>L4/L7, Geo-aware"]
        ConnGW1["Connection Gateway<br/>WebSocket Server 1"]
        ConnGW2["Connection Gateway<br/>WebSocket Server 2"]
        ConnGWN["Connection Gateway<br/>WebSocket Server N"]
    end

    subgraph CoreServices["⚙️ Core Services (Erlang/Elixir)"]
        direction TB
        subgraph Messaging["Messaging Engine"]
            MsgRouter["Message Router<br/>Route to recipient's server"]
            MsgQueue["Offline Message Queue<br/>Store &amp; Forward"]
            GroupSvc["Group Service<br/>Fan-out to members"]
            E2E["E2E Encryption<br/>Signal Protocol"]
        end
        subgraph Presence["Presence &amp; Status"]
            PresenceSvc["Presence Service<br/>Online/Offline/Typing"]
            LastSeen["Last Seen Tracker"]
            StatusSvc["Status/Stories Service<br/>24hr Ephemeral"]
        end
        subgraph Media["Media Pipeline"]
            MediaUpload["Media Upload Service<br/>Image, Video, Audio, Docs"]
            MediaProcess["Media Processing<br/>Compression, Thumbnails"]
            MediaStore["Media Storage<br/>Encrypted Blobs"]
        end
        subgraph Calls["Voice &amp; Video"]
            SignalSvc["Signaling Service<br/>Call Setup/Teardown"]
            TURN["TURN/STUN Servers<br/>NAT Traversal"]
            SFU["SFU<br/>Group Video Calls"]
        end
    end

    subgraph DataLayer["💾 Data Layer"]
        Mnesia["Mnesia<br/>Erlang Native DB<br/>Session, Routing Tables"]
        HBase[("HBase / Cassandra<br/>Message Store<br/>Offline Queue")]
        BlobStore[("Blob Storage<br/>Encrypted Media Files")]
        Redis2["Redis<br/>Presence Cache<br/>Rate Limiting"]
        Kafka2["Kafka<br/>Event Stream<br/>Analytics"]
    end

    subgraph PushLayer["📲 Push Notification"]
        PushSvc["Push Service"]
        APNS["APNs<br/>iOS Push"]
        FCM["FCM<br/>Android Push"]
    end

    Clients <-->|"Persistent WebSocket<br/>+ Noise Protocol"| LB
    LB <--> ConnGW1 & ConnGW2 & ConnGWN
    ConnGW1 & ConnGW2 & ConnGWN <--> MsgRouter
    MsgRouter --> E2E
    MsgRouter <--> MsgQueue
    MsgRouter --> GroupSvc
    GroupSvc -->|"Fan-out"| MsgRouter
    ConnGW1 & ConnGW2 & ConnGWN <--> PresenceSvc
    PresenceSvc --> LastSeen
    Clients --> MediaUpload
    MediaUpload --> MediaProcess --> MediaStore
    MediaStore --> BlobStore
    SignalSvc <--> ConnGW1 & ConnGW2 & ConnGWN
    SignalSvc --> TURN
    SignalSvc --> SFU
    MsgRouter --> Mnesia & HBase
    PresenceSvc --> Redis2
    MsgQueue --> PushSvc
    PushSvc --> APNS & FCM
    CoreServices --> Kafka2

    style Clients fill:#0a2d1a,stroke:#25d366,color:#fff
    style EdgeLayer fill:#f0fff5,stroke:#25d366,color:#333
    style CoreServices fill:#f8fff8,stroke:#555,color:#333
    style DataLayer fill:#f0f8f0,stroke:#555,color:#333
    style PushLayer fill:#f5fff5,stroke:#25d366,color:#333
        </pre>
    </div>

    <div class="diagram-container">
        <h3>WhatsApp - Message Delivery Flow (1:1 Chat)</h3>
        <pre class="mermaid">
sequenceDiagram
    participant A as 👤 Sender (Alice)
    participant GW1 as Connection Gateway<br/>(Alice's Server)
    participant Router as Message Router
    participant DB as Message Store<br/>(HBase)
    participant GW2 as Connection Gateway<br/>(Bob's Server)
    participant B as 👤 Receiver (Bob)
    participant Push as Push Service

    Note over A,B: End-to-End Encryption: Messages encrypted on device using Signal Protocol

    A->>GW1: Send encrypted message<br/>(via WebSocket)
    GW1->>Router: Route message to Bob
    Router->>Router: Lookup Bob's connection server
    Router->>DB: Persist to offline queue

    alt Bob is ONLINE
        Router->>GW2: Forward to Bob's gateway
        GW2->>B: Deliver via WebSocket
        B-->>GW2: ACK (delivered ✓✓)
        GW2-->>Router: Delivery confirmed
        Router->>DB: Remove from offline queue
        Router-->>GW1: Delivery receipt
        GW1-->>A: Show ✓✓ (delivered)
    else Bob is OFFLINE
        Router->>Push: Trigger push notification
        Push->>B: Push notification (FCM/APNs)
        Note over B: Bob comes online later
        B->>GW2: Connect + sync
        GW2->>Router: Request pending messages
        Router->>DB: Fetch offline queue
        DB-->>Router: Queued messages
        Router->>GW2: Deliver batch
        GW2->>B: Deliver all pending messages
        B-->>GW2: ACK all
        GW2-->>Router: Delivery confirmed
        Router->>DB: Clear offline queue
    end

    B->>GW2: Read receipt (blue ✓✓)
    GW2->>Router: Forward read receipt
    Router->>GW1: Relay to Alice
    GW1->>A: Show blue ✓✓ (read)
        </pre>
    </div>

    <div class="diagram-container">
        <h3>WhatsApp - Group Message Fan-Out</h3>
        <pre class="mermaid">
graph LR
    Sender["👤 Sender"] -->|"Encrypted msg"| GW["Connection<br/>Gateway"]
    GW --> Router["Message<br/>Router"]
    Router --> GroupSvc["Group Service<br/>Lookup members"]
    GroupSvc --> FanOut{"Fan-Out<br/>to N members"}
    FanOut -->|"Member 1"| R1["Router → GW → 👤"]
    FanOut -->|"Member 2"| R2["Router → GW → 👤"]
    FanOut -->|"Member 3"| R3["Router → GW → 👤"]
    FanOut -->|"Member N<br/>(offline)"| Queue["Offline Queue<br/>+ Push Notification"]

    style Sender fill:#25d366,stroke:#333,color:#fff
    style FanOut fill:#fff3cd,stroke:#856404,color:#333
    style Queue fill:#f8d7da,stroke:#721c24,color:#333
        </pre>
    </div>

    <div class="tech-stack">
        <span class="tech-tag">Erlang/OTP</span>
        <span class="tech-tag">Elixir</span>
        <span class="tech-tag">Mnesia</span>
        <span class="tech-tag">HBase</span>
        <span class="tech-tag">Cassandra</span>
        <span class="tech-tag">Redis</span>
        <span class="tech-tag">Kafka</span>
        <span class="tech-tag">Signal Protocol</span>
        <span class="tech-tag">WebSocket</span>
        <span class="tech-tag">TURN/STUN</span>
        <span class="tech-tag">FreeBSD</span>
    </div>

    <div class="key-points">
        <div class="key-point">
            <h4>Erlang for Concurrency</h4>
            <p>WhatsApp famously used Erlang/OTP to handle millions of concurrent connections per server. Erlang's lightweight processes and fault-tolerance model are ideal for messaging workloads.</p>
        </div>
        <div class="key-point">
            <h4>End-to-End Encryption</h4>
            <p>All messages use the Signal Protocol. Keys are exchanged between devices; the server never has access to plaintext. Even media files are encrypted before upload.</p>
        </div>
        <div class="key-point">
            <h4>Store &amp; Forward</h4>
            <p>Messages for offline users are persisted in an offline queue (HBase). When the user reconnects, all pending messages are delivered in order and then purged from the server.</p>
        </div>
        <div class="key-point">
            <h4>Presence &amp; Delivery Receipts</h4>
            <p>Single tick (sent), double tick (delivered), blue tick (read). Presence is tracked via persistent WebSocket connections with heartbeat pings.</p>
        </div>
    </div>

    <!-- EASY EXPLANATION -->
    <div class="easy-explanation">
        <h3><span class="emoji">🧠</span> Explain It Like I'm 5: How WhatsApp Works</h3>

        <div class="analogy">
            Think of WhatsApp like a <strong>post office that never sleeps</strong>. When you send a letter (message), the post office (server) figures out which mailbox (connection gateway) your friend is connected to and delivers it instantly. If your friend isn't home (offline), the post office <strong>holds the letter in a locker</strong> (offline queue) and delivers it the moment they come back. The twist? Every letter is in a <strong>sealed envelope that only you and your friend can open</strong> — even the post office can't read it (end-to-end encryption).
        </div>

        <p class="summary-text">Here's what happens when you send "Hi" to a friend:</p>

        <div class="step-flow">
            <div class="step">
                <span class="step-num">1</span>
                <h4>You Type and Hit Send</h4>
                <p>Your phone <strong>encrypts the message</strong> using the Signal Protocol before it even leaves your device. The server will never see the actual text — only scrambled data that only your friend's phone can decode.</p>
            </div>
            <div class="step">
                <span class="step-num">2</span>
                <h4>Always-On Connection</h4>
                <p>Your phone maintains a <strong>persistent WebSocket connection</strong> to a Connection Gateway server. Think of it as an always-open phone line. This is why messages arrive instantly — there's no need to "dial" each time.</p>
            </div>
            <div class="step">
                <span class="step-num">3</span>
                <h4>Message Router Finds Your Friend</h4>
                <p>The <strong>Message Router</strong> looks up which Connection Gateway server your friend is connected to (using Mnesia, Erlang's built-in database). It's like looking up which post office branch handles their area.</p>
            </div>
            <div class="step">
                <span class="step-num">4</span>
                <h4>Delivery (Online vs Offline)</h4>
                <p><strong>If online:</strong> The message is forwarded through the gateway to their phone instantly. You see ✓✓ (delivered). <strong>If offline:</strong> The message is saved in an <strong>offline queue</strong> (HBase), and a push notification is sent via APNs/FCM.</p>
            </div>
            <div class="step">
                <span class="step-num">5</span>
                <h4>The Tick System</h4>
                <p><strong>✓ (single tick)</strong> = message reached the server. <strong>✓✓ (double tick)</strong> = message delivered to their phone. <strong>Blue ✓✓</strong> = they opened and read it. Each tick is a separate acknowledgment traveling back through the system.</p>
            </div>
            <div class="step">
                <span class="step-num">6</span>
                <h4>Group Messages = Fan-Out</h4>
                <p>When you send a message to a group of 50 people, the <strong>Group Service</strong> looks up all 50 members and creates <strong>50 individual deliveries</strong>. Each member gets their own copy routed to their specific gateway. Offline members get queued + push notifications.</p>
            </div>
        </div>

        <div class="interview-tip">
            <h4>💡 Interview Tip</h4>
            <p>The two things interviewers love hearing about WhatsApp: <strong>(1) Erlang</strong> — explain that Erlang can handle millions of lightweight concurrent processes on a single server, which is why WhatsApp served 1 billion users with only ~50 engineers. <strong>(2) Store &amp; Forward</strong> — messages are persisted until delivered, then deleted. The server is a relay, not a permanent store. This is fundamentally different from email or social media.</p>
        </div>
    </div>
</section>

<!-- ==================== GOOGLE SEARCH ==================== -->
<section id="google" class="platform-section google">
    <div class="platform-header">
        <span class="icon">🔍</span>
        <div>
            <h2>Google Search - Web Search Engine</h2>
            <div class="subtitle">Processes 8.5B+ searches/day across an index of hundreds of billions of web pages</div>
        </div>
    </div>

    <div class="info-grid">
        <div class="info-card"><div class="label">Searches / Day</div><div class="value">8.5B+</div></div>
        <div class="info-card"><div class="label">Indexed Pages</div><div class="value">Hundreds of Billions</div></div>
        <div class="info-card"><div class="label">Response Time</div><div class="value">&lt; 200ms</div></div>
        <div class="info-card"><div class="label">Index Size</div><div class="value">100+ PB</div></div>
    </div>

    <div class="diagram-container">
        <h3>High-Level Architecture - Google Search Engine</h3>
        <pre class="mermaid">
graph TB
    subgraph Users["👤 User Layer"]
        Browser["Web Browser"]
        MobileSearch["Google App<br/>Mobile"]
        Voice["Voice Search<br/>Google Assistant"]
    end

    subgraph FrontEnd["🌐 Frontend &amp; Edge"]
        GFE["Google Front End<br/>TLS Termination, Routing"]
        DNS2["Google DNS<br/>Anycast Routing"]
        EdgeCache["Edge Cache<br/>Popular Query Results"]
    end

    subgraph QueryProcessing["🧠 Query Processing Pipeline"]
        QueryParser["Query Parser<br/>Tokenization, Spell Check,<br/>Synonym Expansion"]
        IntentEngine["Intent Classification<br/>Navigational, Informational,<br/>Transactional"]
        QueryRewrite["Query Rewriting<br/>Expansion, Personalization"]
        KnowledgeGraph["Knowledge Graph<br/>Entity Recognition,<br/>Structured Data"]
    end

    subgraph IndexServing["📚 Index Serving Layer"]
        direction TB
        IndexShards["Distributed Index<br/>Sharded by Doc ID"]
        Shard1["Index Shard 1<br/>Inverted Index"]
        Shard2["Index Shard 2<br/>Inverted Index"]
        ShardN["Index Shard N<br/>Inverted Index"]
        DocServer["Document Server<br/>Snippets, Metadata,<br/>Cached Pages"]
    end

    subgraph Ranking["🏆 Ranking Engine"]
        Phase1["Phase 1: Initial Retrieval<br/>BM25 + Term Matching<br/>~1000 candidates"]
        Phase2["Phase 2: ML Ranking<br/>RankBrain / BERT / MUM<br/>~100 candidates"]
        Phase3["Phase 3: Final Ranking<br/>Freshness, Diversity,<br/>Personalization, SafeSearch"]
        AdsRanking["Ads Ranking<br/>Sponsored Results<br/>Quality Score + Bid"]
    end

    subgraph CrawlIndex["🕷️ Crawl &amp; Indexing Pipeline (Offline)"]
        Scheduler["Crawl Scheduler<br/>Priority Queue,<br/>Politeness Rules"]
        Crawler["Web Crawler<br/>(Googlebot)<br/>Distributed Crawlers"]
        Renderer["Rendering Service<br/>JavaScript Rendering<br/>Headless Chrome"]
        Parser["Content Parser<br/>Extract Text, Links,<br/>Structured Data"]
        Indexer["Indexer<br/>Build Inverted Index,<br/>PageRank Computation"]
        DupDetect["Deduplication<br/>Near-duplicate Detection<br/>SimHash"]
    end

    subgraph Storage["💾 Storage Layer"]
        Bigtable[("Bigtable<br/>Crawled Pages,<br/>URL Frontier")]
        Colossus[("Colossus / GFS<br/>Index Files,<br/>Document Store")]
        Spanner[("Spanner<br/>Ads Data,<br/>User Preferences")]
        Memcache["Memcache / Borg<br/>Query Result Cache"]
    end

    Users -->|"HTTPS"| DNS2 --> GFE
    GFE --> EdgeCache
    EdgeCache -->|"Cache Miss"| QueryParser
    QueryParser --> IntentEngine --> QueryRewrite
    QueryRewrite --> KnowledgeGraph
    QueryRewrite --> IndexShards
    IndexShards --> Shard1 & Shard2 & ShardN
    Shard1 & Shard2 & ShardN -->|"Candidate docs"| Phase1
    Phase1 --> Phase2 --> Phase3
    Phase3 --> DocServer
    KnowledgeGraph -->|"Knowledge Panel"| GFE
    AdsRanking -->|"Sponsored results"| GFE
    DocServer -->|"Snippets + URLs"| GFE
    GFE -->|"SERP Response"| Users

    Scheduler --> Crawler --> Renderer --> Parser
    Parser --> DupDetect --> Indexer
    Indexer --> Colossus
    Crawler --> Bigtable
    Parser --> Bigtable
    Phase1 & Phase2 --> Memcache

    style Users fill:#0a1a2d,stroke:#4285f4,color:#fff
    style FrontEnd fill:#f0f5ff,stroke:#4285f4,color:#333
    style QueryProcessing fill:#f5f8ff,stroke:#4285f4,color:#333
    style IndexServing fill:#f8f8ff,stroke:#555,color:#333
    style Ranking fill:#fff8f0,stroke:#ea4335,color:#333
    style CrawlIndex fill:#f0fff0,stroke:#34a853,color:#333
    style Storage fill:#fff5f0,stroke:#fbbc04,color:#333
        </pre>
    </div>

    <div class="diagram-container">
        <h3>Google Search - Query Processing Flow</h3>
        <pre class="mermaid">
sequenceDiagram
    participant U as 👤 User
    participant GFE as Google Front End
    participant Cache as Edge/Query Cache
    participant QP as Query Processor
    participant KG as Knowledge Graph
    participant IDX as Index Servers<br/>(1000s of shards)
    participant Rank as Ranking Engine<br/>(BM25 → BERT → MUM)
    participant Ads as Ads Server
    participant Doc as Document Server

    U->>GFE: Search query (HTTPS)
    GFE->>Cache: Check query cache
    alt Cache Hit (popular query)
        Cache-->>GFE: Cached SERP
        GFE-->>U: Return results (~50ms)
    else Cache Miss
        GFE->>QP: Process query
        QP->>QP: Tokenize, spell-check,<br/>expand synonyms
        QP->>QP: Classify intent<br/>(navigational/informational)
        
        par Parallel Execution
            QP->>KG: Entity lookup
            QP->>IDX: Scatter query to index shards
            QP->>Ads: Fetch relevant ads
        end

        IDX->>IDX: Each shard returns<br/>top-K matching docs
        IDX-->>Rank: ~1000 candidate documents

        Rank->>Rank: Phase 1: BM25 scoring
        Rank->>Rank: Phase 2: ML re-ranking<br/>(BERT/MUM neural models)
        Rank->>Rank: Phase 3: Diversity,<br/>freshness, personalization

        Rank->>Doc: Fetch snippets for top results
        Doc-->>Rank: Titles, URLs, snippets

        KG-->>GFE: Knowledge panel data
        Ads-->>GFE: Sponsored results
        Rank-->>GFE: Organic results (top 10)

        GFE->>GFE: Assemble SERP page
        GFE->>Cache: Cache result
        GFE-->>U: Return SERP (~200ms)
    end
        </pre>
    </div>

    <div class="diagram-container">
        <h3>Google - Web Crawling &amp; Indexing Pipeline</h3>
        <pre class="mermaid">
graph LR
    subgraph Scheduling["Crawl Scheduling"]
        URLFrontier["URL Frontier<br/>Priority Queue"]
        Politeness["Politeness Engine<br/>robots.txt, Rate Limits"]
    end

    subgraph Crawling["Distributed Crawling"]
        Bot1["Googlebot<br/>Instance 1"]
        Bot2["Googlebot<br/>Instance 2"]
        BotN["Googlebot<br/>Instance N"]
    end

    subgraph Processing["Content Processing"]
        Render["JS Renderer<br/>Headless Chrome"]
        Parse["HTML Parser<br/>Text + Links + Schema"]
        Dedup["Deduplication<br/>SimHash / MinHash"]
        Lang["Language Detection<br/>+ Translation"]
    end

    subgraph Indexing["Index Building"]
        InvIdx["Inverted Index<br/>Builder"]
        PageRank["PageRank<br/>Computation"]
        FwdIdx["Forward Index<br/>Doc Metadata"]
    end

    URLFrontier --> Politeness
    Politeness --> Bot1 & Bot2 & BotN
    Bot1 & Bot2 & BotN --> Render --> Parse
    Parse --> Dedup --> Lang
    Lang --> InvIdx & PageRank & FwdIdx
    Parse -->|"New URLs"| URLFrontier

    style Scheduling fill:#e8f5e9,stroke:#4caf50,color:#333
    style Crawling fill:#e3f2fd,stroke:#2196f3,color:#333
    style Processing fill:#fff3e0,stroke:#ff9800,color:#333
    style Indexing fill:#fce4ec,stroke:#e91e63,color:#333
        </pre>
    </div>

    <div class="tech-stack">
        <span class="tech-tag">C++</span>
        <span class="tech-tag">Java</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Go</span>
        <span class="tech-tag">Bigtable</span>
        <span class="tech-tag">Colossus (GFS)</span>
        <span class="tech-tag">Spanner</span>
        <span class="tech-tag">Borg</span>
        <span class="tech-tag">MapReduce</span>
        <span class="tech-tag">TensorFlow</span>
        <span class="tech-tag">BERT/MUM</span>
        <span class="tech-tag">Protocol Buffers</span>
    </div>

    <div class="key-points">
        <div class="key-point">
            <h4>Three-Phase Ranking</h4>
            <p>Initial retrieval uses BM25/term matching to get ~1000 candidates. ML models (BERT, MUM) re-rank for semantic relevance. Final pass applies freshness, diversity, and personalization signals.</p>
        </div>
        <div class="key-point">
            <h4>Scatter-Gather on Index Shards</h4>
            <p>The index is partitioned across thousands of servers. A query is scattered to all relevant shards in parallel, each returns top-K results, and results are merged and ranked globally.</p>
        </div>
        <div class="key-point">
            <h4>Continuous Crawling</h4>
            <p>Googlebot continuously crawls the web using a priority-based URL frontier. High-value pages (news sites) are re-crawled frequently; low-value pages less often. JavaScript rendering uses headless Chrome.</p>
        </div>
        <div class="key-point">
            <h4>Knowledge Graph</h4>
            <p>A massive entity graph (5B+ entities) powers knowledge panels, featured snippets, and entity disambiguation. Integrates structured data from Wikipedia, Wikidata, and schema.org markup.</p>
        </div>
    </div>

    <!-- EASY EXPLANATION -->
    <div class="easy-explanation">
        <h3><span class="emoji">🧠</span> Explain It Like I'm 5: How Google Search Works</h3>

        <div class="analogy">
            Imagine the world's biggest <strong>library with hundreds of billions of books</strong> (web pages). Google has three jobs: <strong>(1) Send librarians (crawlers) to find and catalog every book</strong>, <strong>(2) Build a massive card catalog (index) so you can look things up instantly</strong>, and <strong>(3) When you ask a question, find the 10 best books in under 0.2 seconds</strong> — out of hundreds of billions. That's like finding a specific grain of sand on a beach, instantly.
        </div>

        <p class="summary-text">Google Search has two big parts — an <strong>offline pipeline</strong> (crawling the web) and an <strong>online pipeline</strong> (answering your query):</p>

        <div class="step-flow">
            <div class="step">
                <span class="step-num">1</span>
                <h4>Crawling (Offline)</h4>
                <p><strong>Googlebot</strong> (an army of automated programs) visits web pages by following links. It's polite — it checks <strong>robots.txt</strong> to see what it's allowed to crawl, and doesn't hit any website too fast. Important sites (like news) get crawled every few minutes; small blogs maybe once a month.</p>
            </div>
            <div class="step">
                <span class="step-num">2</span>
                <h4>Rendering &amp; Parsing (Offline)</h4>
                <p>Many modern websites need JavaScript to display content. Google runs a <strong>headless Chrome browser</strong> to render pages just like you would. Then it <strong>extracts the text, links, images, and structured data</strong> from each page.</p>
            </div>
            <div class="step">
                <span class="step-num">3</span>
                <h4>Indexing (Offline)</h4>
                <p>The extracted content is organized into an <strong>inverted index</strong> — a giant lookup table that says "the word 'pizza' appears on these 50 million pages." This index is <strong>sharded across thousands of servers</strong>. Google also computes <strong>PageRank</strong> — how important each page is based on who links to it.</p>
            </div>
            <div class="step">
                <span class="step-num">4</span>
                <h4>You Type a Query (Online)</h4>
                <p>Your query goes to the <strong>Google Front End</strong>, which checks if this exact query was recently searched (cache hit = instant response). If not, the <strong>Query Processor</strong> fixes typos, expands synonyms, and figures out what you actually mean (intent classification).</p>
            </div>
            <div class="step">
                <span class="step-num">5</span>
                <h4>Scatter-Gather on Index (Online)</h4>
                <p>The processed query is sent to <strong>thousands of index shards simultaneously</strong> (scatter). Each shard returns its best matching documents. Results are <strong>gathered and merged</strong> into ~1000 candidates. This all happens in milliseconds.</p>
            </div>
            <div class="step">
                <span class="step-num">6</span>
                <h4>Three-Phase Ranking (Online)</h4>
                <p><strong>Phase 1:</strong> Fast scoring (BM25) narrows 1000 → 100 candidates. <strong>Phase 2:</strong> Deep ML models (BERT, MUM) understand the meaning of your query and re-rank for relevance. <strong>Phase 3:</strong> Final adjustments for freshness, diversity, and personalization. Top 10 results are shown to you.</p>
            </div>
        </div>

        <div class="interview-tip">
            <h4>💡 Interview Tip</h4>
            <p>The key insight for Google Search is the <strong>separation of offline (crawl + index) and online (query + rank) pipelines</strong>. The index is pre-built, so queries don't search the live web — they search a pre-computed index. Also emphasize <strong>scatter-gather</strong>: the index is too large for one machine, so queries fan out to thousands of shards in parallel and results are merged. This is the fundamental pattern behind all search engines at scale.</p>
        </div>
    </div>
</section>

<!-- ==================== INSTAGRAM ==================== -->
<section id="instagram" class="platform-section instagram">
    <div class="platform-header">
        <span class="icon">📸</span>
        <div>
            <h2>Instagram - Photo &amp; Video Sharing Platform</h2>
            <div class="subtitle">2B+ monthly active users, 100M+ photos uploaded daily, hybrid feed generation</div>
        </div>
    </div>

    <div class="info-grid">
        <div class="info-card"><div class="label">Monthly Active Users</div><div class="value">2B+</div></div>
        <div class="info-card"><div class="label">Photos / Day</div><div class="value">100M+</div></div>
        <div class="info-card"><div class="label">Likes / Day</div><div class="value">4.2B+</div></div>
        <div class="info-card"><div class="label">Stories / Day</div><div class="value">500M+</div></div>
    </div>

    <div class="diagram-container">
        <h3>High-Level Architecture - Instagram Platform</h3>
        <pre class="mermaid">
graph TB
    subgraph Clients["📱 Client Layer"]
        iOSApp["iOS App"]
        AndroidApp["Android App"]
        WebApp2["Web App<br/>React"]
    end

    subgraph EdgeCDN2["🌐 CDN &amp; Edge"]
        FBCDN["Facebook CDN<br/>Global Edge PoPs"]
        ImgCDN["Image CDN<br/>Multiple Resolutions"]
        VideoCDN["Video CDN<br/>Reels, Stories, IGTV"]
    end

    subgraph LBLayer["🚪 Load Balancing &amp; Routing"]
        LB2["L7 Load Balancer<br/>Proxygen"]
        APIRoute["API Router<br/>GraphQL Gateway"]
        RateLimit2["Rate Limiter"]
    end

    subgraph AppServices["⚙️ Application Services (Django + Async)"]
        direction TB
        subgraph UserDomain["User Domain"]
            UserSvc2["User Service<br/>Profiles, Settings"]
            AuthSvc2["Auth Service<br/>OAuth, SSO via Meta"]
            FollowSvc["Social Graph Service<br/>Follow/Unfollow, Suggestions"]
        end
        subgraph ContentDomain2["Content Domain"]
            PostSvc["Post Service<br/>Create, Edit, Delete"]
            StorySvc["Stories Service<br/>24hr Ephemeral Content"]
            ReelsSvc["Reels Service<br/>Short Video"]
            CommentSvc["Comment Service<br/>Threaded Comments"]
            LikeSvc["Like Service<br/>Counter + Feed Signal"]
        end
        subgraph FeedDomain["Feed Domain"]
            FeedGen["Feed Generator<br/>Hybrid Fan-out"]
            FeedRank["Feed Ranking<br/>ML Model (Interest, Recency,<br/>Relationship)"]
            ExploreSvc["Explore Service<br/>Discovery + Trending"]
        end
        subgraph MediaPipeline2["Media Pipeline"]
            Upload["Upload Service<br/>Chunked Upload"]
            ImgProcess["Image Processing<br/>Resize, Filter, Compress<br/>(5+ resolutions)"]
            VidProcess["Video Processing<br/>Transcode, Thumbnail"]
            ContentMod["Content Moderation<br/>ML-based NSFW Detection"]
        end
        subgraph Engagement["Engagement"]
            NotifSvc["Notification Service<br/>Push + In-App"]
            DMSvc["Direct Messages<br/>E2E Encrypted"]
            SearchSvc2["Search Service<br/>Users, Tags, Places"]
        end
    end

    subgraph DataLayer2["💾 Data Layer"]
        PostgreSQL2[("PostgreSQL<br/>User Data, Posts,<br/>Comments")]
        Cassandra2[("Cassandra<br/>Feed Store,<br/>Activity Log")]
        Redis3["Redis / Memcached<br/>Feed Cache, Sessions,<br/>Counters"]
        S3Store2[("S3 / Blob Storage<br/>Photos, Videos,<br/>Stories")]
        ES["Elasticsearch<br/>Search Index"]
        Kafka3["Kafka<br/>Event Bus"]
        ML["ML Platform<br/>Feed Ranking,<br/>Content Moderation"]
    end

    Clients -->|"HTTPS"| LB2
    LB2 --> RateLimit2 --> APIRoute
    APIRoute --> UserDomain & ContentDomain2 & FeedDomain & Engagement
    PostSvc --> Upload
    Upload --> ImgProcess & VidProcess
    ImgProcess & VidProcess --> ContentMod
    ContentMod --> S3Store2
    S3Store2 --> FBCDN & ImgCDN & VideoCDN
    FBCDN & ImgCDN & VideoCDN --> Clients

    FeedGen --> FeedRank
    FeedRank --> ML
    PostSvc -->|"New post event"| Kafka3
    Kafka3 --> FeedGen
    Kafka3 --> NotifSvc

    UserDomain --> PostgreSQL2 & Redis3
    ContentDomain2 --> PostgreSQL2 & Cassandra2
    FeedDomain --> Cassandra2 & Redis3
    SearchSvc2 --> ES
    Engagement --> Redis3 & Kafka3

    style Clients fill:#2d0a1a,stroke:#e1306c,color:#fff
    style EdgeCDN2 fill:#fff0f5,stroke:#e1306c,color:#333
    style LBLayer fill:#fff5f8,stroke:#e1306c,color:#333
    style AppServices fill:#fff8fa,stroke:#555,color:#333
    style DataLayer2 fill:#faf0f5,stroke:#555,color:#333
        </pre>
    </div>

    <div class="diagram-container">
        <h3>Instagram - Photo Upload &amp; Feed Generation Flow</h3>
        <pre class="mermaid">
sequenceDiagram
    participant U as 👤 User (Alice)
    participant API as API Gateway
    participant Post as Post Service
    participant Media as Media Pipeline
    participant Mod as Content Moderation
    participant S3 as Blob Storage
    participant CDN2 as Facebook CDN
    participant K as Kafka Event Bus
    participant FG as Feed Generator
    participant Cache as Feed Cache (Redis)
    participant F as 👤 Follower (Bob)

    U->>API: Upload photo + caption
    API->>Post: Create post record
    Post->>Media: Process image
    Media->>Media: Generate 5+ resolutions<br/>(thumbnail, small, medium, large, original)
    Media->>Mod: ML content moderation
    Mod-->>Media: Approved ✓
    Media->>S3: Store all resolutions
    S3-->>CDN2: Replicate to edge PoPs
    Post->>Post: Save post metadata to DB

    Post->>K: Publish "new_post" event

    par Hybrid Fan-Out
        K->>FG: Trigger feed update
        Note over FG: Celebrity (>10K followers):<br/>Pull model - compute at read time
        Note over FG: Regular user:<br/>Push model - write to follower feeds
        FG->>Cache: Push post to follower feed caches<br/>(for regular users)
    and Notifications
        K->>F: Push notification<br/>"Alice posted a new photo"
    end

    Note over F: Bob opens Instagram
    F->>API: GET /feed
    API->>FG: Generate feed
    FG->>Cache: Fetch cached feed entries
    FG->>FG: Merge push entries +<br/>pull celebrity posts
    FG->>FG: ML Ranking<br/>(interest, recency, relationship)
    FG-->>API: Ranked feed
    API-->>F: Personalized feed with Alice's post
        </pre>
    </div>

    <div class="diagram-container">
        <h3>Instagram - Hybrid Fan-Out Strategy</h3>
        <pre class="mermaid">
graph TB
    subgraph PostEvent["New Post Created"]
        NewPost["📸 New Post"]
    end

    NewPost --> Decision{"User has<br/>> 10K followers?"}

    Decision -->|"No (Regular User)"| PushPath
    Decision -->|"Yes (Celebrity)"| PullPath

    subgraph PushPath["Push Model (Write-time Fan-out)"]
        direction TB
        PushWorker["Async Worker<br/>reads follower list"]
        PushWrite["Write post ID to each<br/>follower's feed cache"]
        PushResult["✅ Feed pre-computed<br/>Fast reads for followers"]
    end

    subgraph PullPath["Pull Model (Read-time Fan-out)"]
        direction TB
        PullStore["Store post in<br/>celebrity post index"]
        PullRead["At read time: merge<br/>celebrity posts into feed"]
        PullResult["✅ Avoids writing to<br/>millions of feeds"]
    end

    PushWorker --> PushWrite --> PushResult
    PullStore --> PullRead --> PullResult

    subgraph FeedRead["📱 Feed Read Request"]
        Merge["Merge push entries +<br/>pull celebrity posts"]
        Rank["ML Ranking<br/>Interest + Recency +<br/>Relationship Score"]
        Serve["Serve Top-N Posts"]
    end

    PushResult --> Merge
    PullResult --> Merge
    Merge --> Rank --> Serve

    style PostEvent fill:#e1306c,stroke:#333,color:#fff
    style Decision fill:#fff3cd,stroke:#856404,color:#333
    style PushPath fill:#d4edda,stroke:#155724,color:#333
    style PullPath fill:#cce5ff,stroke:#004085,color:#333
    style FeedRead fill:#f8f9fa,stroke:#333,color:#333
        </pre>
    </div>

    <div class="tech-stack">
        <span class="tech-tag">Python / Django</span>
        <span class="tech-tag">React Native</span>
        <span class="tech-tag">GraphQL</span>
        <span class="tech-tag">PostgreSQL</span>
        <span class="tech-tag">Cassandra</span>
        <span class="tech-tag">Redis</span>
        <span class="tech-tag">Memcached</span>
        <span class="tech-tag">Kafka</span>
        <span class="tech-tag">Elasticsearch</span>
        <span class="tech-tag">S3</span>
        <span class="tech-tag">Facebook CDN</span>
        <span class="tech-tag">PyTorch</span>
    </div>

    <div class="key-points">
        <div class="key-point">
            <h4>Hybrid Fan-Out</h4>
            <p>Regular users use push model (write to follower feeds at post time). Celebrities use pull model (compute at read time) to avoid writing to millions of feeds. This balances write amplification vs read latency.</p>
        </div>
        <div class="key-point">
            <h4>ML-Powered Feed Ranking</h4>
            <p>Feed is ranked using ML signals: interest score (engagement history), recency, relationship strength (DMs, profile visits), and content type preference. Not chronological.</p>
        </div>
        <div class="key-point">
            <h4>Multi-Resolution Media</h4>
            <p>Each uploaded image is processed into 5+ resolutions. The client requests the appropriate size based on device screen and network conditions, reducing bandwidth usage.</p>
        </div>
        <div class="key-point">
            <h4>Thundering Herd Protection</h4>
            <p>When a celebrity posts, millions of followers may request the same content simultaneously. Cache stampede protection uses request coalescing and staggered cache expiry.</p>
        </div>
    </div>

    <!-- EASY EXPLANATION -->
    <div class="easy-explanation">
        <h3><span class="emoji">🧠</span> Explain It Like I'm 5: How Instagram Works</h3>

        <div class="analogy">
            Think of Instagram like a <strong>newspaper that's different for every single reader</strong>. When you post a photo, it's like dropping a flyer at the newspaper office. For your friends (regular users), the newspaper <strong>prints your flyer into their personal edition right away</strong> (push model). But for celebrities with millions of followers, the newspaper doesn't print millions of copies immediately — instead, it <strong>keeps the flyer on file and adds it when each reader picks up their paper</strong> (pull model). This clever trick is called <strong>hybrid fan-out</strong>.
        </div>

        <p class="summary-text">Here's the full journey of a photo from your camera to your friend's feed:</p>

        <div class="step-flow">
            <div class="step">
                <span class="step-num">1</span>
                <h4>You Upload a Photo</h4>
                <p>Your photo is sent to the <strong>Upload Service</strong> via chunked upload (so large files don't fail on bad networks). The <strong>Media Pipeline</strong> then creates <strong>5+ versions</strong> of your photo — thumbnail, small, medium, large, and original — so each device gets the right size.</p>
            </div>
            <div class="step">
                <span class="step-num">2</span>
                <h4>Content Moderation</h4>
                <p>Before your photo goes live, an <strong>ML model scans it</strong> for nudity, violence, spam, and policy violations. This happens automatically in milliseconds. If flagged, it goes to human review. If clean, it proceeds.</p>
            </div>
            <div class="step">
                <span class="step-num">3</span>
                <h4>Storage &amp; CDN</h4>
                <p>All image versions are stored in <strong>blob storage (S3)</strong> and replicated to <strong>Facebook's global CDN</strong> — hundreds of edge servers worldwide. When your friend views the photo, it loads from the nearest edge server, not from a central data center.</p>
            </div>
            <div class="step">
                <span class="step-num">4</span>
                <h4>Feed Update (Hybrid Fan-Out)</h4>
                <p>A <strong>"new_post" event</strong> is published to Kafka. The Feed Generator checks: <strong>Do you have fewer than 10K followers?</strong> If yes → your post ID is <strong>written directly into each follower's feed cache</strong> (push). If you're a celebrity → your post is just <strong>indexed</strong>, and followers pull it when they open the app.</p>
            </div>
            <div class="step">
                <span class="step-num">5</span>
                <h4>Your Friend Opens Instagram</h4>
                <p>The <strong>Feed Generator</strong> merges pre-pushed posts + celebrity posts pulled on-demand. Then the <strong>ML Ranking model</strong> sorts everything by: how interested your friend is in your content, how recent the post is, and how close your relationship is (based on DMs, profile visits, likes).</p>
            </div>
            <div class="step">
                <span class="step-num">6</span>
                <h4>Why Not Just Show Everything Chronologically?</h4>
                <p>Instagram found that users <strong>miss 70% of posts</strong> in a chronological feed because they follow too many accounts. The ML-ranked feed ensures you see the posts you care about most. The Explore page uses similar ML to show content from accounts you <strong>don't</strong> follow but might like.</p>
            </div>
        </div>

        <div class="interview-tip">
            <h4>💡 Interview Tip</h4>
            <p>The star concept for Instagram is <strong>hybrid fan-out</strong>. Explain the tradeoff clearly: <strong>Push model</strong> = fast reads but expensive writes (writing to millions of feeds). <strong>Pull model</strong> = cheap writes but slow reads (computing feed on the fly). Instagram combines both — push for regular users, pull for celebrities. This shows you understand write amplification vs read latency tradeoffs, which is exactly what interviewers want to hear.</p>
        </div>
    </div>
</section>

<!-- ==================== COMPARISON TABLE ==================== -->
<section class="platform-section" style="margin-top: 60px;">
    <h2 style="text-align:center; color: #7b2ff7; font-size: 2rem; margin-bottom: 30px;">📊 Cross-Platform Comparison</h2>

    <div class="diagram-container">
        <h3>Architecture Pattern Comparison</h3>
        <pre class="mermaid">
graph LR
    subgraph Patterns["Key Architecture Patterns"]
        direction TB
        P1["🎬 Netflix<br/>Microservices + Custom CDN<br/>Adaptive Bitrate Streaming"]
        P2["🏏 JioHotstar<br/>Multi-CDN + SSAI<br/>Extreme Concurrency (59M)"]
        P3["💬 WhatsApp<br/>Erlang Actors + WebSocket<br/>E2E Encryption + Store-Forward"]
        P4["🔍 Google Search<br/>Scatter-Gather + 3-Phase Ranking<br/>Continuous Crawl Pipeline"]
        P5["📸 Instagram<br/>Hybrid Fan-out + ML Ranking<br/>Multi-Resolution Media Pipeline"]
    end

    subgraph CommonPatterns["Shared Patterns"]
        direction TB
        C1["Load Balancing<br/>+ Auto-scaling"]
        C2["Caching Layers<br/>(Redis, Memcached)"]
        C3["Event-Driven<br/>(Kafka)"]
        C4["Microservices<br/>Architecture"]
        C5["CDN for<br/>Static Content"]
        C6["ML/AI for<br/>Personalization"]
    end

    P1 & P2 & P3 & P4 & P5 --> C1 & C2 & C3 & C4 & C5 & C6

    style Patterns fill:#f8f8ff,stroke:#7b2ff7,color:#333
    style CommonPatterns fill:#f0fff0,stroke:#4caf50,color:#333
        </pre>
    </div>
</section>

<footer>
    <p>System Design Interview Reference | Built with Mermaid.js</p>
    <p style="margin-top: 8px; font-size: 0.85rem;">
        Sources: 
        <a href="https://blog.algomaster.io" style="color:#7b2ff7">AlgoMaster</a> · 
        <a href="https://www.systemdesignhandbook.com" style="color:#7b2ff7">System Design Handbook</a> · 
        <a href="https://blog.bytebytego.com" style="color:#7b2ff7">ByteByteGo</a> · 
        <a href="https://blog.hotstar.com" style="color:#7b2ff7">Hotstar Engineering Blog</a> · 
        <a href="https://developers.google.com/search/docs/fundamentals/how-search-works" style="color:#7b2ff7">Google Search Docs</a>
    </p>
    <p style="margin-top: 5px; font-size: 0.75rem; color: #666;">Content was rephrased for compliance with licensing restrictions.</p>
    <div style="margin-top: 30px; padding-top: 20px; border-top: 1px solid #222;">
        <p style="font-size: 1.4rem; font-weight: 700; letter-spacing: 3px; background: linear-gradient(90deg, #7b2ff7, #00d2ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; opacity: 0.6;">ANUBHAV THAKUR</p>
        <p style="font-size: 0.75rem; color: #444; margin-top: 4px; letter-spacing: 1px;">© 2026 · All Rights Reserved</p>
    </div>
</footer>

<script>
    mermaid.initialize({
        startOnLoad: true,
        theme: 'default',
        securityLevel: 'loose',
        flowchart: {
            useMaxWidth: true,
            htmlLabels: true,
            curve: 'basis',
            padding: 15,
            nodeSpacing: 30,
            rankSpacing: 50
        },
        sequence: {
            useMaxWidth: true,
            showSequenceNumbers: false,
            actorMargin: 50,
            messageMargin: 40
        }
    });
</script>

</body>
</html>
