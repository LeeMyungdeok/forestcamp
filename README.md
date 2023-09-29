# forestcamp X cloudmate 인턴십 협업 프로젝트입니다



<br>
<p align="center">
<img width="400px" src="https://github.com/LeeMyungdeok/forestcamp/assets/115915362/1b353e95-3818-4f7b-a253-0f9b0679acc8">
<br>
<img src= "https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=white" />
<img src= "https://img.shields.io/badge/nodedotjs-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src= "https://img.shields.io/badge/mysql-4479A1?style=flat-square&logo=mysql&logoColor=white" />
<img src= "https://img.shields.io/badge/mongodb-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src= "https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white" />
<img src= "https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white" />
<br>
<img src= "https://img.shields.io/badge/amazonec2-FF9900?style=flat-square&logo=amazonec2&logoColor=white" />
<img src= "https://img.shields.io/badge/amazonsimpleemailservice-DD344C?style=flat-square&logo=amazonsimpleemailservice&logoColor=white" />
<img src= "https://img.shields.io/badge/docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src= "https://img.shields.io/badge/inux-FCC624?style=flat-square&logo=linux&logoColor=white" />
<br>
</p>

## 주제 선정 이유
코로나19 대유행 이후, 자연과 야외 활동에 대한 갈망이 증가함에 따라 캠핑장 예약에 대한 인기가 폭발적으로 증가하고 있습니다. 이러한 수요 증가로 인해 지역과 관계없이 캠핑장 예약이 엄청난 경쟁이 일어나고 있어, 예약을 얻기가 어려워진 상황입니다. 그러나 이러한 어려움 중에는 불법 캠핑장 예약 매크로 사이트로 인한 차별적인 문제도 불거져 나왔습니다.
우리의 목표는 이러한 어려움을 극복하고 캠핑을 즐기고자 하는 모든 이들에게 도움을 주기 위한 서비스를 제공하는 것입니다. 일반 정보를 갖고 있지 않은 사람들에게도 캠핑장 예약 정보를 쉽게 접할 수 있도록 하여, 자연과 캠핑의 아름다움을 누릴 수 있는 기회를 확대하는 것이 우리의 목표입니다. 이를 통해 사람들은 더 많은 야외 활동을 즐기며, 동시에 불법 예약과 차별을 줄이는데 도움이 되는 서비스를 제공하고자 합니다.

### development environment

#### Recipe-provided-project
```
json-server --watch ./bin_FoodData.json --host 0.0.0.0 --port 5000
```
```
json-serve
```
```
r --watch ./Trash.json --host 0.0.0.0 --port 5001
```

#### server
```
uvicorn main:app --host 0.0.0.0 --port 3000 --reload
```

#### client
```
nodemon app.js
```

## back-end 아키텍쳐 설계

<img width="700" alt="image" src="https://github.com/LeeMyungdeok/Recipe-provided-project/assets/115915362/fa80152a-5bb5-4977-9e4f-a94d953fa51e">

### 기능 동작
|                sign in              |                sign up               |
| :----------------------------------: | :----------------------------------: | 
| <img src='https://github.com/LeeMyungdeok/Recipe-provided-project/assets/115915362/0a8dd09a-962c-4eb5-9ee7-aea4d4bcc16f' width='400px' height='300px'> | <img src='https://github.com/LeeMyungdeok/Recipe-provided-project/assets/115915362/96fccd2d-74b5-4c75-9f83-2857754edf8d' width='400px' height='300px'>                                 |

|                return              |                rental               |
| :----------------------------------: | :----------------------------------: |
| <img src='https://github.com/LeeMyungdeok/Recipe-provided-project/assets/115915362/b6b795d0-f00b-4429-8351-fe532fa74a7c' width='400px' height='300px'> | <img src='https://github.com/LeeMyungdeok/Recipe-provided-project/assets/115915362/36730ab2-37b2-4ecf-8324-3318801bfbc4' width='400px' height='300px'> |

## 배포

예정 입니다.

## 팀명: 이세계식당

* [팀원](링크) - 이명덕, 서민희

## 담당 업무

- backend
  - 공공 데이터 포털에서 요리 재료에 대한 데이터를 가공했습니다.
    - 재료에 대한 전처리는 주로 코넬파이를 이용하여 형태소 분리 또는 정규 표현식을 사용하여 작업을 진행했습니다. 
  - 요리 레시피에 대한 데이터 및 재료 데이터를 가지고 Fast api를 사용하여 Rest full 방식으로 프로세스를 구축했습니다.
    - json 파일을 임의의 server로 사용하여 전처리를 잘못된부분을 필터링을 걸치도록 하기위해 구축했습니다.
    - 검색, 연관검색, 신고, 레시피 조회 등 전반적인 api 설계 부터 구현까지 위주로 담당업무를 진행했습니다. 
- frontend
  - xhr를 사용하여 client와 server을 연결했습니다.
    - 기존에 axios를 사용했지만 xhr을 알게 되어 어떤 흐름으로 가는지 경험했습니다. 
 
## 보완점

* 데이터 전처리에 대한 경우 완벽하지 못하여 재료가 아닌 값이 나오는 경우가 있습니다. 그것을 사용자가 신고를 해줌으로써 필터안에 들어가게 되고 그 후 다시 그 음식에 대한 레시피를 조회하면 필터링이 될 수 있도록 설계를 했습니다. 비롯 초반에는 애러가 종종 발생하지만 사용자들이 사용하고 신고를 눌러 줌으로써 데이터가 쌓여 더욱 정교한 프로세스서가 될수 있는 성장형 프로그램을 만들었습니다.
* 현재 AWS에서 다시 Develop 예정입니다.
