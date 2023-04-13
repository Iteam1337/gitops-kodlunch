# gitops-kodlunch

Kodlunch om GitOps.

## SSH-nycklar

[Deploy Keys](https://github.com/Iteam1337/gitops-kodlunch/settings/keys)

## Bootstrap

```shell
# Setup Flux.
flux bootstrap github --components-extra=image-reflector-controller,image-automation-controller --owner=iteam1337 --repository=gitops-kodlunch --branch=main --path=./clusters/demo --personal

# Create GIT secret.
flux create secret git git --url=ssh://git@github.com:22/iteam1337/gitops-kodlunch.git --private-key-file=./identity
```

## Monitor

```shell
flux get all -A --status-selector ready=false
```
