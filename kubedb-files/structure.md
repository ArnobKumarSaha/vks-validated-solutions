# KubeDB_on_VKS_Reference_Architecture.docx — Structure

The doc is a VMware-style reference architecture with four main sections. The single-row tables in the docx are code blocks, so they are listed as code below.

```
Title page: "KubeDB on vSphere Kubernetes Service on VMware Cloud Foundation" (+ cover image)
Contents (TOC)

1. Executive Summary
2. vSphere Kubernetes Service              — what VKS is (+ image)
   └ KubeDB by AppsCode                    — table (24 rows): "VKS provides" vs "KubeDB adds" (+ image)
3. Solution Architecture                   — 2 diagrams + component/version table (9 rows)
   ├ VKS Cluster Configuration             — config table (15) + vks-cluster.yaml (CAPI Cluster, VKS 3.7 / v1.36.2)
   ├ Storage Design                        — table: workload → vSAN policy → StorageClass (15)
   ├ Networking Design
   ├ High Availability and Placement
   ├ Security and Multi-Tenancy
   ├ Data Protection and DR                — table: layer/tool/what it protects (15)
   ├ Monitoring and Day-2 Operations
   ├ Onboarding Existing Databases
   └ Kubernetes Packages                   — big package/version table (54 rows)
4. Solution Validation                     — hands-on walkthrough
   ├ Install KubeDB on VKS                 — vcf context login → storageclass → cluster UID (for the license)
   │                                         → helmreleases → helm install kubedb v2026.10.12 → verify pods
   ├ Deploy HA PostgreSQL                  — namespace + TLS cert → pg-ha.yaml → apply/watch
   └ Validate KubeDB on VKS                — status, PVCs, auth secret, failover (delete pg-ha-0),
                                             PostgresOpsRequest, S3 backup (KubeStash), test matrix (21 rows)
5. Conclusion
```

## Notes

- **What vs. how:** sections 1–3 explain the design and the reasoning behind it. Section 4 is the runnable procedure.
- **Tables to check first:** "KubeDB adds" (24 rows), Kubernetes Packages (54 rows) and the validation test matrix (21 rows).
- **Images:** there are 13 in `word/media/`. Three of them (`kubedb_platform.png`, `kubedb_fig2.png`, `kubedb_fig3.png`) look like KubeDB's own figures, judging by their names. The rest appear to be VMware template images [inferred].
