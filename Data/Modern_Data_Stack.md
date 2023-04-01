# Modern Data Stack

## Question:

- Modern Data Stack 에 대해 설명해줘

<br>

## Answer:

- Modern Data Stack은 최신 데이터 파이프라인 아키텍처를 지칭하는 용어로, 데이터 엔지니어링에서 사용되는 기술 스택을 일컫습니다.
- Traditional Data Stack과는 달리 클라우드 기반의 모던한 아키텍처를 기반으로 합니다.

Modern Data Stack은 일반적으로 4개의 주요 구성 요소로 구성됩니다.

Extract, Transform, Load (ETL) / Extract, Load, Transform (ELT): 데이터를 추출하고, 필요한 형식으로 변환한 후, 데이터 웨어하우스 또는 데이터 레이크로 이동하는 작업을 담당합니다. 이를 위해서는 Apache Airflow, Apache Nifi, AWS Glue, Google Cloud Dataflow 등의 도구를 사용할 수 있습니다.

데이터 저장소(Data Warehouses/Lakes): 추출한 데이터를 저장하는 공간을 의미합니다. 데이터 레이크는 비정형 데이터를 저장하며, 데이터 웨어하우스는 정형 데이터를 저장합니다. Redshift, BigQuery, Snowflake 등의 클라우드 데이터베이스를 사용합니다.

Business Intelligence(BI) / 분석도구(Analytics): 데이터를 시각화하고, 분석하는 작업을 담당합니다. 이를 위해서는 Looker, Tableau, Power BI 등의 도구를 사용할 수 있습니다.

Data Engineering Tools: 데이터 엔지니어링 작업을 위한 도구로, 소스 제어, 데이터 검증, 작업 스케줄링 등을 포함합니다. Apache Spark, Apache Kafka, Apache Beam, DBT 등의 도구를 사용할 수 있습니다.

Modern Data Stack은 클라우드 기반의 서비스와 도구를 사용하기 때문에, 가볍고 확장 가능하며 유연한 아키텍처를 가지고 있습니다. 또한 비용이 저렴하며, 시간과 인력을 절약할 수 있습니다. 이러한 이점들로 인해, 최신 데이터 파이프라인을 구축하는 기업이 증가하고 있습니다.