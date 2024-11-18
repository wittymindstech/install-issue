
Download [Openssl3.0.2](https://openssl-library.org/source/old/3.0/index.html) from this  [link](https://openssl.org/source/old/3.0/openssl-3.0.2.tar.gz)
Download tar.gz and extract it and $cd openssl-3.2.0

Also, run below commands to compile and install openssl in Mac

`./config`
`make`
`make test` 
`make install`



Add devcontainer in vscode since Mac have networking limitations.
Then, in VS Code Terminal

`make cluster`
`make install-crds`
`make install-minio`

`kubectl get svc --namespace minio -l app=minio`
NAME            TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
minio           LoadBalancer   10.96.220.171   <pending>     9000:31084/TCP   3m5s
minio-console   LoadBalancer   10.96.136.136   <pending>     9001:32555/TCP   3m5s



`kubectl port-forward -n minio service/minio-console 8443:9001`
Forwarding from 127.0.0.1:8443 -> 9001
