# AWS AMP AMG 이슈사항에 대한 질문

## Question: 

- AWS의 EKS 환경에 aws managed prometheus를 managed grafana에 연결했고 data source 까지 confirm 되었는데 grafana에서 explore를 했을 때, 사용가능한 메트릭이 없다.
- 해결책은 무엇인가

<br>

## Answer

- 만약 AWS의 EKS 환경에 aws managed prometheus를 managed grafana에 연결했고 data source까지 confirm 되었는데 grafana에서 explore를 했을 때, 사용가능한 메트릭이 없다면 다음과 같은 해결책을 시도해 볼 수 있습니다.

<br>

1. Prometheus 레이블을 확인합니다.

- Prometheus는 레이블 기반의 메트릭을 사용합니다. 따라서 Grafana에서 Prometheus 데이터 소스를 구성할 때 Prometheus 서버의 레이블을 포함하여 쿼리를 작성해야 합니다.
- 레이블을 올바르게 지정하지 않으면 쿼리 결과가 표시되지 않을 수 있습니다.

<br>

2. Prometheus 서버와 Grafana 사이의 네트워크 연결을 확인합니다.

- 데이터 소스가 연결되었지만 Grafana에서 데이터를 수신하지 못할 수 있습니다. 
- 이 경우 네트워크 연결을 확인하고 연결 문제가 있는 경우 해당 문제를 해결해야 합니다.

<br>

3. Prometheus 서버에 적절한 권한이 있는지 확인합니다.

- Prometheus 서버에 액세스하는 데 필요한 권한이 AWS IAM 정책에 제대로 구성되어 있는지 확인합니다.

<br>

4. Prometheus 서버가 적절한 메트릭을 수집하고 저장하는지 확인합니다.

- Prometheus 서버가 수집하는 메트릭이 올바른지 확인합니다. 또한 저장소에 데이터가 저장되는지 확인합니다.

<br>

5. 쿼리 문법을 확인합니다.

- Grafana에서 작성한 쿼리의 구문이 올바른지 확인합니다. 쿼리에 문제가 있는 경우 쿼리를 수정하고 다시 실행해야 합니다.

<br>

위의 해결책들 중에서 문제를 해결할 수 있는 것을 시도해보시기 바랍니다.