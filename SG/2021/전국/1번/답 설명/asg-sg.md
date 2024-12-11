# 2021 제 1문제 ASG-sg

## 인바운드 규칙
![asg-sg](/imgs/2021-1/img/asg-sg.png)
ssh 포트가 열려있는 대상은 bastion-sg이고<br>
tcp 8080 포트가 열려있는 대상은 alb-sg이다

---

## 아웃바운드 규칙
![asg-sg2](/imgs/2021-1/img/asg-sg2.png)
모든 트레픽을 전체 대상에게 나가는것을 허용한다