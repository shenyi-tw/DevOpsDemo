## all pods

```sh
k get pod -A
NAMESPACE            NAME                                                        READY   STATUS    RESTARTS         AGE
calico-system        calico-kube-controllers-5f99c5d58d-52b6r                    1/1     Running   0                77s
calico-system        calico-node-5frm9                                           1/1     Running   3 (118m ago)     20h
calico-system        calico-node-5xnfm                                           1/1     Running   3 (4h22m ago)    20h
calico-system        calico-node-j67cs                                           1/1     Running   1 (7h2m ago)     9h
calico-system        calico-node-qflpp                                           1/1     Running   5 (100m ago)     20h
calico-system        calico-typha-7849cb4c6c-t2894                               1/1     Running   0                87s
calico-system        calico-typha-7849cb4c6c-t4f8w                               1/1     Running   0                87s
istio-system         istio-ingressgateway-989467bf-h4kd5                         1/1     Running   0                4h8m
istio-system         istiod-9f9884bbb-dwgsk                                      1/1     Running   0                4h6m
istio-system         istiod-9f9884bbb-f9kfq                                      1/1     Running   0                53s
kube-system          cloud-controller-manager-rke2-cp1                           1/1     Running   27 (117m ago)    27h
kube-system          cloud-controller-manager-rke2-cp2                           1/1     Running   16 (100m ago)    21h
kube-system          cloud-controller-manager-rke2-cp3                           1/1     Running   7 (4h21m ago)    21h
kube-system          etcd-rke2-cp1                                               1/1     Running   10               27h
kube-system          etcd-rke2-cp2                                               1/1     Running   6                21h
kube-system          etcd-rke2-cp3                                               1/1     Running   5                21h
kube-system          kube-apiserver-rke2-cp1                                     1/1     Running   5                27h
kube-system          kube-apiserver-rke2-cp2                                     1/1     Running   10               21h
kube-system          kube-apiserver-rke2-cp3                                     1/1     Running   4 (4h22m ago)    21h
kube-system          kube-controller-manager-rke2-cp1                            1/1     Running   25 (117m ago)    27h
kube-system          kube-controller-manager-rke2-cp2                            1/1     Running   14 (100m ago)    21h
kube-system          kube-controller-manager-rke2-cp3                            1/1     Running   8 (4h21m ago)    21h
kube-system          kube-proxy-rke2-cp1                                         1/1     Running   4 (118m ago)     27h
kube-system          kube-proxy-rke2-cp2                                         1/1     Running   5 (100m ago)     21h
kube-system          kube-proxy-rke2-cp3                                         1/1     Running   3 (4h22m ago)    21h
kube-system          kube-proxy-rke2-worker1                                     1/1     Running   0                7h2m
kube-system          kube-scheduler-rke2-cp1                                     1/1     Running   8 (118m ago)     27h
kube-system          kube-scheduler-rke2-cp2                                     1/1     Running   5 (100m ago)     21h
kube-system          kube-scheduler-rke2-cp3                                     1/1     Running   3 (4h22m ago)    21h
kube-system          rke2-coredns-rke2-coredns-6bb85f9dd8-mm5lw                  1/1     Running   0                109m
kube-system          rke2-coredns-rke2-coredns-6bb85f9dd8-wv8nr                  1/1     Running   0                3h16m
kube-system          rke2-coredns-rke2-coredns-autoscaler-7b9c797d64-tpqg4       1/1     Running   0                109m
kube-system          rke2-metrics-server-868fc8795f-2brqd                        1/1     Running   0                3h16m
kube-system          rke2-snapshot-controller-7dcf5d5b46-nrggl                   1/1     Running   0                3h16m
kube-system          rke2-snapshot-validation-webhook-bf7bbd6fc-cvsdd            1/1     Running   0                109m
local-path-storage   local-path-provisioner-79874bcbd9-zdpsd                     1/1     Running   0                4h27m
monitoring           alertmanager-kube-prometheus-stack-alertmanager-0           2/2     Running   0                4h8m
monitoring           kube-prometheus-stack-grafana-6f4b5f5594-s96c8              3/3     Running   0                170m
monitoring           kube-prometheus-stack-kube-state-metrics-75c8d49686-8mxr2   1/1     Running   1 (3h31m ago)    4h27m
monitoring           kube-prometheus-stack-operator-844b69b876-5fx9q             1/1     Running   0                4h27m
monitoring           kube-prometheus-stack-prometheus-node-exporter-8phz4        1/1     Running   1 (118m ago)     6h50m
monitoring           kube-prometheus-stack-prometheus-node-exporter-kv6cc        1/1     Running   4 (100m ago)     6h50m
monitoring           kube-prometheus-stack-prometheus-node-exporter-pjj88        1/1     Running   0                6h50m
monitoring           kube-prometheus-stack-prometheus-node-exporter-t4tqk        1/1     Running   1 (4h22m ago)    6h50m
monitoring           prometheus-kube-prometheus-stack-prometheus-0               2/2     Running   0                4h8m
observability        loki-0                                                      2/2     Running   0                4h8m
observability        loki-canary-fjl5z                                           1/1     Running   0                6h34m
observability        loki-chunks-cache-0                                         2/2     Running   0                4h9m
observability        loki-results-cache-0                                        2/2     Running   0                4h9m
observability        otel-collector-5d996c8d7c-q5kc6                             1/1     Running   0                4h27m
observability        promtail-8lmqp                                              1/1     Running   0                6h53m
observability        promtail-8mftx                                              1/1     Running   1 (118m ago)     6h53m
observability        promtail-mzktw                                              1/1     Running   3 (100m ago)     6h53m
observability        promtail-pfwnq                                              1/1     Running   1 (4h22m ago)    6h53m
observability        tempo-0                                                     1/1     Running   0                4h8m
security-demo-go     auth-check-5ddcb4fb55-x7665                                 2/2     Running   0                4h7m
security-demo-go     blog-gin-app-v1-578cc4b446-6899k                            2/2     Running   0                4h7m
security-demo-go     blog-gin-app-v2-7f987b78fd-h6qtz                            2/2     Running   1 (4h6m ago)     4h7m
security-demo-go     booking-service-9ffdf58b4-mhmxz                             2/2     Running   1 (4h6m ago)     4h8m
security-demo-go     ecpay-flask-app-cff98dc48-xfmwv                             2/2     Running   0                4h8m
security-demo-go     ecpay-helper-service-856c8cb5fb-q6xkn                       2/2     Running   1 (4h6m ago)     4h7m
security-demo-go     go-bff-service-5f56fb98bd-ddckd                             2/2     Running   1 (4h6m ago)     4h7m
security-demo-go     go-jwt-auth-service-57ddc86989-5mb42                        2/2     Running   1 (4h6m ago)     4h7m
security-demo-go     go-lib-service-7f479bb9bb-wvwqf                             2/2     Running   0                4h8m
security-demo-go     menu-service-7df645fdf8-mthvn                               2/2     Running   1 (4h7m ago)     4h8m
security-demo-go     mes-service-5c844ccf8c-j4jz8                                2/2     Running   1 (4h6m ago)     4h7m
security-demo-go     oauth-client-5b944d4d97-45fbg                               2/2     Running   11 (3h39m ago)   4h8m
security-demo-go     oauth-server-7d96cb97c6-qvd2m                               2/2     Running   1 (4h6m ago)     4h8m
security-demo-go     pubsub-service-57dbd4d67d-bdq7s                             3/3     Running   0                4h7m
security-demo-go     vue-my-app-7c45c87648-2bm8p                                 2/2     Running   0                4h8m
tigera-operator      tigera-operator-66dff64c48-42mqx                            1/1     Running   11 (114m ago)    27h
```