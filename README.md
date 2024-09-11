# opensearch-dashboard
---
>📝 Elasticsearch 를 처음부터 구성하여 적절히 셋업하고 운영하기란 쉽지 않은 일이다.
>게다가 특정 로그에 대해서 조건부로 알림 경보를 셋업하는것 또한 쉬운일이 아니다.
>
>Open distro 프로젝트는 알림과 보안, 분석 도구를 제공하는 플러그인과 Elasticsearch, Kibana 를 번들로 묶어 간결하고 쉽게 구성하여 사용할 수 있게 간소화한 오픈소스 프로젝트이다. 이것이 바로 Opensearch 의 전신이다.

## opensearch-dashboard 구축
### 구조
```
.
├─ docker-compose.yml
└─ opensearch-data(디렉토리)
```
### opensearch-dashboard 실행
* 아래 코드를 긁어다가 붙여넣으면 된다.
```bash
{
cd docker
sudo chown -R 1000:root opensearch-data
docker compose up -d
}
```

## 문제점
### 1. opensearch dashboard server is not yet
> 📝 **SSL/TLS 관련 문제로 인해 연결이 끊어지고 있는 것**
- 필자의 해결책은 도메인 구매 후 alb를 통해서 오는 요청을 443 포트로 리다이렉트 진행(AWS 환경에서 진행)