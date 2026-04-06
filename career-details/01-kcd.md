# 한국신용데이터 (KCD) — 상세 경력기술서

> 정보보안팀 / 팀원 | 2023.03 ~ 현재 (3년+) | 핀테크 (마이데이터)

---

## 핵심 역할

핀테크 기업의 네트워크 보안 인프라 설계/운영 전담.
Palo Alto 방화벽(온프레미스 + AWS VM-Series) 운영, 대외기관 VPN 관리,
IaC 기반 방화벽 관리 체계 구축, ChatOps 자동화, SecOps 도구 자체 개발.

---

## 자동화 프로젝트 (2026~)

### [2026.03] RSAC 2026 참관 및 세션 수집 시스템
- RSA Conference 참관 (샌프란시스코), 세션 자동 수집/번역 시스템 개발, 사내 발표

### [2026.03] CATO SASE IP 할당 관리
- CATO Networks IP 할당 자동화 CLI 도구

### [2026.03] 방화벽 정책 IaC 자동화
- Terraform + Atlantis GitOps, YAML Policy-as-Data, AI 연동

### [2026.02] 방화벽 정책 취약점 감사 시스템
- ISMS-P 기준 과오픈/미사용 정책 자동 탐지, Flask 웹 대시보드

### [2026.01] ChatOps 기반 DHCP 자동화
- Slack Bot(@DHCP) → API GW → Lambda → SQS → Lambda → Panorama API
- DHCP 설정 시간 수분 → 수초, 2주 만에 설계~운영 완료

---

## 주요 프로젝트

### [2025.03] CATO SASE 도입
- CATO Networks SASE 솔루션 도입, 임직원 IP Range 변경

### [2025.03] 개발 EKS Outbound 통신 개선
- 파노라마 EKS 연동 후 서비스 단위 정책 분리
- EKS VPC 전체 Any 오픈 → 서비스 단위 세밀한 Outbound 제어로 전환

### [2025.02] 파노라마 연동 및 EKS 연동
- 방화벽 설정 중앙 관리 + EKS Pod 수준 정책 관리
- IAM Cross-account Role + K8s Service Account + ClusterRole 설정
- Pod IP-to-Tag 매핑으로 Namespace/Pod 단위 정책 적용

### [2025.02] AWS DX-PA 방화벽 제거 (대외기관 VPN 통합)
- 15개+ 대외기관 VPN을 Fortinet 단일 구조로 이관
- SNAT/DNAT 설정, 대외기관 미팅 및 협업
- DX-PA 인스턴스 제거로 AWS 비용 절감

### [2024.12~2025.01] 외부망 물리 방화벽 교체 (PA-820 → PA-1410)
- 본사 5층 서버실 2대 + 선릉 KT IDC 2대 (총 4대)
- 파노라마 연동 → 정책 마이그레이션 → Slave/Master 순차 교체
- 4대 방화벽 무중단 교체 완료, CPU 과부하 이슈 근본 해결

### [2024.11~2026.02] DB 방화벽 제거 프로젝트
- DB 통신 VPC Peering 전환에 따른 DB 방화벽 불필요
- TGW, GWLB, FW 인스턴스 리소스 정리, 비용 절감

### [2024.09] EKS ALB 대상 FQDN 정책 → URL Category 전환
- ECS→EKS 이관으로 FQDN 정책이 사실상 광범위 오픈 상태
- FQDN → URL Category 형식으로 정책 전환, 서비스별 정책 분리
- EKS 환경에서도 서비스 단위 세밀한 Outbound 통신 제어 복원

### [2024.08~2025.02] AWS 방화벽 라이선스 교체 및 OS 업그레이드 (총 10대)
- AWS Palo Alto VM-Series 10대 라이선스 만료 + PAN-OS EOL 대응
- 개발 FW 2대, 운영 DMZ 2대, 운영 Internal 2대, ASIS VM500 2대, ASIS VM300 2대
- 대체 방화벽 구성 → 트래픽 이관(Zonal Shift + TGWA 라우팅) → 업그레이드 → 원복
- 6개월간 새벽 작업 다수, SRE/서비스팀 협업
- 전체 AWS 방화벽 Credit 라이선스 전환 + PAN-OS 11.1.x 업그레이드 완료

### [2024.07] KCS-KCD VPN 라우팅 방식 변경 (BGP → Static)
- KCS TGW 라우팅 변경이 KCD DX FW에 영향, 대외기관 통신 장애 발생
- AWS Site-to-Site VPN을 BGP → Static 라우팅으로 변경하여 안정성 확보

### [2024.05] SSLVPN 긴급 취약점 패치
- Ivanti Pulse Secure VPN CVE-2023-38042 등 긴급 보안 패치
- Passive → Active 순차 패치로 무중단 대응

### [2024.05] NMS 모니터링 도구 도입 (PRTG/Zabbix)
- 방화벽 하드웨어/소프트웨어 이상 상태 추이 분석 체계 구축

### [2024.04] 본사 방화벽 DataPlane CPU 과부하 분석 및 대응
- PA-820 DP CPU 급상승 원인 분석 (보안 프로파일 과다 적용)
- 단기(프로파일 최적화) → 중기(NMS 도입) → 장기(PA-1410 교체) 로드맵 수립

### [2024.04] 멘로(RBI) 예외 통신 방화벽 차단 정책
- PAC 파일 기반 멘로 예외 정책 분석 및 비업무 트래픽 식별
- 전사 20개+ 팀 단계적 차단 정책 적용
- 방화벽 5대에 정책 반영, 업무망/인터넷망 논리적 분리 강화

### [2024.03] 온프레미스 방화벽 OS 업그레이드
- 대상: Office 방화벽 2대 + IDC 방화벽 2대 (총 4대)
- PAN-OS 9.1.x → 10.1.12 무중단 업그레이드
- 이중화 해제 후 작업 권장 사항 문서화

### [2023] 고도화/개선 계획 수립
- 네트워크 보안 전반의 개선 필요사항 도출 및 로드맵 수립
- 물리 인프라 IP 확장, NAC 도입 검토, 방화벽 정책 개선, AWS 방화벽 대체 검토 등

### [2023] 임직원 IP 대역 분리
- 무작위 할당되던 임직원 IP를 특성별(개발/비개발) 분리
- DHCP 대역 분리 완료, 정책 적용 세분화 가능

### [2023] 방화벽 네이밍 표준화 및 네트워크 존 분류
- 방화벽 룰 네이밍 표준화, 네트워크 존/대역 분류 명칭 통일
- SIEM 탐지 알람 이벤트별 식별, 정책 관리 효율화
- 전사 네트워크 존(HQ_EXT, HQ_INT, AWS_MAIN, AWS_DEV, AWS_DB 등) 체계 수립

---

## 사용 기술

| 분류 | 기술 |
|------|------|
| 방화벽 | Palo Alto (PAN-OS, Panorama, VM-Series, PA-1410), Fortinet (FortiGate VM) |
| SASE/RBI | CATO Networks, Menlo Security |
| VPN | IPSec VPN (AWS Site-to-Site, Fortinet), SSLVPN (Ivanti Pulse Secure) |
| Cloud | AWS (VPC, TGW, GWLB, Lambda, EKS, S3, SQS, API GW, Direct Connect) |
| IaC | Terraform, Atlantis |
| 개발 | Python, Flask, React/TypeScript |
| 자동화 | Slack Bot, AWS Lambda, ChatOps |
| 모니터링 | OpenSearch, PRTG/Zabbix, Prometheus, Grafana |
| AI | Kiro, Bedrock (Claude), GPT-4o |
