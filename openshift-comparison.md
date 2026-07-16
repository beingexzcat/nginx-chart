# Openshift and Kubernetes differences

| Kubernetes | OpenShift |
|---|---|
| Ingress and ingress controllers as API related | Redhat came up with this solution to present Routes based on HAProxy for the ingress which provides robustness of haproxy|
| Have to rely on external image registry | Uses a built-in native image registry, so customers do not need to configure on their own |
| Standard RBAC. But by default it lets pods run from dangerous root privileges | Has RBAC and SCC (Security Context Constraints) - blocks containers from running as root and forces containers to run as non-privileged users. Red Hat realised that this would be run by entrprises and it should be hardened enough from day one and encourage developers to build images which can run without root - since security is essence in big organizations |
| Monitoring requires installing Prometheus + Grafana separately | Has built-in Prometheus and Grafana, ready to use from day one |

