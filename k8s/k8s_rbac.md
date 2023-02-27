## 쿠버네티스 환경에서 rbac에 대한 설명 및 사용 사례를 알려줘

- Kubernetes에서 RBAC(Role-Based Access Control)은 클러스터 내에서의 인증과 인가를 관리하는 중요한 기능입니다. 이를 통해 Kubernetes의 모든 리소스, 예를 들어 Pod, Service, Deployment, ConfigMap, Secret 등에 대한 접근 권한을 정확하게 제어할 수 있습니다.

- Kubernetes에서 RBAC는 사용자, 그룹 및 서비스 계정에 대한 역할(Role)과 권한(Binding)을 사용하여 구현됩니다. 이를 통해 특정 사용자나 그룹이 특정 리소스나 기능에 대한 권한을 가지도록 할 수 있습니다. RBAC 규칙은 Kubernetes API 서버에서 관리되며, kube-apiserver는 인증 후 이를 검증하여 권한을 제공합니다.

- 예를 들어, 개발팀의 일부 구성원이 특정 네임스페이스에 있는 Pod를 만들고 삭제할 수 있도록 권한을 부여하려면, 다음과 같은 방법으로 RBAC를 구성할 수 있습니다.


<br>

1. 역할(Role) 생성

```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  name: pod-manager
  namespace: development
rules:
- apiGroups: [""]
  resources: ["pods"]
  verbs: ["create", "delete"]

```

<br>


- 이 RBAC 정책은 development 네임스페이스에서 pods 리소스에 대한 create 및 delete 작업을 수행할 수 있는 pod-manager 역할을 정의합니다.

<br>

2. 바인딩(Binding) 생성

```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: pod-manager-binding
  namespace: development
subjects:
- kind: Group
  name: dev-team
  apiGroup: rbac.authorization.k8s.io
roleRef:
  kind: Role
  name: pod-manager
  apiGroup: rbac.authorization.k8s.io
```

<br>

- 이 RBAC 정책은 dev-team 그룹에 pod-manager 역할을 할당하여, 해당 그룹의 사용자가 development 네임스페이스에서 pods 리소스에 대한 create 및 delete 작업을 수행할 수 있도록 합니다.

- 이와 같은 방법으로, Kubernetes에서 RBAC를 사용하여 권한을 구성할 수 있습니다. RBAC의 사용 사례로는 보안 강화, 권한 분리, 권한 부여 등이 있습니다. 이를 통해 Kubernetes 클러스터의 보안을 강화하고, 리소스에 대한 접근 권한을 제한하여 안정성을 확보할 수 있습니다.
