# Deploy Mosquitto Message Broker with ConfigMap and Secret Volume Types

## Project Overview

This project demonstrates how to deploy the [Mosquitto](https://mosquitto.org/) MQTT message broker in a Kubernetes cluster while managing configuration and sensitive data securely using ConfigMap and Secret volume types.

## Technologies Used

- **Kubernetes**
- **Docker**
- **Mosquitto**

## Description

- Define and mount configuration data using Kubernetes **ConfigMap**.
- Define and mount sensitive data (passwords or certificates) using Kubernetes **Secret**.
- Deploy the Mosquitto message broker container with both ConfigMap and Secret volumes mounted into the container.

## Files Included

- `mosquitto.yaml`: Kubernetes Deployment manifest with ConfigMap and Secret volume mounts.
- `config-file.yaml`: ConfigMap definition containing Mosquitto configuration.
- `secret-file.yaml`: Secret definition containing sensitive information.
- `example-secret-certificate.yaml`: Example of a secret for certificates.
- `mosquitto-without-volumes.yaml`: Minimal Mosquitto deployment without volume mounts.

## How to Deploy

1. **Start Minikube or your Kubernetes cluster:**

   ```bash
   minikube start
   ```

2. **Apply the ConfigMap:**

   ```bash
   kubectl apply -f config-file.yaml
   ```

3. **Apply the Secret:**

   ```bash
   kubectl apply -f secret-file.yaml
   ```

4. **Deploy Mosquitto with volumes:**

   ```bash
   kubectl apply -f mosquitto.yaml
   ```

5. **Verify deployment:**

   ```bash
   kubectl get pods
   ```

## License

This project is shared for educational purposes.

---

## Author

GitHub: [shlaskin101](https://github.com/shlaskin101)
