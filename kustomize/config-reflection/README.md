# build
```bash
$ kubectl kustomize .
```

# 作成
```bash
$ kubectl apply -k .
```

# 削除
```bash
$ kubectl delete -k .
```

# 注意点
varsはリソース設定をPodにわたすことのみを目的としている

## 参考リンク
- https://kubectl.docs.kubernetes.io/pages/app_customization/config_reflection.html