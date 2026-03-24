---
layout: page
title: Projects
permalink: /work/
description: Things I've built — at school, at work, and on the side.
nav: true
nav_order: 3
---

<div class="projects-page">

  <div class="proj-section">
    <div class="proj-section-label">Academic &middot; 2025</div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div>
          <div class="proj-card-title">fAI &mdash; Fair AI Hiring</div>
          <div class="proj-card-sub">Adversarial debiasing system to detect and reduce gender bias in AI-powered resume screening. Tested on 27 professions.</div>
        </div>
        <span class="proj-badge proj-badge-blue">Demo Day 2025</span>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">PyTorch</span>
        <span class="proj-tag">Adversarial ML</span>
        <span class="proj-tag">Fairness</span>
        <span class="proj-tag">Python</span>
        <span class="proj-tag">React</span>
      </div>

      <div class="proj-stats">
        <div class="proj-stat"><span class="proj-stat-num">−23%</span><span class="proj-stat-lbl">gender bias</span></div>
        <div class="proj-stat"><span class="proj-stat-num">&lt;2%</span><span class="proj-stat-lbl">accuracy lost</span></div>
        <div class="proj-stat"><span class="proj-stat-num">27</span><span class="proj-stat-lbl">professions tested</span></div>
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
          <p>Hiring teams upload their screening model &rarr; audit using Equal Opportunity and Equalized Odds metrics &rarr; debias via the adversarial pipeline &rarr; earn a Fair AI badge. Compliant with PIPEDA, CHRA, and the EU AI Act. Humans always make the final call.</p>

          <div class="proj-links">
            <a href="{{ '/assets/pdf/fai_slides.pdf' | relative_url }}" target="_blank" rel="noopener">Slides (PDF) ↗</a>
          </div>

          <p class="proj-team">Kina Kim, Fatima Masood, Shuting Xie, Iman Cheema, Aaina Garg &middot; Demo Day 2025</p>
        </div>
      </details>
    </div>
  </div>

  <div class="proj-section">
    <div class="proj-section-label">IBM &middot; Current</div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div>
          <div class="proj-card-title">Db2 as a Service &mdash; BYOC on Azure</div>
          <div class="proj-card-sub">IBM Db2 SaaS deployed inside the customer&rsquo;s own Azure VPC &mdash; IBM manages the full service lifecycle while customers retain ownership of their data, security posture, and cloud infrastructure.</div>
        </div>
        <span class="proj-badge proj-badge-gray">GA June 2025</span>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Go</span>
        <span class="proj-tag">IBM Cloud</span>
        <span class="proj-tag">Azure</span>
        <span class="proj-tag">CI/CD pipelines</span>
        <span class="proj-tag">Db2</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">
          <h5>What I worked on</h5>
          <p>I work on the cloud pipelines that deploy, operate, and monitor Db2 instances running inside customer Azure VPCs at scale &mdash; building toward zero manual intervention and reducing pipeline failures.</p>

          <h5>What the product does</h5>
          <ul>
            <li><strong>Compliance controls</strong> &mdash; database runs inside the customer&rsquo;s own VPC, meeting the strictest data sovereignty requirements</li>
            <li><strong>Independent scaling</strong> &mdash; compute and storage scale separately; auto-increase ensures customers never run out of storage</li>
            <li><strong>High availability</strong> &mdash; 2-node setup across 2 availability zones with automated failover</li>
            <li><strong>Data co-location</strong> &mdash; keeps data within the customer&rsquo;s Azure account, right next to their apps and resources</li>
          </ul>

          <div class="proj-links">
            <a href="https://www.ibm.com/new/announcements/ibm-db2-and-db2-warehouse-saas-on-azure-byoc" target="_blank" rel="noopener">Announcement ↗</a>
            <a href="https://cloud.ibm.com/apidocs/db2-on-cloud-byoc" target="_blank" rel="noopener">API docs ↗</a>
          </div>
        </div>
      </details>
    </div>

    <div class="proj-card">
      <div class="proj-card-header">
        <div>
          <div class="proj-card-title">Db2 as a Service (IBM Cloud)</div>
          <div class="proj-card-sub">IBM&rsquo;s fully managed relational database for mission-critical OLTP workloads &mdash; high availability, automated backups, built-in ML capabilities, and enterprise-grade security on IBM Cloud and AWS.</div>
        </div>
        <span class="proj-badge proj-badge-gray">IBM Cloud</span>
      </div>

      <div class="proj-tags">
        <span class="proj-tag">Go</span>
        <span class="proj-tag">IBM Cloud</span>
        <span class="proj-tag">Python</span>
        <span class="proj-tag">Anomaly detection</span>
        <span class="proj-tag">Db2</span>
      </div>

      <details class="proj-details">
        <summary>Read more</summary>
        <div class="proj-details-body">
          <h5>What I worked on</h5>
          <p>Developed ML-based anomaly detection to identify irregular patterns in Db2 commands &mdash; catching issues before they surface as customer-facing failures. Also enhanced system reliability and maintained cloud pipelines supporting Db2 on Cloud operations.</p>

          <h5>What the product does</h5>
          <ul>
            <li><strong>Blazing-fast engine</strong> &mdash; IBM BLU Acceleration and advanced query optimizations from IBM Research for OLTP workloads</li>
            <li><strong>Elastic scaling</strong> &mdash; independently scale compute and storage via UI or REST API</li>
            <li><strong>Built-in ML</strong> &mdash; train and run ML models directly in the Db2 engine using SQL, Python, or R</li>
            <li><strong>Fully managed</strong> &mdash; automated monitoring, failovers, and geo-replicated disaster recovery backups</li>
          </ul>

          <div class="proj-links">
            <a href="https://www.ibm.com/docs/en/db2-as-a-service?topic=overview" target="_blank" rel="noopener">Docs ↗</a>
          </div>
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
.proj-card-title { font-size: 1rem; font-weight: 600; color: var(--global-text-color); margin-bottom: 0.3rem; }
.proj-card-sub { font-size: 0.85rem; color: var(--global-text-color-light); line-height: 1.55; }
.proj-badge {
  font-size: 0.7rem; padding: 0.2rem 0.6rem; border-radius: 20px;
  white-space: nowrap; flex-shrink: 0; font-weight: 500;
}
.proj-badge-blue {
  background: rgba(70, 130, 180, 0.1); color: var(--global-theme-color);
  border: 1px solid rgba(70, 130, 180, 0.25);
}
.proj-badge-gray {
  background: var(--global-code-bg-color); color: var(--global-text-color-light);
  border: 1px solid var(--global-divider-color);
}
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
.proj-links {
  display: flex; gap: 0.6rem; flex-wrap: wrap;
  margin-top: 0.85rem; padding-top: 0.85rem;
  border-top: 1px solid var(--global-divider-color);
}
.proj-links a {
  font-size: 0.78rem; padding: 0.25rem 0.7rem; border-radius: 6px;
  border: 1px solid var(--global-divider-color); color: var(--global-text-color-light);
  text-decoration: none; transition: border-color 0.15s, color 0.15s;
}
.proj-links a:hover { border-color: var(--global-theme-color); color: var(--global-theme-color); }
.proj-team {
  font-size: 0.78rem; color: var(--global-text-color-light);
  margin-top: 0.85rem; padding-top: 0.75rem;
  border-top: 1px solid var(--global-divider-color);
}
@media (max-width: 480px) {
  .proj-card-header { flex-direction: column; gap: 0.5rem; }
  .proj-badge { align-self: flex-start; }
}
</style>
