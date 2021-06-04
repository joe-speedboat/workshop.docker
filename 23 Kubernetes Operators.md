
Kubernetes operators are a big step into this direction, since the migration of Docker applications into new versions needed often some attention. Operators are containerized system administrators that maintain a kind of workload.
This might be `prometheus` (which initially developed the operator concept).
`AWX` which is the OpenSource Version of the Ansible Tower.
Operators are the answer to missing kubernetes know-how and the leak of system administrators.
If you look into a running OpenShift cluster you can get an idea of where we will end:
```
[chris@control(wiki/system:admin) ~]☯ oc get clusteroperators.config.openshift.io
NAME                                       VERSION                         AVAILABLE   PROGRESSING   DEGRADED   SINCE
authentication                             4.7.0-0.okd-2021-05-22-050008   True        False         False      13h
baremetal                                  4.7.0-0.okd-2021-05-22-050008   True        False         False      95d
cloud-credential                           4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
cluster-autoscaler                         4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
config-operator                            4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
console                                    4.7.0-0.okd-2021-05-22-050008   True        False         False      9d
csi-snapshot-controller                    4.7.0-0.okd-2021-05-22-050008   True        False         False      17h
dns                                        4.7.0-0.okd-2021-05-22-050008   True        False         False      11d
etcd                                       4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
image-registry                             4.7.0-0.okd-2021-05-22-050008   True        False         False      9d
ingress                                    4.7.0-0.okd-2021-05-22-050008   True        False         False      117d
insights                                   4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
kube-apiserver                             4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
kube-controller-manager                    4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
kube-scheduler                             4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
kube-storage-version-migrator              4.7.0-0.okd-2021-05-22-050008   True        False         False      9h
machine-api                                4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
machine-approver                           4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
machine-config                             4.7.0-0.okd-2021-05-22-050008   True        False         False      15h
marketplace                                4.7.0-0.okd-2021-05-22-050008   True        False         False      9d
monitoring                                 4.7.0-0.okd-2021-05-22-050008   True        False         False      13h
network                                    4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
node-tuning                                4.7.0-0.okd-2021-05-22-050008   True        False         False      9d
openshift-apiserver                        4.7.0-0.okd-2021-05-22-050008   True        False         False      9h
openshift-controller-manager               4.7.0-0.okd-2021-05-22-050008   True        False         False      6d4h
openshift-samples                          4.7.0-0.okd-2021-05-22-050008   True        False         False      9d
operator-lifecycle-manager                 4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
operator-lifecycle-manager-catalog         4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
operator-lifecycle-manager-packageserver   4.7.0-0.okd-2021-05-22-050008   True        False         False      26h
service-ca                                 4.7.0-0.okd-2021-05-22-050008   True        False         False      283d
storage                                    4.7.0-0.okd-2021-05-22-050008   True        False         False      171d
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg5MDQ5NTYyNF19
-->