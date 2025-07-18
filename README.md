# DevOps_CI_CD
End-to-End CI/CD Pipeline with Kubernetes (GitOps) -


[Developer's Machine]
   |
   | (1) git push
   ↓
[Git Repository (GitHub/GitLab)] ←→ [CI Server (Jenkins/GitHub Actions)]
   |                                   |
   | (2) Triggers CI Pipeline          | (3) Build, Test, Package
   |                                   ↓
   |                         [Container Registry (Docker Hub/ECR)]
   |                                   |
   | (4) Updates Deployment Manifests  |
   ↓                                   |
[GitOps Repo (K8s Manifests)]          |
   |                                   |
   | (5) GitOps Controller Detects Change
   ↓
[Kubernetes Cluster]
   | (6) Synchronizes State
   ↓
[Running Application] → [Monitoring (Prometheus/Grafana)]
