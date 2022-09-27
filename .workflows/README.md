# Workflows

This directory contains workflow to be running when push event on git.

---

## Naming convention

`*-workflow.yaml`

---

## Submit

```sh
argo submit ci-workflow.yaml \
  --name ci-$(head -c 512 /dev/urandom | tr -dc 'a-z0-9' | head -c 8) \
  --serviceaccount workflow \
  --watch
```

---
