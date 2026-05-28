# 30 Days Kubernetes Roadmap (Hindi)

यह roadmap beginner से job-ready practical level तक जाने के लिए बनाया गया है।  
हर दिन 60-90 मिनट दो: 30% theory + 70% hands-on.

---

## Week 1: Core Basics (Pod, Deployment, Service, Ingress)

### Day 1
- Kubernetes architecture basics: Node, Pod, Deployment, Service
- Command practice: `kubectl get`, `kubectl describe`, `kubectl logs`
- Task: Nginx deployment run करो

### Day 2
- Pod lifecycle समझो (`Pending`, `Running`, `CrashLoopBackOff`)
- Task: गलत image देकर error reproduce करो और fix करो

### Day 3
- Deployment and ReplicaSet relation
- Task: replicas 1 से 3 करो और verify करो

### Day 4
- Service types: `ClusterIP`, `NodePort`, `LoadBalancer`
- Task: same app को `NodePort` से access करो

### Day 5
- Labels and selectors
- Task: 2 deployments बनाओ और selectors से correct service mapping करो

### Day 6
- Ingress basics (host/path based routing)
- Task: `nginx.local` से ingress route setup करो

### Day 7 (Revision Day)
- Week 1 का mini test:
  - fresh cluster में deployment + service + ingress setup from scratch

---

## Week 2: Production Basics (Config, Health, Resources, Rollout)

### Day 8
- ConfigMap basics
- Task: app config ConfigMap से inject करो

### Day 9
- Secret basics
- Task: Secret create करके env var में mount करो

### Day 10
- Probes: `livenessProbe`, `readinessProbe`
- Task: deployment में probes add करो

### Day 11
- Resource requests/limits
- Task: nginx deployment में CPU/memory requests+limits add करो

### Day 12
- Rolling update and rollback
- Task: image update करो, फिर rollback करो

### Day 13
- Namespaces and quotas basics
- Task: `dev` namespace बनाकर app deploy करो

### Day 14 (Revision Day)
- Week 2 mini project:
  - deployment + service + ingress + configmap + secret + probes + resources

---

## Week 3: Scale, Storage, Observability

### Day 15
- HPA (Horizontal Pod Autoscaler) concept
- Task: metrics server enable करके HPA apply करो

### Day 16
- Load testing basics
- Task: `hey`/`ab` या curl loop से traffic generate करो और HPA behavior observe करो

### Day 17
- PersistentVolume (PV) and PersistentVolumeClaim (PVC)
- Task: simple app + PVC attach करके data persistence test करो

### Day 18
- StatefulSet concept (high level)
- Task: basic StatefulSet demo run करो

### Day 19
- Logs collection basics
- Task: app logs filter and troubleshoot practice

### Day 20
- Monitoring basics (Prometheus/Grafana intro)
- Task: metrics देखो (CPU/Memory/Pod restarts)

### Day 21 (Revision Day)
- Incident drill:
  - Pod crash
  - Bad config
  - Service not reachable
  - Fix using kubectl debugging

---

## Week 4: Production and Company Readiness

### Day 22
- Helm basics
- Task: nginx Helm chart install/uninstall/upgrade

### Day 23
- Kustomize basics
- Task: dev/prod overlays create करो

### Day 24
- CI/CD intro (GitHub Actions/GitLab/Jenkins)
- Task: simple pipeline बनाओ जो image build + deploy करे

### Day 25
- Security basics: RBAC, service account, least privilege
- Task: namespace user permissions सीमित करो

### Day 26
- NetworkPolicy basics
- Task: allow/deny traffic policy demo

### Day 27
- TLS + DNS + Ingress production pattern
- Task: HTTPS ingress flow समझो (cert-manager overview)

### Day 28
- Cloud Kubernetes intro (EKS/GKE/AKS differences)
- Task: one cloud provider docs read + notes

### Day 29
- Resume-ready mini project build
- Task: multi-tier app (frontend + backend) with ingress and autoscaling

### Day 30 (Final Day)
- Mock interview + debugging round
- Task:
  - broken manifest fix
  - rollout failure recover
  - explain architecture in simple words

---

## Daily Command Checklist

हर दिन यह commands run करो:

```bash
kubectl get pods -A
kubectl get svc -A
kubectl get ingress -A
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

---

## Portfolio Tasks (GitHub पर डालने के लिए)

1. Nginx basic deployment project  
2. Ingress host/path routing demo  
3. ConfigMap + Secret + probes project  
4. HPA autoscaling demo with load test  
5. Helm/Kustomize based environment deployment

---

## Interview Readiness Target

इस roadmap के बाद आप यह confidently explain कर पाओ:
- Pod vs Deployment vs Service vs Ingress
- Why readiness/liveness matter
- Why requests/limits required in production
- How rollback works
- Basic troubleshooting flow

---

अगर चाहो, next step में मैं इसी roadmap का **Day 1 to Day 7 exact commands pack** भी बना दूँ (`week1-commands.md`) ताकि आप copy-paste करके practice कर सको।
