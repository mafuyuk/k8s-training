$ kubectl apply -f ./

$ kubectl get deployments
$ kubectl get pods





# 出力時に特定のJSON PATHの値のみを出力
$ kubectl get pods sample-deployment-6cd85bd5f-lpktq -o jsonpath='{.metadata.labels}'

# 指定したラベルを持つPod情報のうち、指定のJSON Pathをカラムにして出力
$ kubectl get pods -l app=sample-app \
  -o custom-columns="NAME:{metadata.name},IP:{status.podIP}"  

# Serviceの確認  
$ kubectl get services sample-clusterip
$ kubectl describe svc sample-clusterip

# ClusterIPはクラスター内のpodからしかアクセスできないので 
$ kubectl run --image=centos6 --restart=Never --rm -i testpod \
  -- curl -s http://sample-clusterip:8080

# 削除
$ kubectl delete services sample-clusterip
$ kubectl delete deployments sample-deployment

