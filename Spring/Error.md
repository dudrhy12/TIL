## 2023.11.12

1. XXXApplication Run 시, 바로 종료된다
 - 에러 메세지 : 2023-11-12T19:55:01.059+09:00 ERROR 9884 --- [  restartedMain] j.LocalContainerEntityManagerFactoryBean : Failed to initialize JPA EntityManagerFactory: [PersistenceUnit: default] Unable to build Hibernate SessionFactory; nested exception is org.hibernate.MappingException: Could not instantiate id generator [entity-name=jpabook.jpashop.domain.OrderItem]
 - 그래서 OrderIem 코드에 집중해보기도 하였고
 - buil.gradle 과 application.yml 도 수정해보았으나
 - 결구은 h2 버전 문제였다
 - 스프링부트를 3.xx를 사용하기 때문에 h2를 2.xx를 사용해야 한다