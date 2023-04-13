# gitops-kodlunch

Kodlunch om GitOps.

## SSH-nycklar

[Deploy Keys](https://github.com/Iteam1337/gitops-kodlunch/settings/keys)

## Bootstrap

```shell
flux bootstrap github --components-extra=image-reflector-controller,image-automation-controller --owner=iteam1337 --repository=gitops-kodlunch --branch=main --path=./clusters/demo --personal
```
