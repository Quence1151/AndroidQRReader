## 콘텐츠 유형(HTTP: Content-Type) 정리
### 정의
  - Content-Type은 api 연동시에 보내는 자원을 명시하기 위해 사용
1. application/x-www-form-urlencoded
    - html의 form의 기본 Content-Type으로 요즘은 자주 사용하지 않지만 여전히 사용하는 경우가 종종 존재
      ex) 안드로이드
    - 보내는 데이터를 URL인코딩 이라고 부르는 방식으로 인코딩 후에 웹서버로 보내는 방식을 의미
    - ``` javascript
       key = value & key = value
2. application/jon
    - RestFul API 사용의 증가로 자연스럽게 가장 많이 사용하게된 형식
      - ``` json
        {
          "key" = "value"
        }
3. multipart/form-data
    - exCode
    - ``` javascript
      var photoFile = document.getElementById("photo");
      const formData = new FormData();
      formData.append("photo", photoFile.files[0]); // 파일 첨부
      formData.append("comment", commentValue); // 텍스트 첨부
      axios.post('https://domain/form-post-url', formData, { // 요청
        headers: {
        'Content-Type': 'multipart/form-data'
        }
      })
4. text/plain
    - 형태 : 일반 텍스트 형식으로 전송 