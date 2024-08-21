# Grafana-Monitoring-System

1. **Create Namespace:**

   First, create a namespace to organize all resources under a specific namespace:
   ```bash
   kubectl apply -f namespace.yaml
   ```
   
2. **Create Persistent Volume and Persistent Volume Claim:**

    Create Persistent Volume (PV) and Persistent Volume Claim (PVC) to persist Prometheus and Grafana data:
    ```bash
    kubectl apply -f pv-pvc.yaml
    ```

3. **Create ConfigMap:**

   Transfer Prometheus and Alertmanager configuration files to Kubernetes through ConfigMaps:
   ```bash
   kubectl apply -f configmaps.yaml
   ```
   
4. **Create Grafana Deployment and Service:**
   ```bash
    kubectl apply -f grafana.yaml
    ```
   
5. **Create Prometheus Deployment and Service:**
   ```bash
   kubectl apply -f prometheus.yaml
   ```
   
6. **Create Node Exporter Deployment and Service:**
   ```bash
   kubectl apply -f node-exporter-daemonset.yaml
   ```
   
7. **Create Alertmanager Deployment and Service:**
   ```bash
   kubectl apply -f alertmanager.yaml
   ```

## Verify the Results

You can run the following commands to test if the system is working.
 ```bash
 kubectl get pods -n monitoring
 kubectl get svc -n monitoring
 ```
