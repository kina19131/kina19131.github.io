---
layout: page
title: Projects
permalink: /work/
description: Things I've built — at school, at work, and on the side.
nav: true
nav_order: 3
---

<div class="projects-page">

  <!-- ── ACADEMIC ─────────────────────────────────────── -->
  <div class="proj-section">
    <div class="proj-section-label">Academic &middot; 2025</div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div class="proj-card-title-block">
          <div class="proj-card-title">fAI &mdash; Fair AI Hiring</div>
          <div class="proj-card-sub">Adversarial debiasing system to detect and reduce gender bias in AI-powered resume screening. Built during AI4Good Mila Lab Fellowship.</div>
        </div>
        <div class="proj-header-links">
          <a href="{{ '/assets/pdf/fai_slides.pdf' | relative_url }}" target="_blank" rel="noopener" class="proj-header-chip">Slides ↗</a>
        </div>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">PyTorch</span>
        <span class="proj-tag">Adversarial ML</span>
        <span class="proj-tag">Fairness</span>
        <span class="proj-tag">Python</span>
      </div>

      <div class="proj-stats">
        <div class="proj-stat"><span class="proj-stat-num">−23%</span><span class="proj-stat-lbl">demographic disparity</span></div>
        <div class="proj-stat"><span class="proj-stat-num">&lt;2%</span><span class="proj-stat-lbl">accuracy lost</span></div>
        <div class="proj-stat"><span class="proj-stat-num">$3K</span><span class="proj-stat-lbl">competitive funding</span></div>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">
          <blockquote>
            <strong>Ignored as Erin. Hired as Mack.</strong> Erin McKelvey applied to dozens of tech jobs &mdash; no callbacks. She switched to the name <em>Mack</em>. Her response rate jumped to 70%. Today, Mack is a CEO.
          </blockquote>
          <p>Only 15% of tech CEOs are women. Amazon built an AI screener trained on mostly male r&eacute;sum&eacute;s &mdash; it penalized terms like &ldquo;women&rsquo;s college.&rdquo; They scrapped it. We built fAI to fix this.</p>

          <h5>How it works</h5>
          <p>Two models trained in opposition: a <strong>classifier</strong> that predicts profession from a r&eacute;sum&eacute;, and an <strong>adversary</strong> that tries to guess gender from the classifier&rsquo;s output. If the adversary succeeds, the classifier is penalized. Over training cycles, it learns to carry no gender signal. The adversary is removed &mdash; leaving a fairer model.</p>

          <h5>Platform</h5>
          <p>Hiring teams upload their screening model &rarr; audit using Equal Opportunity and Equalized Odds metrics &rarr; debias via the adversarial pipeline &rarr; earn a Fair AI badge. Secured $3,000 in competitive funding and endorsement from leading researchers at Mila. Compliant with PIPEDA, CHRA, and the EU AI Act. Humans always make the final call.</p>

          <p class="proj-team">Kina Kim, Fatima Masood, Shuting Xie, Iman Cheema, Aaina Garg &middot; AI4Good Mila Lab Fellowship &middot; Demo Day 2025</p>
        </div>
      </details>
    </div>
  </div>

  <!-- ── IBM ────────────────────────────────────────────── -->
  <div class="proj-section">
    <div class="proj-section-label">IBM &middot; Current</div>

    <!-- BYOC -->
    <div class="proj-card">
      <div class="proj-card-header">
        <div class="proj-card-title-block">
          <div class="proj-card-title">Db2 as a Service &mdash; BYOC on Azure</div>
          <div class="proj-card-sub">IBM Db2 SaaS deployed inside the customer&rsquo;s own cloud VPC &mdash; IBM manages the full service lifecycle while customers retain complete ownership of their data and infrastructure.</div>
        </div>
        <div class="proj-header-links">
          <a href="https://www.ibm.com/new/announcements/ibm-db2-and-db2-warehouse-saas-on-azure-byoc" target="_blank" rel="noopener" class="proj-header-chip">Announcement ↗</a>
          <a href="https://cloud.ibm.com/apidocs/db2-on-cloud-byoc" target="_blank" rel="noopener" class="proj-header-chip">API docs ↗</a>
        </div>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Go</span>
        <span class="proj-tag">Ruby</span>
        <span class="proj-tag">gRPC</span>
        <span class="proj-tag">REST APIs</span>
        <span class="proj-tag">AWS</span>
        <span class="proj-tag">Azure</span>
        <span class="proj-tag">CI/CD</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">

          <h5>What I worked on</h5>
          <p>Designed RESTful API contracts and implemented backend services in Go/Ruby with gRPC-based dispatching for new cloud backup features, enabling reliable database instance lifecycle management. Architected testing infrastructure for Db2 on Cloud across AWS and Azure, ensuring 99.9% reliability for enterprise database operations serving 500+ customers.</p>

          <h5>Architecture</h5>
          <div class="byoc-diagram-wrap">
            <svg viewBox="0 0 640 310" xmlns="http://www.w3.org/2000/svg" class="byoc-diagram" aria-label="BYOC architecture: customer VPC on left, credentials and access in centre, IBM control plane on right">
              <defs>
                <marker id="arr" markerWidth="7" markerHeight="7" refX="6" refY="3.5" orient="auto">
                  <path d="M0,0 L7,3.5 L0,7 Z" class="byoc-arrow"/>
                </marker>
              </defs>

              <!-- Customer Cloud outer -->
              <rect x="8" y="28" width="230" height="270" rx="8" class="byoc-box-blue-outer"/>
              <text x="18" y="47" class="byoc-label-outer">Customer Cloud (AWS / Azure / GCP)</text>

              <!-- Customer VPC inner -->
              <rect x="18" y="54" width="210" height="235" rx="6" class="byoc-box-blue-inner"/>
              <text x="28" y="71" class="byoc-label-inner">Customer VPC</text>

              <!-- App -->
              <rect x="78" y="78" width="100" height="28" rx="4" class="byoc-node-blue"/>
              <text x="128" y="97" class="byoc-node-text">Customer App</text>

              <!-- Workloads box -->
              <rect x="28" y="118" width="190" height="100" rx="5" class="byoc-box-workloads"/>
              <text x="38" y="134" class="byoc-label-inner">Workloads</text>
              <rect x="36" y="140" width="82" height="22" rx="3" class="byoc-node-blue"/>
              <text x="77" y="156" class="byoc-node-text">Databases</text>
              <rect x="126" y="140" width="82" height="22" rx="3" class="byoc-node-blue"/>
              <text x="167" y="156" class="byoc-node-text">Deployments</text>
              <rect x="36" y="168" width="82" height="22" rx="3" class="byoc-node-blue"/>
              <text x="77" y="184" class="byoc-node-text">Autoscaling</text>
              <rect x="126" y="168" width="82" height="22" rx="3" class="byoc-node-blue"/>
              <text x="167" y="184" class="byoc-node-text">Logs / Metrics</text>

              <!-- Nodes -->
              <rect x="28" y="228" width="190" height="50" rx="5" class="byoc-box-workloads"/>
              <text x="38" y="244" class="byoc-label-inner">Nodes</text>
              <rect x="36" y="250" width="30" height="18" rx="3" class="byoc-node-blue"/>
              <rect x="72" y="250" width="30" height="18" rx="3" class="byoc-node-blue"/>
              <rect x="108" y="250" width="30" height="18" rx="3" class="byoc-node-blue"/>
              <rect x="144" y="250" width="30" height="18" rx="3" class="byoc-node-blue"/>

              <!-- App → Workloads -->
              <line x1="128" y1="106" x2="128" y2="116" class="byoc-line" marker-end="url(#arr)"/>

              <!-- Credentials box -->
              <rect x="258" y="80" width="128" height="68" rx="6" class="byoc-box-yellow"/>
              <text x="322" y="97" class="byoc-label-mid">Credentials</text>
              <rect x="266" y="103" width="112" height="18" rx="3" class="byoc-node-yellow"/>
              <text x="322" y="116" class="byoc-node-text-dark">IAM / Secret Key</text>
              <rect x="266" y="123" width="112" height="18" rx="3" class="byoc-node-yellow"/>
              <text x="322" y="136" class="byoc-node-text-dark">Cross-Account Connect</text>

              <!-- Access box -->
              <rect x="258" y="165" width="128" height="88" rx="6" class="byoc-box-yellow"/>
              <text x="322" y="182" class="byoc-label-mid">Access</text>
              <rect x="266" y="188" width="112" height="18" rx="3" class="byoc-node-yellow"/>
              <text x="322" y="201" class="byoc-node-text-dark">Public Trusted IP</text>
              <rect x="266" y="210" width="112" height="18" rx="3" class="byoc-node-yellow"/>
              <text x="322" y="223" class="byoc-node-text-dark">VPC Peering</text>
              <rect x="266" y="232" width="112" height="18" rx="3" class="byoc-node-yellow"/>
              <text x="322" y="245" class="byoc-node-text-dark">VPN</text>

              <!-- Arrows centre ↔ sides -->
              <line x1="238" y1="195" x2="256" y2="195" class="byoc-line" marker-end="url(#arr)"/>
              <line x1="258" y1="115" x2="240" y2="115" class="byoc-line" marker-end="url(#arr)"/>
              <line x1="388" y1="115" x2="406" y2="115" class="byoc-line" marker-end="url(#arr)"/>
              <line x1="406" y1="195" x2="388" y2="195" class="byoc-line" marker-end="url(#arr)"/>

              <!-- IBM Control Plane outer -->
              <rect x="406" y="28" width="226" height="270" rx="8" class="byoc-box-green-outer"/>
              <text x="416" y="47" class="byoc-label-outer-green">IBM Control Plane</text>

              <rect x="414" y="56" width="98" height="28" rx="4" class="byoc-node-green"/>
              <text x="463" y="75" class="byoc-node-text">Dashboard</text>
              <rect x="520" y="56" width="98" height="28" rx="4" class="byoc-node-green"/>
              <text x="569" y="75" class="byoc-node-text">API / CLI</text>

              <rect x="414" y="94" width="98" height="28" rx="4" class="byoc-node-green"/>
              <text x="463" y="113" class="byoc-node-text">Jobs</text>
              <rect x="520" y="94" width="98" height="28" rx="4" class="byoc-node-green"/>
              <text x="569" y="113" class="byoc-node-text">Backend</text>

              <rect x="414" y="132" width="204" height="28" rx="4" class="byoc-node-green"/>
              <text x="516" y="151" class="byoc-node-text">Database Engine</text>

              <rect x="414" y="170" width="204" height="28" rx="4" class="byoc-box-green-note"/>
              <text x="516" y="189" class="byoc-node-text">Backup &amp; Recovery</text>

              <rect x="414" y="208" width="204" height="28" rx="4" class="byoc-box-green-note"/>
              <text x="516" y="227" class="byoc-node-text">Monitoring &amp; Alerts</text>

              <rect x="414" y="246" width="204" height="40" rx="4" class="byoc-box-green-note"/>
              <text x="516" y="262" class="byoc-node-text">AWS / Azure / GCP</text>
              <text x="516" y="278" class="byoc-node-text">External Resources</text>
            </svg>
            <p class="byoc-diagram-caption">BYOC architecture: customer data stays inside their own VPC; IBM manages the control plane separately.</p>
          </div>

          <h5>What the product does</h5>
          <ul>
            <li><strong>Compliance controls</strong> &mdash; database runs inside the customer&rsquo;s own VPC, meeting the strictest data sovereignty requirements</li>
            <li><strong>Independent scaling</strong> &mdash; compute and storage scale separately with auto-increase thresholds</li>
            <li><strong>High availability</strong> &mdash; 2-node setup across 2 availability zones with automated failover</li>
            <li><strong>Data co-location</strong> &mdash; keeps data within the customer&rsquo;s cloud account, co-located with their apps</li>
          </ul>

        </div>
      </details>
    </div>

    <!-- Db2 SaaS -->
    <div class="proj-card">
      <div class="proj-card-header">
        <div class="proj-card-title-block">
          <div class="proj-card-title">Db2 as a Service (IBM Cloud)</div>
          <div class="proj-card-sub">IBM&rsquo;s fully managed relational database for mission-critical OLTP workloads &mdash; high availability, automated backups, built-in ML capabilities, and enterprise-grade security on IBM Cloud and AWS.</div>
        </div>
        <div class="proj-header-links">
          <a href="https://www.ibm.com/docs/en/db2-as-a-service?topic=overview" target="_blank" rel="noopener" class="proj-header-chip">Docs ↗</a>
        </div>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Python</span>
        <span class="proj-tag">GAN</span>
        <span class="proj-tag">Random Forest</span>
        <span class="proj-tag">Anomaly Detection</span>
        <span class="proj-tag">Bash</span>
        <span class="proj-tag">Db2</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">

          <h5>What I worked on</h5>
          <p>Led development and delivery of fix patches to address customer-reported issues and improve feature reliability, ensuring smooth version control and dependency management by identifying and replacing outdated packages. Contributed to new feature development, including external backup capacity. Designed and implemented a GAN-based SQL query generator that produced 1,000+ synthetic test cases, expanding traditional testing coverage, increasing edge-case detection by 15%, and surfacing critical bugs in the Db2 query optimizer prior to production release.</p>

          <h5>What the product does</h5>
          <ul>
            <li><strong>Blazing-fast engine</strong> &mdash; IBM BLU Acceleration and advanced query optimizations from IBM Research for OLTP workloads</li>
            <li><strong>Elastic scaling</strong> &mdash; independently scale compute and storage via UI or REST API</li>
            <li><strong>Built-in ML</strong> &mdash; train and run ML models directly in the Db2 engine using SQL, Python, or R</li>
            <li><strong>Fully managed</strong> &mdash; automated monitoring, failovers, and geo-replicated disaster recovery backups</li>
          </ul>

        </div>
      </details>
    </div>

  </div>

  <!-- ── UNIVERSITY OF WATERLOO ───────────────────────── -->
  <div class="proj-section">
    <div class="proj-section-label">University of Waterloo &middot; 2018&ndash;2019</div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div class="proj-card-title-block">
          <div class="proj-card-title">AR Exhibit Scanner &mdash; Computer Museum</div>
          <div class="proj-card-sub">Image-recognition AR app built with Unity and Vuforia to let museum visitors scan exhibits and surface contextual information and media overlays in real time.</div>
        </div>
        <div class="proj-header-links">
          <a href="{{ '/assets/pdf/Kina Kim Unity + Vuforia AR development documentation.pdf' | relative_url }}" target="_blank" rel="noopener" class="proj-header-chip">Docs ↗</a>
        </div>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Unity</span>
        <span class="proj-tag">Vuforia</span>
        <span class="proj-tag">C#</span>
        <span class="proj-tag">Android</span>
        <span class="proj-tag">Cloud Recognition</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">

          <h5>What it does</h5>
          <p>Visitors point their phone at a museum artifact; the app recognises the image against a Vuforia cloud database and overlays information boxes, video, or audio. Recognition and metadata are managed entirely through Vuforia&rsquo;s cloud target API, so new exhibits can be added without a re-build.</p>

          <h5>How it was built</h5>
          <p>Configured Unity with the Vuforia AR SDK and an AR Camera scene, wired up Cloud Recognition with Vuforia access keys, and handled metadata-driven media playback (mp4 / mp3 URLs) inside C# scripts. Navigated a series of Android build issues &mdash; SDK path mismatches, Gradle failures, and API-level mismatches &mdash; and documented every fix for the team.</p>

          <h5>Next steps (left for the team)</h5>
          <ul>
            <li>Responsive information box sizing across Android screen sizes</li>
            <li>Main menu screen and in-app exit button</li>
            <li>App Store distribution and visitor-facing setup poster</li>
          </ul>

          <p class="proj-team">Project Assistant &middot; Computer Museum, University of Waterloo &middot; Jun 2018&ndash;Jun 2019</p>
        </div>
      </details>
    </div>

  </div>

  <!-- ── SNU RUBIS LAB ─────────────────────────────────── -->
  <div class="proj-section">
    <div class="proj-section-label">Seoul National University &middot; 2020</div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div class="proj-card-title-block">
          <div class="proj-card-title">Autonomous Vehicle Research &mdash; RUBIS Lab</div>
          <div class="proj-card-sub">Remote lab infrastructure and CAN bus data handling for autonomous vehicle systems at Seoul National University&rsquo;s Real-Time Ubiquitous Systems Laboratory.</div>
        </div>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Docker</span>
        <span class="proj-tag">Bash</span>
        <span class="proj-tag">Python</span>
        <span class="proj-tag">VNC</span>
        <span class="proj-tag">CAN Bus</span>
        <span class="proj-tag">Autonomous Vehicles</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">

          <h5>Openlab</h5>
          <p>Built a Dockerfile to activate a VNC server on Ubuntu, enabling a browser-based GUI for remote users. Wrote bash scripts to automate the full autonomous vehicle launch sequence, and packaged them as a one-click desktop icon so operators could start and monitor vehicle status without touching the command line.</p>

          <h5>System</h5>
          <p>Worked on inter-module communication between the Application Processor (AP) and Multipoint Control Unit (MCU) over Ethernet. Wrote data handler scripts to pack and unpack Control Area Network (CAN) frames passing through the pipeline.</p>

          <h5>Demo</h5>
          <div class="proj-video-grid">
            <video controls preload="none" class="proj-video">
              <source src="{{ '/assets/video/output.mp4' | relative_url }}" type="video/mp4">
            </video>
            <video controls preload="none" class="proj-video">
              <source src="{{ '/assets/video/output2.mp4' | relative_url }}" type="video/mp4">
            </video>
          </div>

          <p class="proj-team">Research Intern &middot; RUBIS Lab, School of Computer Science and Engineering &middot; May&ndash;Jul 2020</p>
        </div>
      </details>
    </div>

  </div>
</div>

<style>
.projects-page { margin-top: 0.5rem; }
.proj-section { margin-bottom: 2rem; }
.proj-section-label {
  font-size: 0.7rem; font-weight: 600; letter-spacing: 0.08em;
  text-transform: uppercase; color: var(--global-text-color-light);
  padding-bottom: 0.6rem; margin-bottom: 0.85rem;
  border-bottom: 1px solid var(--global-divider-color);
}
.proj-card {
  border: 1px solid var(--global-divider-color); border-radius: 10px;
  padding: 1.25rem 1.4rem; margin-bottom: 0.85rem;
  background: var(--global-bg-color); transition: border-color 0.2s;
}
.proj-card:hover { border-color: var(--global-theme-color); }
.proj-card-header {
  display: flex; align-items: flex-start;
  justify-content: space-between; gap: 1rem; margin-bottom: 0.75rem;
}
.proj-card-title-block { flex: 1; min-width: 0; }
.proj-card-title { font-size: 1rem; font-weight: 600; color: var(--global-text-color); margin-bottom: 0.3rem; }
.proj-card-sub { font-size: 0.85rem; color: var(--global-text-color-light); line-height: 1.55; }
.proj-header-links { display: flex; flex-direction: column; gap: 0.35rem; flex-shrink: 0; align-items: flex-end; }
.proj-header-chip {
  font-size: 0.72rem; padding: 0.2rem 0.65rem; border-radius: 6px;
  border: 1px solid var(--global-divider-color); color: var(--global-text-color-light);
  text-decoration: none; white-space: nowrap; transition: border-color 0.15s, color 0.15s;
}
.proj-header-chip:hover { border-color: var(--global-theme-color); color: var(--global-theme-color); }
.proj-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 0.9rem; }
.proj-tag {
  font-size: 0.72rem; padding: 0.2rem 0.6rem; border-radius: 20px;
  background: var(--global-code-bg-color); color: var(--global-text-color-light);
  border: 1px solid var(--global-divider-color);
}
.proj-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.6rem; margin-bottom: 0.9rem; }
.proj-stat { background: var(--global-code-bg-color); border-radius: 8px; padding: 0.65rem 0.5rem; text-align: center; }
.proj-stat-num { display: block; font-size: 1.2rem; font-weight: 700; color: var(--global-theme-color); line-height: 1.1; }
.proj-stat-lbl { display: block; font-size: 0.68rem; color: var(--global-text-color-light); margin-top: 0.2rem; }
.proj-details summary {
  font-size: 0.8rem; color: var(--global-theme-color); cursor: pointer;
  list-style: none; display: inline-flex; align-items: center; gap: 0.3rem; user-select: none;
}
.proj-details summary::-webkit-details-marker { display: none; }
.proj-details summary::after { content: "↓"; font-size: 0.75rem; transition: transform 0.2s; }
.proj-details[open] summary::after { transform: rotate(180deg); }
.proj-details-body {
  margin-top: 1rem; padding-top: 1rem;
  border-top: 1px solid var(--global-divider-color);
  font-size: 0.875rem; color: var(--global-text-color); line-height: 1.65;
}
.proj-details-body blockquote {
  border-left: 3px solid var(--global-theme-color); padding-left: 0.85rem;
  margin: 0 0 0.85rem; color: var(--global-text-color-light); font-style: italic; border-radius: 0;
}
.proj-details-body h5 {
  font-size: 0.7rem; font-weight: 600; text-transform: uppercase;
  letter-spacing: 0.07em; color: var(--global-text-color-light); margin: 1rem 0 0.4rem;
}
.proj-details-body p { margin-bottom: 0.6rem; }
.proj-details-body ul { padding-left: 1.1rem; margin-bottom: 0.75rem; }
.proj-details-body ul li { margin-bottom: 0.35rem; }
.proj-video-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; margin: 0.5rem 0 0.75rem;
}
.proj-video {
  width: 100%; border-radius: 6px; border: 1px solid var(--global-divider-color);
}
@media (max-width: 480px) {
  .proj-video-grid { grid-template-columns: 1fr; }
}
.proj-team {
  font-size: 0.78rem; color: var(--global-text-color-light);
  margin-top: 0.85rem; padding-top: 0.75rem;
  border-top: 1px solid var(--global-divider-color);
}

/* ── BYOC Diagram ─────────────────────────── */
.byoc-diagram-wrap {
  margin: 0.75rem 0 1rem; border: 1px solid var(--global-divider-color);
  border-radius: 8px; padding: 0.75rem; background: var(--global-code-bg-color);
}
.byoc-diagram { width: 100%; height: auto; display: block; }
.byoc-diagram-caption {
  font-size: 0.72rem; color: var(--global-text-color-light);
  text-align: center; margin: 0.5rem 0 0; font-style: italic;
}
.byoc-box-blue-outer  { fill: none; stroke: #3b82f6; stroke-width: 1.5; stroke-dasharray: 5 3; }
.byoc-box-blue-inner  { fill: none; stroke: #60a5fa; stroke-width: 1; stroke-dasharray: 3 2; }
.byoc-box-workloads   { fill: rgba(59,130,246,0.07); stroke: #60a5fa; stroke-width: 0.75; }
.byoc-node-blue       { fill: #2563eb; }
.byoc-box-yellow      { fill: rgba(234,179,8,0.12); stroke: #ca8a04; stroke-width: 1.2; }
.byoc-node-yellow     { fill: rgba(234,179,8,0.25); stroke: #ca8a04; stroke-width: 0.5; }
.byoc-box-green-outer { fill: rgba(34,197,94,0.07); stroke: #16a34a; stroke-width: 1.5; stroke-dasharray: 5 3; }
.byoc-node-green      { fill: #15803d; }
.byoc-box-green-note  { fill: rgba(34,197,94,0.12); stroke: #16a34a; stroke-width: 0.75; }
.byoc-line            { stroke: #94a3b8; stroke-width: 1; fill: none; }
.byoc-arrow           { fill: #94a3b8; }
.byoc-label-outer       { font-size: 9px; fill: #60a5fa; font-weight: 600; text-anchor: start; }
.byoc-label-outer-green { font-size: 9px; fill: #4ade80; font-weight: 600; text-anchor: start; }
.byoc-label-inner       { font-size: 8px; fill: #93c5fd; font-weight: 500; text-anchor: start; }
.byoc-label-mid         { font-size: 9px; fill: #fbbf24; font-weight: 600; text-anchor: middle; }
.byoc-node-text         { font-size: 8px; fill: #ffffff; text-anchor: middle; dominant-baseline: middle; }
.byoc-node-text-dark    { font-size: 8px; fill: #78350f; text-anchor: middle; dominant-baseline: middle; }

@media (max-width: 480px) {
  .proj-card-header { flex-direction: column; gap: 0.5rem; }
  .proj-header-links { flex-direction: row; }
}
</style>
