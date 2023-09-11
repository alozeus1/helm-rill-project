# helm-rill-project
deploy statefulset application using helm chart


RILL-APP HELM CHART:

This Helm chart deploys the rill-app application to a Kubernetes cluster. The chart is meticulously designed to cater to different environments such as staging and production, ensuring smooth deployments across different stages of your development process.

FEATURES:

Stateful Application Deployment: Allows for stable, persistent storage.
Environment-Specific Configurations: Separate value files for different environments such as staging and production.
Node Specific Scheduling: Ensures pods are scheduled on nodes with specific labels.
Pod Anti-Affinity: Ensures optimal distribution of pods across nodes.
Pre-requisites
Kubernetes cluster (v1.16+ recommended).
Helm v3 installed on your local machine.
kubectl command-line tool configured to communicate with your cluster.
Quick Start
Clone the repository:

#bash
Copy code
git clone "https://github.com/alozeus1/helm-rill-project.git" && cd myrill-project
Deploy using the default values:

#bash
Copy code
helm install rill-app-release-name .
Deploy in a specific environment (e.g., staging):

#bash
Copy code
helm install -f values.stage.yaml rill-app-stage-release .
Configuration
This chart offers a multitude of configuration options. Check values.yaml for default configurations. For environment-specific overrides, refer to values.stage.yaml and values.prod.yaml.

KEY CONTRIBUTION:

Image: Adjust the application's image and tag.
Ephemeral Storage: Size of the ephemeral storage required for the application.
Persistent Volume: Configuration for persistent volume like size and storage class.
Node Selector: Ensures pods are scheduled on specific nodes.
Affinity: Set rules on which pods can be co-located on a node.
Environment Specific Deployments
You can maintain different configurations for various environments:

Staging: Use values.stage.yaml

#bash
Copy code
helm install -f values.stage.yaml rill-app-stage-release .
Production: Use values.prod.yaml

#bash
Copy code
helm install -f values.prod.yaml rill-app-prod-release .

CONTRIBUTION:

We appreciate your contributions! Please submit a pull request, and our maintainers will review your changes.

LICENSE:

This project is licensed under the MIT License. See the LICENSE file for more details.
