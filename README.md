![Gokul Krishna V, DevOps and Platform Engineer](assets/hero.svg)

![whoami: Gokul Krishna V, DevOps and Platform Engineer, Bengaluru. 3+ years, GCP and AWS, GKE, Terraform, CI/CD, release automation, cloud migration. Open to work, available immediately.](assets/terminal.svg)

![Key numbers: 8-10 GKE releases a week, 100+ S3 buckets migrated with zero data loss, 100+ apps on one Jenkins pipeline, 50+ apps published](assets/metrics.svg)

## What I've built

![Platform CI/CD on GKE: git push or tag, Cloud Build, Artifact Registry, Cloud Deploy, dev, staging, manual approval, production](assets/pipeline-gke.svg)

<details>
<summary><b>How the GKE platform works</b></summary>

- Separate GCP projects for dev, staging, production and infra; the environment is chosen from the Git commit or tag; production only by Cloud Deploy promotion behind a manual approval.
- Cloud Build and Cloud Deploy pipelines with per-environment manifests; GKE infrastructure in Terraform.
- Secrets in Secret Manager, validated before every build and synced to Kubernetes; production secrets pre-synced during staging builds so promotions never ship stale values.
- Distributed deploy lock on Cloud Storage so concurrent deployments never collide.
- Images cached by commit SHA, cutting dev builds from minutes to seconds; dependency scanning and style checks as quality gates.
- Preview environments with automatic cleanup; Workload Identity, least-privilege IAM, HPA, liveness and readiness probes.

</details>

![AWS to GCP migration: S3 to Cloud Storage, CloudFront to Cloud CDN, Auto Scaling Groups to Managed Instance Groups, zero data loss](assets/migration.svg)

<details>
<summary><b>How the migration was done</b></summary>

- Copied S3 to Cloud Storage with gsutil and rsync, kept the transfer logs, scripted recovery of every object that failed to copy, and ran daily delta syncs until cutover.
- Replaced each CloudFront distribution with Cloud CDN, tracked old to new URLs in an inventory sheet and tested every URL for cache hits.
- Replaced Auto Scaling Groups with Managed Instance Groups from a custom VM image, running Docker images from Artifact Registry.

</details>

![Android release pipeline with Jenkins and Fastlane for 100+ apps: commit, build, test, sign, deploy, Google Play](assets/pipeline-android.svg)

<details>
<summary><b>More: iOS releases, AWS analytics and cost tracking</b></summary>

- **iOS release operations:** Apple Developer setup, certificates, provisioning profiles and push keys per app; Azure DevOps pipeline to TestFlight; App Review rejections handled through to approval; wrote the team's iOS launch runbook.
- **Platform analytics:** daily and monthly usage dashboard (Athena, Glue, QuickSight) for signups and daily active users.
- **Cost visibility:** daily AWS cost report email, then per-workload cost tracking with resource tags and a QuickSight dashboard.
- **Monitoring:** alerts and live dashboards on AWS and GCP that show what failed and exactly where.

</details>

## Tech stack

![Skills: Google Cloud (GKE, Cloud Build, Cloud Deploy, Compute Engine, Cloud Storage, Cloud CDN, Artifact Registry, Secret Manager, IAM, Workload Identity), AWS (S3, Lambda, CloudWatch, CloudFront, Route 53, Athena, Glue, QuickSight), CI/CD (Jenkins, Fastlane, Gradle, Azure DevOps, Git, GitHub), Kubernetes, Terraform, Docker, Linux, Python, Bash, SQL, App Store Connect, TestFlight, Google Play Console, Android, Firebase, code signing, alerting, dashboards, cost reporting, Jira](assets/tools.svg)

## Experience

| Role | Company | Period |
|---|---|---|
| DevOps Engineer | Learnyst | Jan 2025 - Aug 2026 |
| Mobile DevOps Engineer | Learnyst | Jul 2023 - Dec 2024 |

**Also:** mentored two junior engineers on app build and release, with knowledge-transfer sessions and step-by-step docs; the team's go-to for deployment and release issues.

**Education:** B.E. in Computer and Information Sciences, RNS Institute of Technology (2019 - 2023)

## Connect

[LinkedIn](https://www.linkedin.com/in/gokul-krishna-v-b5b237234/) · Open to DevOps, Platform, SRE and Cloud roles · Available immediately
