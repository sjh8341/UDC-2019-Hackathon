# 루니버스기반 리워드형 근무기록 관리서비스, MyWorkChain (by SL2)

**MyWorkChain**은 근무 기록을 안전하고 투명하게 관리하기 위한 블록체인 기반의 리워드형 근무 기록 서비스 플랫폼입니다.
**MyWorkChain**을 사용함으로써 다음과 같은 혜택을 누릴 수 있습니다.
- 근무 기록 안전 보관 및 확인
- 성실 근무 리워드 포인트를  사용하여 마켓 이용
- 직원의 주 52시간 근무 현황 파악
- 리워드 포인트를 활용한 복지 혜택
---
## MyWorkChain의 애플리케이션
- Web App(직원용) : 출퇴근 인증, 근무기록 조회, 적립 리워드 조회
> Spec - Spring Boot, JQuery
- Admin Webpage(회사용) : 총 보유 리워드 관리, 복수의 근무지 관리, 직원의 주 52시간 근무 현황 파악
> Spec - Spring Boot, JQuery
- Market : 직원의 리워드 포인트로 상품 구매, 상품 구매내역 조회
> Spec - Node.js, Vue.js 

---

## Smart Contract 

| Application | Smart Contract | API                | API명              |
|-------------|----------------|--------------------|--------------------|
| Luniverse   | GET            | Balance of MWCA    | Balance   |
| Luniverse   | GET            | Balance of BwG     | Balance                   |
| Luniverse   | GET            | Balance of User |    Balance                |
| Luniverse   | POST           | transfer2User      | 리워드 토큰 전송   |
| Luniverse   | POST           | transfer2MWCA      | 상품구매 토큰 전송 |
| Market      | UserItems      | purchaseItem       | 상품구매           |
| Market      | UserItems      | returnItem         | 상품구매취소       |
| Market      | UserItems      | purchaseList       | 구매목록           |
| App         | WorkStamp      | checkStamp         | 근무기록           |
| App         | WorkStamp      | stampList          | 근무기록조회       |
| Admin       | UserCompany    | addCompanyUser     | 직원주소등록       |
| Admin       | UserCompany    | delCompanyUser     | 직원주소삭제       |
| Admin       | UserCompany    | companyUserList     | 직원주소목록       |
