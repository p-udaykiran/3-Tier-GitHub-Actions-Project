<h1 align="center">🚀 3-Tier Application Deployment on Amazon EKS</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/cncf/artwork/master/projects/kubernetes/icon/color/kubernetes-icon-color.svg" alt="Kubernetes" width="70"/>
  <img src="https://www.svgrepo.com/show/448253/terraform.svg" alt="Terraform" width="70"/>
  <img src="https://icon.icepanel.io/AWS/svg/Containers/EKS-Cloud.svg" alt="Amazon EKS" width="70"/>
  <img src="https://raw.githubusercontent.com/gilbarbara/logos/de2c1f96ff6e74ea7ea979b43202e8d4b863c655/logos/github-actions.svg" alt="Github Action" width="70"/>
  <img src="https://www.svgrepo.com/show/448221/docker.svg" alt="Docker" width="70"/>
  <img src="https://www.svgrepo.com/show/452075/node-js.svg" alt="Node.js" width="70"/>
  <img src="https://www.svgrepo.com/show/331761/sql-database-sql-azure.svg" alt="Database" width="70"/>
</p>

<p align="center">
  <b>Automating CI/CD for a 3-Tier Node.js Application using GitHub Actions, Terraform & Amazon EKS</b><br>
  End-to-End Pipeline with Security Scans, Docker, Kubernetes, and Cloud-Native Deployment.
</p>

<hr>

<h2>📌 Project Overview</h2>
<p>
This repository demonstrates a <b>3-Tier Application</b> deployment (Frontend + Backend + Database) on <b>Amazon EKS</b> using <b>Terraform</b> and <b>GitHub Actions</b>.  
The pipeline includes:
</p>
<ul>
  <li>✔️ <b>CI Pipeline</b> → Node.js syntax checks, <b>Gitleaks</b>, <b>Trivy</b> scans, <b>SonarQube</b> analysis</li>
  <li>✔️ <b>CD Pipeline</b> → Docker image build & push → Image vulnerability scan → Deployment to EKS</li>
  <li>✔️ <b>Infrastructure</b> → Amazon EKS cluster provisioned with <b>Terraform</b></li>
</ul>

<hr>

<h2>⚡ Prerequisites</h2>
<ul>
  <li>AWS Account with IAM permissions</li>
  <li>Terraform Installed (<a href="https://developer.hashicorp.com/terraform/downloads">Download</a>)</li>
  <li>AWS CLI (<a href="https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html">Install</a>)</li>
  <li>kubectl (<a href="https://kubernetes.io/docs/tasks/tools/">Install</a>)</li>
  <li>DockerHub Account</li>
  <li>GitHub Repository with Actions enabled</li>
</ul>

<hr>

<h2>🛠️ CI/CD Pipeline Workflow</h2>

<h3>🔹 1. Continuous Integration (CI)</h3>
<ul>
  <li>✅ Syntax check for Frontend & Backend Node.js code</li>
  <li>✅ <b>Gitleaks</b> – Secret scanning</li>
  <li>✅ <b>Trivy</b> – File system vulnerability scan</li>
  <li>✅ <b>SonarQube</b> – Code quality & bug detection</li>
  <li>✅ Build & Push Docker images (Frontend & Backend)</li>
  <li>✅ <b>Trivy</b> – Docker image vulnerability scan</li>
</ul>

<h3>🔹 2. Continuous Delivery (CD)</h3>
<ul>
  <li>✅ Deploy application manifests to <b>Amazon EKS</b> (Frontend, Backend, MySQL, Ingress)</li>
</ul>

<hr>

<h2>🚀 GitHub Actions Workflow</h2>
<pre>
.github/workflows/node.js.yml
</pre>

<p>The workflow includes:</p>
<ol>
  <li>Node.js Compilation Check</li>
  <li>Gitleaks Secret Scanning</li>
  <li>Trivy Vulnerability Scans</li>
  <li>SonarQube Analysis</li>
  <li>Docker Build & Push</li>
  <li>Trivy Image Scanning</li>
  <li>Deployment to Amazon EKS</li>
</ol>

<hr>

<h2>📊 Project Structure</h2>
<pre>
├── api/                   # Backend Node.js code
│   ├── Dockerfile
│   └── ...
├── client/                # Frontend Node.js code
│   ├── Dockerfile
│   └── ...
├── k8s-prod/              # Kubernetes manifests
│   ├── sc.yaml            # Storage Class
│   ├── mysql.yaml         # MySQL Deployment & Service
│   ├── backend.yaml       # Backend Deployment & Service
│   ├── frontend.yaml      # Frontend Deployment & Service
│   ├── ci.yaml            # Config/Secrets
│   ├── ingress.yaml       # Ingress Controller
├── .github/workflows/     # GitHub Actions workflows
│   └── deploy.yml
└── README.md              # Documentation
</pre>

<hr>

<h2>✅ Verification</h2>
<pre>
# Check EKS nodes
kubectl get nodes

# Check deployed pods
kubectl get pods -n kube-system
kubectl get pods --all-namespaces

# Verify Ingress
kubectl get ingress
</pre>

<hr>

<h2>📌 Deployment Flow</h2>
<p align="center">
  <img src="https://raw.githubusercontent.com/p-udaykiran/3-Tier-GitHub-Actions-Project/refs/heads/main/client/public/workflow.png" alt="Pipeline Diagram"/>
</p>

<hr>

<h2>🙌 Contributing</h2>
<p>
Contributions are welcome! Feel free to open issues or submit pull requests for improvements, bug fixes, or additional features.
</p>
<p align="center"> <a href="https://www.linkedin.com/in/udaykiran-pagidimari-30275725a/">LinkedIn</a>
</p>
