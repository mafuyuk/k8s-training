```bash
$ kctx docker-desktop
$ k apply -k fluxcd

# Deploy Keysに公開鍵を追加
$ fluxctl --k8s-fwd-ns flux identity
```

# 削除
```bash
$ k delete -k fluxcd
```

# 参考リンク
- https://dev.classmethod.jp/cloud/aws/eks-flux-with-kustomize-example-cd/