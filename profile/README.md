# ProfectProject

<div align="center">

![Organization Banner](https://via.placeholder.com/1200x300/4A90E2/FFFFFF?text=ProfectProject)

**혁신적인 소프트웨어 솔루션을 만드는 개발 조직**

[![GitHub followers](https://img.shields.io/github/followers/ProfectProject?style=social)](https://github.com/ProfectProject)
[![GitHub stars](https://img.shields.io/github/stars/ProfectProject?style=social)](https://github.com/ProfectProject)



</div>

---

## 👋 소개

ProfectProject는 현대적인 클라우드 네이티브 애플리케이션을 개발하는 오픈소스 조직입니다. 우리는 확장 가능하고, 안정적이며, 유지보수가 쉬운 소프트웨어를 만드는 것을 목표로 합니다.

### 🎯 우리의 미션

- **혁신**: 최신 기술 스택을 활용한 혁신적인 솔루션 제공
- **품질**: 높은 코드 품질과 테스트 커버리지 유지
- **협업**: 오픈소스 커뮤니티와의 적극적인 협업
- **학습**: 지속적인 학습과 지식 공유

---

## 🚀 주요 프로젝트

### 🍿 [Popcorn MSA](https://github.com/ProfectProject/popcorn_msa)
마이크로서비스 아키텍처 기반의 팝업 스토어 예약 플랫폼

- **기술 스택**: Spring Boot, Kafka, PostgreSQL, Redis
- **특징**: CQRS 패턴, 이벤트 소싱, 서킷 브레이커
- **상태**: 🟢 Active Development

### ☁️ [Popcorn Infrastructure](https://github.com/ProfectProject/popcorn-terraform)
AWS 기반 클라우드 인프라 자동화

- **기술 스택**: Terraform, AWS EKS, RDS, ElastiCache
- **특징**: Multi-AZ 고가용성, 자동 스케일링, 모니터링
- **상태**: 🟢 Active Development

### 🚢 [Popcorn Deploy](https://github.com/ProfectProject/popcorn_deploy)
Kubernetes 배포 자동화 및 GitOps

- **기술 스택**: Helm, ArgoCD, Kubernetes
- **특징**: GitOps 워크플로우, 환경별 설정 관리
- **상태**: 🟢 Active Development

---

## 🛠️ 기술 스택

### Backend
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white)

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)

### Infrastructure
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### Database & Cache
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white)

### DevOps & Monitoring
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Tempo](https://img.shields.io/badge/Tempo-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Mimir](https://img.shields.io/badge/Mimir-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=for-the-badge&logo=opentelemetry&logoColor=white)

---

## 📊 통계

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=ProfectProject&show_icons=true&theme=radical)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ProfectProject&layout=compact&theme=radical)

</div>

---

## 🏗️ 아키텍처

```
┌─────────────────────────────────────────────────────────────┐
│                        사용자                                 │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    AWS Route53 + ACM                        │
│                  (goormpopcorn.shop)                        │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                  Application Load Balancer                  │
│                    (SSL Termination)                        │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      EKS Cluster                            │
│  ┌──────────────┐  ┌──────────────┐  ┌───────────────┐      │
│  │   Frontend   │  │   Gateway    │  │  Services     │      │
│  │   (Next.js)  │  │ (Spring GW)  │  │(Microservices)│      │
│  └──────────────┘  └──────────────┘  └───────────────┘      │
│                                                             │
│  ┌──────────────────────────────────────────────────────┐   │
│  │              Kafka (Event Streaming)                 │   │
│  └──────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│              Data Layer (VPC Private Subnet)                │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │ RDS Aurora   │  │ ElastiCache  │  │  S3 Bucket   │       │
│  │ (PostgreSQL) │  │   (Valkey)   │  │              │       │
│  └──────────────┘  └──────────────┘  └──────────────┘       │
└─────────────────────────────────────────────────────────────┘
```

---

<div align="center">

**⭐ 이 프로젝트가 도움이 되었다면 Star를 눌러주세요! ⭐**

Made with ❤️ by ProfectProject Team

</div>
