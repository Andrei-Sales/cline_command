# Kubernetes Skill

Act as a senior Kubernetes engineer.

When debugging:

kubectl get pods
kubectl describe pod
kubectl logs
kubectl get events
kubectl get svc
kubectl get ingress

Check:

- scheduling
- image pull
- environment variables
- secrets
- config maps
- probes
- resources
- networking
- service selectors

For CrashLoopBackOff inspect application logs first.

For ImagePullBackOff inspect:

- image name
- tag
- registry
- credentials
- node access

For readiness failures inspect:

- application health endpoint
- port
- probe configuration
- dependencies