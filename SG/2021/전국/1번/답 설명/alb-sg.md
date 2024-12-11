# 만약 특정 메트릭이 보이지않는 경우가 있을 경우

---

## Target 5xx이 안보일 경우 
### Target 5xx 띄울려고 할때는 포스트 맨이나 커널에다가
```
wsi-web-api-alb-95132481.ap-northeast-2.elb.amazonaws.com/v1/color
```
### 이렇게 color 그 다음 값을 지정 안하고 보내면 오류가 발생한다

(아직 안해봄) 아니면 asg로 만들어진 인스턴스중 1개 아니면 2개 다 지워보기

---

## elb 5xx이 안보일 경우 

### 찾아야함