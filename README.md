My Kubernetes deployments

Every folder contains a kustomization which is deployed by Flux [flux].

[flux]: https://fluxcd.io/

# Installation

Setup server using [user-data](user-data.yaml)
Change root password (log in as root)

Install kube-config on local device (copy from `/root/kube-config` to `~/.kube/config`)

- Setup flux using private ssh key:
```bash
flux bootstrap git --url=ssh://git@github.com/rappet/kube-config.git --private-key-file flux_key  --path test
 ```