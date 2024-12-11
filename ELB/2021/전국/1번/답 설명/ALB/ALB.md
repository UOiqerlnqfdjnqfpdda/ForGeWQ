# 2021 제 1번 문제 ALB 설정 파트

### Aplication Load Balancer을 선택한다
![alb-1](/imgs/2021-1/img/alb-1.png)

---

### 외부로 부터 트레픽을 받을것이기 떄문에 인터넷 경계로 설정한다
![alb-2](/imgs/2021-1/img/alb-2.png)

---

### VPC설정하고 가용영역에서 서브넷 매핑 설정 파트가 있는데 인터넷 경계일 경우 public이다 반대로 내부면 private이다
![alb-3](/imgs/2021-1/img/alb-3.png)

---

### 보안그룹을 설정하고 ALB 자체의 포트를 설정해주고 만들어둔 target Group을 설정한다
![alb-4](/imgs/2021-1/img/alb-4.png)

---

# 나머지는 기본값으로 하고 생성한다
