# Pihole

## Generating configmap

```bash
kubectl -n pihole create configmap pihole-hosts --from-file=./configmap/
```
