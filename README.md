# GitOps Demo Repository

This repository demonstrates a scalable GitOps structure for managing hub infrastructure and tenant resources across multiple sites using Argo CD, Helm, and hierarchical values.

## Repository Structure

- `/global-values/`: Global configurations shared across all sites and clusters.
- `/sites/`: Site-specific configurations, including hub and tenant customizations.
- `/hub-infrastructure-chart/`: Helm chart for managing hub infrastructure (e.g., namespaces, operators, MCPs, ICSPs).
- `/tenant-chart/`: Helm chart for tenant-specific resources (e.g., HostedControlPlane, NodePools).
- `/application-sets/`: Argo CD ApplicationSets for dynamic management of resources.

## Key Features

- **Hierarchical Values System**: Supports global, site-specific, and cluster-specific overrides.
- **Dynamic Resource Management**: Uses Argo CD to manage resources declaratively.
- **Modularity**: Separate Helm charts for hub infrastructure and tenant resources.

## Usage

1. Clone the repository.
2. Deploy Argo CD in your Kubernetes environment.
3. Apply the ApplicationSets from `/application-sets/`.
4. Explore the hierarchical configurations for different sites and clusters.

