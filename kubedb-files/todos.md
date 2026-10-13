# KubeDB on VKS — TODOs

## 1. Screenshots (add to the docx and `kubedb/images/`)
- [ ] Grafana "KubeDB / Postgres / Summary" for `demo/pg-ha` (ACE Grafana, `/grafana/d/Tg8xCwXDk/kubedb-postgres-summary`) → docx Figure 5, `4_POSTGRES_HA_VALIDATION.md` step 9
- [ ] Prometheus Targets filtered to `pg-ha-stats`, 6 targets UP (`kubectl port-forward -n monitoring svc/kube-prometheus-stack-prometheus 9090`, then `http://localhost:9090/targets?search=pg-ha`) → docx Figure 6
- [ ] Or ship text-only: the docx currently has Figures 1–4 only, which is acceptable
- [ ] vCenter screenshots for `1_CONFIGURE_SUPERVISOR.md` and Cloud Native Storage > Container Volumes: ask KK (our SSO user has limited rights), or ship text-only

## 2. Reference Architecture (Word)
- [ ] Confirm the footer "Item No: vmw-bc-wp-tech-uslet-word-2026; Sep-26" with KK
- [ ] Open the docx in Word, accept the "update fields" prompt (refreshes the TOC), check the layout (title/subtitle appears twice on pages 1–2: template cover or duplicate?), save
- [ ] Confirm product claims: "Courier" as the public product name; GA status of Oracle, Qdrant, Milvus, Weaviate; "more than 30" engines
- [ ] Decide: Figure 3 and the Supervisor-services text name Argo CD for GitOps, but our stack uses Flux; mention Flux?
- [ ] Confirm the license wording: one `license.txt` for KubeDB and KubeStash, `?p=kubedb` link
- [ ] Send to KK — VMware publishes it

## 3. `kubedb/` folder
- [ ] Add a "Cleanup Procedure" section to `3A_KUBEDB_PLATFORM_INSTALLER.md` (3B has one); needs the verified uninstall steps for the installer-managed HelmReleases
- [ ] Add the white paper URL to `kubedb/README.md` once VMware publishes the RA
- [ ] Share the folder with KK — VMware pushes it to vks-validated-solutions

## 4. Lab cluster (`appscode-c1`)
- [ ] Ask KK to resize the control plane (1× best-effort-medium ran at 94–97% memory, 109% on 2026-10-13; API server TLS handshake timeouts)

## 5. Broadcom TAP
- [ ] Register at https://tap.broadcom.com/home ("Register", top right), using Grant's guide
- [ ] Ask Grant: is TAP required for this validation, or a separate track?

## 6. Companion blog post
- [ ] Draft blog linking to the RA; share with VMware for cross-promotion
