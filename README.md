# Spring Boot Actuator and Micrometer Boilerplate

## Actuator and Micrometer

> **NOTE**
>
> Spring Boot 2.0 이상에서 Actuator와 Micrometer가 통합되어 성능 지표를 자동으로 수집

### Actuator

- 애플리케이션의 상태와 성능을 모니터링하고 관리할 수 있는 엔드포인트 제공
- 헬스 체크, 환경 정보, 메트릭 등 확인 가능

### Micrometer

- 애플리케이션 성능 지표를 수집, Prometheus, Datadog 등 외부 모니터링 시스템과 통합

### 주의 사항

1. 필요한 엔드포인트만 노출하고, 가능하면 *(와일드카드) 사용을 피한다.
2. shutdown 엔드포인트는 활성화하지 않는다.
3. JMX를 사용하지 않으면 비활성화한다.
4. Actuator 기본 경로는 사용하지 않는다.
5. Actuator는 애플리케이션과 다른 포트를 사용한다.
6. 권한이 있는 사용자만 Actuator에 접근할 수 있도록 설정한다.
7. audit event를 통해 접근 기록을 남긴다.

## Reference

- https://docs.spring.io/spring-boot/reference/actuator/endpoints.html#actuator.endpoints
- https://docs.spring.io/spring-boot/reference/actuator/metrics.html#actuator.metrics.export.prometheus
- https://grafana.com/tutorials/provision-dashboards-and-data-sources/
- https://grafana.com/docs/grafana/latest/administration/provisioning/
- https://techblog.woowahan.com/9232/
