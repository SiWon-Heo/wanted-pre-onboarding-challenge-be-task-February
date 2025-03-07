1. 관계형 데이터베이스(RDBMS)와 비관계형 데이터베이스(NoSQL)의 장단점 비교

- RDBMS의 장점

  (1) 무결성 보존

  관계형 데이터베이스에 추가된 모든 데이터는 지정된 행렬의 스키마를 준수해야 합니다. 따라서 데이터 일관성, 무결성, 보안 및 규정 준수가 중요한 경우에 유용합니다. 또한 ACID 속성으로 인해 동기화와 트랜잭션의 유효성이 보장됩니다. 오류가 발생할 여지가 없기 때문에 금융 관련 프로그램 등 최고 수준의 데이터 무결성이 필요한 어플리케이션을 실행할 때 유용합니다.

  (2) 방대한 사용자 커뮤니티 

  SQL은 50년간 사용되어왔고, 여전히 많이 사용되고 있습니다. 의도하지 않은 결과물이 발생할 때 그에 대한 답을 찾기 쉽고, 기성 개발자와 쉽게 협업할 수 있다는 장점이 있습니다.

  (3) 쉬운 사용 난이도

  SQL은 비교적 유저 친화적이고, 간단한 키워드를 통해 사용할 수 있습니다.

- RDBMS의 단점

  (1) 부족한 확장성
  
  SQL 데이터베이스는 수직으로 확장하는 형태를 띄고, 용량을 늘리려면 저장공간을 늘리는 수 밖에 없습니다. 또한 데이터베이스가 커질수록 핸들링을 위해 더 많은 연산 자원이 필요합니다. 유지보수 및 운영비용도 당연히 많이 들 수 밖에 없습니다. 수평적 확장을 시도해볼 수는 있는데, 이 경우 데이터 파티셔닝이 필요하며 고도로 숙련된 개발자를 필요로 합니다. 

  (2) 정규화

  부족한 확장성 덕분에 SQL은 데이터 중복을 웬만하면 방지하려고 합니다. 여러 테이블의 정보를 조회하려면 join을 사용해 연결해서 쿼리합니다.하지만 이러한 과정은 데이터베이스가 커지면서 join 및 조회에 대한 작업을 느리게합니다.

  (3) 부족한 유연성

  SQL의 스키마는 매우 엄격합니다. 일단 한번 설계 후 배포하면 유연성이 떨어지고, 수정 작업은 어렵고 리소스 집약적인 편입니다. 그래서 관계형 데이터베이스는 운영하기 이전에 사전 계획에 상당한 시간을 투자해야 합니다. 따라서 모든 데이터가 이미 구조화되어 있고, 크기나 유형에서 큰 변화가 기대되지 않는 경우에만 적합합니다.

- NoSQL의 장점

  (1) 높은 가용성
  NoSQL 데이터베이스는 여러 서버에 데이터를 분산할 수 있습니다. 따라서 single point of failure에 보다 안전합니다. 
  
  (2) 높은 쿼리 속도
  NoSQL은 데이터 중복에 대해 RDBMS에 비해 포용적이며, 데이터 정규화를 하지 않기 때문에 특정 쿼리에 대한 모든 정보가 이미 함께 저장됩니다. 따라서 join이 필요하지 않고, 큰 데이터베이스에서의 조회가 쉽습니다. 또한 단순한 쿼리에 대해 매우 빠른 성능을 보여줍니다. 구조화된 데이터에 대해 매우 복잡한 쿼리도 지원 가능합니다. 물론 데이터베이스 크기와 join 조건이 증가하면 쿼리 속도 또한 그에 맞게 줄어들 것입니다.
  
  (3) 낮은 진입장벽
  관계형 데이터베이스는 사전 설계에 노력이 매우 많이 들어가야 하는 반면, NoSQL은 부담없이 데이터 유형과 필드를 추가할 수 있으며 시작 또한 쉽게 할 수 있습니다. 따라서 다양한 데이터 유형을 보유하고 있거나 지속적으로 새로운 기능을 추가할 프로그램에 대해 적합합니다. 
  
  (4) 수평적 확장
  내재적으로 여러 서버에 나뉘어 배포되기 때문에, 확장성이 제한되어 지속적으로 하드웨어를 업그레이드 해야하는 관계형 데이터베이스에 반해 NoSQL은 클라우드 인스턴스나 서버만 추가하면 저렴하게 확장이 가능합니다.
  
 - NoSQL의 단점
  
    (1) 표준화되지 않은 사용법
    RDBMS가 SQL을 갖는 것에 반해 NoSQL은 표준화된 쿼리 언어가 없습니다. SQL언어만 배우면 되는 관계형 데이터베이스에 반해 NoSQL은 학습의 난이도가 높은 편입니다. 또한 복잡한 형태의 NoSQL 데이터베이스에 복잡한 형태의 쿼리를 수행해야 할 때는 오히려 관계형 데이터베이스에 비해 기술적 노력이 많이 필요할 수 있습니다.
  
    (2) 작은 유저 규모
    아무래도 관계형 데이터베이스보다는 유저 풀이 작고 전문가가 적은 편입니다.
  
    (3) 부족한 일관성
    ACID 속성을 항상 보존하는 관계형 데이터베이스와는 달리 NoSQL은 항상 업데이트된, 정확한 데이터를 반환하는 것을 보장하지는 않습니다. 이는 분산 접근 방식을 사용하기 때문으로, 쿼리되는 서버에 따라 각기 다른 값을 동시에 반환받을 수 있기 때문입니다. 하지만 그 속도와 가용성이 이러한 부정확성을 극복할 정도로 매우 좋기 때문에 조건을 만족하는 서비스들에 현재 NoSQL이 사용되고 있습니다.
  
  
2. 트랜잭션(transaction)이란 무엇인가요?

- 트랜잭션이란...............

3. MySQL에서 조인(join)의 역할은 무엇인가요? 다양한 join의 방식에 대해 설명해주세요.

- 조인이란...........

4. MySQL에서 인덱스(index)란 무엇인가요?

- 인덱스란............
