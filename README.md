Install SUSE Observability Agent GitHub Action
🛰️ Install SUSE Observability Agent

A GitHub Action that installs or upgrades the SUSE Observability Agent on any Kubernetes cluster using Helm, with support for custom namespace, chart versioning, repo configuration, and TLS options.

This action simplifies deployment by automatically:
✔️ Ensuring the namespace exists
✔️ Adding the correct Helm repo
✔️ Installing or upgrading the SUSE Observability Agent chart
✔️ Passing required StackState values
✔️ Handling latest/specific chart versions

🚀 Features

🔧 Automatic namespace creation

📦 Helm repo auto-add + update

🆕 Install or upgrade SUSE Observability Agent

🔐 Secret-friendly API key handling

📌 Optional chart version pinning

⚙️ Configurable TLS skip options

🧩 Works with any Kubernetes cluster (RKE2, K3s, EKS, AKS, GKE, etc.)

📥 Inputs
Input Name	Required	Default	Description
stackstate_API_Key	✅ Yes	—	StackState API key (use secrets).
stackstateClusterName	✅ Yes	—	Logical name of the observed Kubernetes cluster.
stackstate_URL	✅ Yes	—	SUSE Observability receiver endpoint URL.
Namespace	❌ No	suse-observability	Namespace where the agent will be installed.
HelmRepo	❌ No	https://charts.rancher.com/server-charts/prime/suse-observability	Helm repo URL.
ChartName	❌ No	suse-observability/suse-observability-agent	Helm chart reference.
ChartVersion	❌ No	empty	Specific chart version. If empty → latest version installed.
NodeagentskipTLSVerify	❌ No	true	Sets nodeAgent.skipKubeletTLSVerify.
GlobalskipSslValidation	❌ No	false	Sets global.skipSslValidation.