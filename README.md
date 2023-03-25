# Chat_fortunefrog
chatgpt api활용 운세를 봐주는 웹 사이트 제작 및 배포, 광고배너 추가 프로젝트

<img width="709" alt="스크린샷 2023-03-25 오후 11 15 26" src="https://user-images.githubusercontent.com/112843229/227722681-c18573d9-0028-4675-b2c5-a1603e4579e0.png">

<img width="725" alt="스크린샷 2023-03-25 오후 11 16 16" src="https://user-images.githubusercontent.com/112843229/227722698-7562ec21-c4af-4be0-bd65-3e9025af0f94.png">


<역할 부여 >

“너는 운세 전문가야”

→ 시스템쪽에 최대한 길게 가스라이팅을 매우 많이 해줘야한다.

답변을 피하거나 안해주는걸 안하게

프롬프트 엔지니어링

역할놀이, 연극, 가스라이팅 (핵심)

그리고 시스템에 넣은 내용을

유저메시지로 한번 더 물어봐주면 

좀 더 정확해진다. 

어시스턴트의 메시지 마저 수정하고 적용하면 더 정확해짐

가스라이팅을 영어로 하면 더 잘됨

가스라이팅을 어떻게 할건지에 대한 힌트 → 프롬프트 엔지니어링

[https://www.reddit.com/r/ChatGPT/comments/110712f/dan_80/](https://www.reddit.com/r/ChatGPT/comments/110712f/dan_80/) → “또다른 자아” 민감한 질문을 다 대답해줌

- 댄의 자아 만들기

필터에 걸리지 않는 대답 

gpt-4 좀 더 한글이 잘 됨

<파라미터>

1. 무작위성

낮으면 똑같은 말만 함

1. 답변길이
    
    =토큰 답변이 잘려요. 최대한 늘리면 길게 답변이 나옴
    
    토큰이란?
    
    글자수랑 토큰은 일치 하는게 아니다 > 보통 곱하기4
    
    토크나이저
    
    [https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer)
    
    미리 몇개의 토큰으로 만들어지는지 알 수 있다.
    
    한글은 토큰 소모가 많다
    
    점성술사 역할 부여한게 토큰 323개…ㅎㄷㄷ
    
2. 상위 확률 단어
    
    예를 들면 0.8 이면 → 확률들을 더함
    
    내가 좋아하는 동물은 —- 
    
    강아지 0.5 o
    
    고양이 0.3 o 
    
    늑대 0.1
    
    아이폰 0.001
    
    탑 피를 높이는 이상한게 나올 확률이 높은데 창의적이게 된긴함 
    
    템퍼리쳐랑 거의 유사
    
    기본값을 두고 그거에서 정함
    
3. 빈도 패널티
    
    등장하는 단어가 계속 나오면 패널티를 줌
    
    똑같은 단어가 계속 나오는걸 막아줌
    
    똑같은 대답으로 토큰 수만 채움
    
    → 오늘의 운세는 좋습니다 X3000
    
    그래도 학습을 잘 해놨기 떄문에 조절 잘 안해도 잘 나오긴 함
    
4. 존재 패널티
    
    위에 꺼랑 개념 비슷
    

<환경세팅> 

챗GPT Playground

[https://platform.openai.com/playground](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVNwV2RVSEVlb3FPaXpSaVp3YlJ5SGV6Nk9GQXxBQ3Jtc0tuSk8tU3BEQTZ2aGlhNkJTdmFqWTFzVEFOcC15X1RYcDJlTGlhSldJRFpybzBEbVhRbFdHTUJ3NzhQci1vQnNBeFJkUkQ3SVZkbmNXUnZoTTY5NjltWG1UZmltWU9tbVBQZWZxOXM1dFh1dVhwZHc1NA&q=https%3A%2F%2Fplatform.openai.com%2Fplayground&v=b404R9bssc0)

노드js

[https://nodejs.org](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbFpDYS1VYk1kcHNuQkRMMnpCYU1fMVlwamN2Z3xBQ3Jtc0tsdWpGd0VCY3pzS1lvS2o3QkFYZUp4WnZWTlVMdThhV0lmNjlhZ21QT1hLelo4THEtN3BzRlJtZDEtZWtqMWpsaDFSY1Bid2RYUTViejRoODlzSkRqV2I3ZzNpMXBQS3dWeEZoYWdZYV9US25qbUthZw&q=https%3A%2F%2Fnodejs.org%2F&v=b404R9bssc0)

Visual Studio Code

[https://code.visualstudio.com](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa1pQNU1tNUhuY2hGMUtCZF9KQ1RIMHptVk1ad3xBQ3Jtc0tsb3d4TGdUVEx5cnZyNmdZbmNOcHpaREVCUC1lVHhmaVFqczJIeVJmakhKMjBxUy1CN0xIR3R3RzJTNkxXZFJtcUJkVTVTUE9iY2xWSUFySjdzVW1EeDFXUmNUbTgtMlU2VXlJb21nWGNLazRuQ2dpMA&q=https%3A%2F%2Fcode.visualstudio.com%2F&v=b404R9bssc0)

Cloudflare pages

[https://pages.cloudflare.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmt1LXJNOWgtS1dZSW9aMndyMDgzdXJlMVNKQXxBQ3Jtc0tuand2ZnFWOXlRUzdfbmRLZDMyQXY4RGNJbFRSRUQ1MlNkTThDZGJPUWktTWY4SWg5U0gwOU1UN1JldkNjckFRX0JSWGhhTmxaYnJTS3pSTVJFSHp1eU9DNzM0b29lRWItQkFVZU95TFpEc3FuQVdaUQ&q=https%3A%2F%2Fpages.cloudflare.com%2F&v=b404R9bssc0)

AWS

[https://aws.amazon.com/ko/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbE5RQUxaT2ZlUFhiYVVoWDBibVRIallma1F3d3xBQ3Jtc0tsdXFETnU5TE85X0s5T0tUV3dTNXREYlVCVk5CbWtWRl93c0gwN0JuRFUzTzJaZTYzZ1hNdjQ0d0N4RDMzNDJXU1QyM0ZkWjZlRUJMY0tHc1ZsSTZuMnpJNzNzU3VHSllhMXFvTzZYOFhWWElDM0lZYw&q=https%3A%2F%2Faws.amazon.com%2Fko%2F&v=b404R9bssc0)

-람다 사용할거임

영문 주소 바꿔주기

[https://www.jusoen.com/](https://www.jusoen.com/)

이런거 만듭니다.

[https://fortunedoge.chat/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmdsLWdIeGYtU09aaGFGcU9kaGhRTlpVWjN1QXxBQ3Jtc0ttR3hKQ2U3R2RMWDM0eGlXOEJmSk1WNEIzeDdkZEtoZllMYXg1SnpURzF2cFJEWFk3MXQwU0FJTjlSakJ5MDItSkhDZTUyRzJNb0tnUkpVX1Bsa0JjQkxVTF84aW1HRVhDYTdfSktfYzlZTnhPOFhZTQ&q=https%3A%2F%2Ffortunedoge.chat%2F&v=b404R9bssc0)

AWS gogle otp - 몇 백만원 과금 막을 수 있다

[https://tech4u.tistory.com/41](https://tech4u.tistory.com/41)

[https://www.npmjs.com/package/openai](https://www.npmjs.com/package/openai)

API Key

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

[https://platform.openai.com/docs/api-reference/chat/create](https://platform.openai.com/docs/api-reference/chat/create)

npm i express

[https://www.npmjs.com/package/express](https://www.npmjs.com/package/express)

express 안내서

[https://expressjs.com/ko/starter/installing.html](https://expressjs.com/ko/starter/installing.html)

깃허브 코드

[https://gist.github.com/youtube-jocoding/65b06d527465fac173640cc18fa55ed3](https://gist.github.com/youtube-jocoding/65b06d527465fac173640cc18fa55ed3)

[https://studioplug.tistory.com/353](https://studioplug.tistory.com/353)

# 해결

1. lsof로 사용중인 포트에서 죽이고자 하는 프로세스ID를 알아낸다. 아래 내용에서는 node의 PID인 22731이다.

```xml
(base) wonjinyi@wonjinYi:~/Desktop/LearnNode$ lsof -i tcp:8080
COMMAND   PID     USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
chrome   2189 wonjinyi   64u  IPv6 396182      0t0  TCP ip6-localhost:54042->ip6-localhost:http-alt (ESTABLISHED)
node    22731 wonjinyi   28u  IPv6 396158      0t0  TCP *:http-alt (LISTEN)
node    22731 wonjinyi   36u  IPv6 396183      0t0  TCP ip6-localhost:http-alt->ip6-localhost:54042 (ESTABLISHED)
node    22731 wonjinyi   37u  IPv6 396994      0t0  TCP ip6-localhost:http-alt->ip6-localhost:54044 (CLOSE_WAIT)
```

2. kill -9 <프로세스ID> 로 프로세스를 죽인다.

```xml
(base) wonjinyi@wonjinYi:~/Desktop/LearnNode$ kill -9 22731
[1]+  죽었음               node 200823
```

3. 이후 다시 프로그램을 실행하면 해당 포트에서 정상적으로 실행된다.

! tap 누르면 html 자동완성

fetch 사용하기

[https://developer.mozilla.org/ko/docs/Web/API/Fetch_API/Using_Fetch](https://developer.mozilla.org/ko/docs/Web/API/Fetch_API/Using_Fetch)

채팅 ui

[https://codepen.io/rossmartin/pen/XJmpQr](https://codepen.io/rossmartin/pen/XJmpQr)

전의 내용을 저장하고 알려주는게 필요

챗 gpt 자체는

api로 구현할때 이력을 다 보내야 함

<생년월일 시간 입력 받기>

이미지 생성

[https://openai.com/product/dall-e-2](https://openai.com/product/dall-e-2)

현재 날짜

let todayDateTime = new Date().toLocaleString(’ko-KR’,{timeZone: Asia/Seoul});

<채팅 올 동안 로딩 스피너 구현하기>

아이콘 제공 - 부트스트랩과 유사(부트스트랩 안에 폰트어썸 들어가있음) 아이콘을 폰트처럼 만들어줌

[https://fontawesome.com/](https://fontawesome.com/)

font awesome cdn 폰트 어썸 임포트 해주는 링크 → 부트스트랩도 이랬음

<실전 배포>

서버 스케일링을 aws한테 맡기고 모두가 쓸수 있는 환경에 집중

[프론트 엔드]

Cloudflare pages

[https://pages.cloudflare.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmt1LXJNOWgtS1dZSW9aMndyMDgzdXJlMVNKQXxBQ3Jtc0tuand2ZnFWOXlRUzdfbmRLZDMyQXY4RGNJbFRSRUQ1MlNkTThDZGJPUWktTWY4SWg5U0gwOU1UN1JldkNjckFRX0JSWGhhTmxaYnJTS3pSTVJFSHp1eU9DNzM0b29lRWItQkFVZU95TFpEc3FuQVdaUQ&q=https%3A%2F%2Fpages.cloudflare.com%2F&v=b404R9bssc0)

왜쓰냐? 

매트리 파이보다는

언리미티드 → 밴드위스 상관없이 무료

완전 트래픽 프리하게 올리는것

워커스라는것을 제공 

람다같은 개념

api요금 토큰

pages 들어가서 크레이트 만들기

배포완료

[https://chatfrog.pages.dev/](https://chatfrog.pages.dev/) 

ㅎㅎ

[백엔드]

AWS lambda

[https://aws.amazon.com/ko/lambda/](https://aws.amazon.com/ko/lambda/)

원래면 ec2로 서버를 만들어서 거기에 다 올려서 씀

근데 서버가 작으면 터짐

서버리스 - lambda

서버 설치하거나 만들 필요없이

하나의 함수에 넣어서 올리면 됨

코드만있다가 실행요청이 오면 그때만 시작되고 서버가 꺼짐

요금도 합리적 요청당 얼마 이런식으로 됨

굳이 서버가 필요없고

무료요청 100만건 프리티어 → 무료로 쓸 수 있음 

백엔드가 잠깐 떳다가 죽는

익스프레스를 서버리스에 특화된걸로 바꿈

서버개념 

트리거 추가 

API gateway

리소스 추가 proxy

api 배포

<광고>

카카오 에드핏

[https://adfit.kakao.com/info](https://adfit.kakao.com/info)

토스 아이디로 송금하기 

카카오 큐알코드로 송금하기

토스로 만들기

[https://blog.naver.com/juny607/222631830394](https://blog.naver.com/juny607/222631830394)
