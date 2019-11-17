# Pihole

## Generating configmap

```bash
kubectl -n pihole create configmap pihole-hosts --from-file=./configmap/
```

## Custom hosts

Seems Pihole can now resolve them just fine:

```bash
nslookup traefik.local 192.168.0.11
```

However, stupid Sagem router inserts itself as DNS server to clients, instead of passing the configured DNS server. And for some reason, it doesn't seem to allow the query.