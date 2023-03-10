# LDAP

## Question: 

- LDAP 개념에 대해, 자꾸 까먹는 것 같아. 기억에 쉽게 남도록 예시를 들어 설명 부탁해

<br>

## Answer:

- LDAP는 Lightweight Directory Access Protocol의 약자로, 인터넷에서 사용되는 디렉토리 서비스 프로토콜입니다. LDAP는 네트워크 상의 여러 대의 컴퓨터에서 사용자 정보, 그룹 정보, 디렉토리 정보 등을 중앙 집중적으로 관리할 수 있도록 해줍니다.

<br>

- 이를 예시로 설명해보겠습니다. 예를 들어, 한 회사에서는 수백 명의 직원들이 각각의 컴퓨터에 로그인하여 업무를 수행하고 있습니다. 이 때, 각 컴퓨터에서는 로그인에 필요한 사용자 이름과 암호 등의 정보를 로컬하게 관리하고 있을 경우, 매번 새로운 직원이 입사하거나 기존 직원이 퇴사하는 등의 경우마다 모든 컴퓨터에서 사용자 정보를 일일이 수정해줘야 합니다.

- 하지만 LDAP를 이용하면, 모든 컴퓨터에서 사용자 정보를 중앙 집중적으로 관리할 수 있습니다. 예를 들어, 모든 사용자 정보를 하나의 LDAP 서버에 저장하고, 각 컴퓨터에서는 이 LDAP 서버에 접근하여 로그인에 필요한 정보를 가져올 수 있습니다. 이렇게 하면 새로운 직원이 입사하거나 기존 직원이 퇴사하는 경우에도, 단 한 군데에서만 사용자 정보를 수정하면 됩니다.

<br>

- 또 다른 예시로, LDAP는 이메일 서비스에서도 사용됩니다. 이메일 주소와 관련된 정보들(이름, 소속, 부서 등)을 LDAP 서버에 저장해두고, 이 정보를 이용하여 이메일 주소록을 만들거나 이메일 발송 시 수신자 정보를 가져올 수 있습니다.

<br>

- 이렇게 LDAP는 중앙 집중적인 디렉토리 서비스를 제공하여, 네트워크 상의 여러 대의 컴퓨터나 서비스에서 사용자 정보나 디렉토리 정보를 일관성 있게 관리할 수 있도록 도와줍니다.

<br>