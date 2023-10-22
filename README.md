# my-dissertation

# Effective Secrets Management in Kubernetes with HashiCorp Vault

Welcome to the Git repository for my dissertation project, "Effective Usage of Secrets Management in a Kubernetes Environment." This project explores the importance of securing sensitive information in a Kubernetes environment and demonstrates the use of HashiCorp Vault as a reliable solution.

## About HashiCorp Vault

HashiCorp Vault is a versatile and secure secret management solution designed for protecting, managing, and controlling access to sensitive data, such as credentials, API keys, and certificates. Here's why Vault is considered the best solution:

- **Centralized Management**: Vault provides a centralized platform for managing secrets and credentials across your infrastructure.

- **Dynamic Secrets**: It can generate and revoke dynamic secrets, reducing the risk of exposure.

- **Scalability**: Vault seamlessly scales with your applications and infrastructure, making it a great fit for Kubernetes.

- **Flexible Authentication**: It supports various authentication methods, including AppRole, LDAP, and more.

- **Auditing and Access Control**: Vault ensures detailed auditing and robust access control.

## Practical Implementation

In this project, we demonstrate the effective usage of HashiCorp Vault within a Kubernetes cluster using KIND (Kubernetes IN Docker).

### Directory Structure

- **Kubernetes Files**:
  - `Deployment.yaml`: HashiCorp Vault deployment configuration.
  - `k8s-role.yaml`: Kubernetes role for HashiCorp Vault.
  - `k8s-rolebinding.yaml`: Role binding for Kubernetes authentication.
  - `service.yaml`: Service configuration for HashiCorp Vault.
  - `persistent-volume.yaml`: Persistent volume configuration.
  - `persistent-volume-claims.yaml`: Persistent volume claims.

- **Sample Application Files**:
  - `sample-app-deployment.yaml`: Configuration for the sample application.
  - `service-account.yaml`: Service account for the sample application.

### Vault Configuration

Inside the HashiCorp Vault, the following configurations have been implemented:

- **KV Secret Engine**: Enabled to store secrets for the sample application. Key-Value (KV) secret engines allow you to manage and version secrets efficiently.

- **AppRole Authentication**: Utilized for the sample application to communicate with Vault securely. AppRole authentication is ideal for applications running in Kubernetes clusters.

### Accessing Secrets

Once the project is set up, you can access secrets within the Kubernetes cluster. For example, running the following command will display the username and password from your application's pod:

```shell
kubectl logs < application_pod_name >
