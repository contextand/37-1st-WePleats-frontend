# WePleats 프로젝트 개요

- 기본적인 커머스 사이트 flow를 가진 사이트 선정해 클론 코딩을 진행했습니다.
- 회원가입 - 로그인 - 메인 - 리스트 - 상세 - 결제 / 장바구니 - 리뷰
- 개발자들의 보다 개성있는 데스크를 위해 다채로운 색상의 프로덕트 판매하는 사이트를 기획했습니다.

## 개발 인원 및 기간

- 개발기간 : 2030/1/1 ~ 2030/1/14
- 개발 인원 : 프론트엔드 3명, 백엔드 2명
- [백엔드 github 링크]()

## 적용 기술

> - Front-End : React.js, sass
> - Back-End : Node.js, Express, JSON Web TOKEN, Bcrypt, My SQL, Multer
> - Common : AWS(EC2,RDS), RESTful API

## 프로젝트 시연 영상

[프로젝트 영상](https://www.youtube.com/watch?v=Mao03-WqfxQ)

<br>

# 구현 페이지 및 기능 소개

## 구현 목표 (내가 작업한 페이지)

- [ ] Nav, Footer
- [x] 회원가입/로그인
- [ ] 메인
- [x] 리스트
- [ ] 상세
- [ ] 장바구니
- [x] 결제
- [ ] 리뷰

## 구현 사항 설명

### 회원가입 / 로그인

- 비교적 입력창이 많아 가입하기 버튼을 눌렀을 때 잘못된 입력으로 되돌아가는 것이 사용자 경험에 좋지 않다고 생각해 아래와 같은 기능을 넣었습니다.
- 필수 입력값에 동기적 유효성 검사로 안내문구를 보여주고 모두 통과 시 버튼을 활성화했습니다. (회원가입, 로그인)
- useRef 와 FileReader로 프로필 사진도 첨부했지만, 백엔드와 소통 오류로 formData 를 활용해 데이터를 전송하진 못했습니다.
- 로그인 시 fetch 함수를 사용해 데이터를 전달하고 localStorage 에 토큰을 저장했습니다.

### 리스트 페이지

- 쿼리스트링 url 주소의 변수 값을 useSearchParams 훅을 사용해 가져와 사용했습니다.
- useEffect 훅과 fetch 함수를 사용해 전체 카테고리를 불러왔고, 필터 클릭 시 쿼리 스트링을 추가해 해당 값의 데이터를 불러왔습니다.
- 백엔드 통신 전에 활용할 목데이터를 빠르게 만들어 팀원에게 공유했습니다.

### 결제 페이지

- 프로젝트 기간을 고려해 일부 기능만 구현했습니다.
- 결제할 제품 목록을 받아와서 제품 목록과 가격 총합을 보여주고, 쿠폰을 사용할 경우 총합 금액에서 빼줍니다.
- 그 외 입력창 레이아웃은 flex 사용했고, 주소 입력창은 grid를 적용해 구현했습니다. 

# 관련 블로그 포스팅 

## 프로젝트를 진행하며 배운 내용은 블로그에 포스팅했습니다.

- [Mock 데이터 array.map() 에러 메시지 대응](https://velog.io/@rayong/Mock-%EB%8D%B0%EC%9D%B4%ED%84%B0-array.map-%EC%97%90%EB%9F%AC-%EB%A9%94%EC%8B%9C%EC%A7%80-%EB%8C%80%EC%9D%91)
- [팀프로젝트 Github 활용 및 컨플릭트 해결](https://velog.io/@rayong/%ED%8C%80%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Github-%ED%99%9C%EC%9A%A9-%EB%B0%8F-%EC%9C%A0%EC%9D%98%EC%82%AC%ED%95%AD)
- [리스트 페이지 디자인(기능X), Mock 데이터 활용](https://velog.io/@rayong/%EB%A6%AC%EC%8A%A4%ED%8A%B8-%ED%8E%98%EC%9D%B4%EC%A7%80-%EB%94%94%EC%9E%90%EC%9D%B8%EA%B8%B0%EB%8A%A5X-Mock-%EB%8D%B0%EC%9D%B4%ED%84%B0-%ED%99%9C%EC%9A%A9)
- [회원가입 페이지 유효성 검사](https://velog.io/@rayong/%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85-%ED%8E%98%EC%9D%B4%EC%A7%80-%EC%9C%A0%ED%9A%A8%EC%84%B1-%EA%B2%80%EC%82%AC)
- [회원가입 사진 입력하기, FileReader, useRef](https://velog.io/@rayong/%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85-%EC%82%AC%EC%A7%84-%EC%A0%84%EC%86%A1%ED%95%98%EA%B8%B0-FileReader-FormDate-useRef)
- [회원가입 동기적 유효성 검사, 정규표현식, Object.entries, every](https://velog.io/@rayong/%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85-%EB%8F%99%EA%B8%B0%EC%A0%81-%EC%9C%A0%ED%9A%A8%EC%84%B1-%EA%B2%80%EC%82%AC-%EC%A0%95%EA%B7%9C%ED%91%9C%ED%98%84%EC%8B%9D-Object.entries-every)
- [사진 포함한 데이터 전송하기 FormData()](https://velog.io/@rayong/%EC%82%AC%EC%A7%84-%ED%8F%AC%ED%95%A8%ED%95%9C-%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%A0%84%EC%86%A1%ED%95%98%EA%B8%B0-FormData)
- [로그인 통신, 토큰 받고 사용하기, jwt](https://velog.io/@rayong/%EB%A1%9C%EA%B7%B8%EC%9D%B8-%ED%86%B5%EC%8B%A0-%ED%86%A0%ED%81%B0-%EB%B0%9B%EA%B3%A0-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-jwt)
- [카테고리 쿼리스트링, null 값 찍히는 에러 해결](https://velog.io/@rayong/%EC%B9%B4%ED%85%8C%EA%B3%A0%EB%A6%AC-%EC%BF%BC%EB%A6%AC%EC%8A%A4%ED%8A%B8%EB%A7%81-null-%EA%B0%92-%EC%B0%8D%ED%9E%88%EB%8A%94-%EC%97%90%EB%9F%AC-%ED%95%B4%EA%B2%B0)
- [프로퍼티가 없는 중첩 객체에 접근하는 법, 옵셔널 체이닝, optional chaining](https://velog.io/@rayong/%ED%94%84%EB%A1%9C%ED%8D%BC%ED%8B%B0%EA%B0%80-%EC%97%86%EB%8A%94-%EC%A4%91%EC%B2%A9-%EA%B0%9D%EC%B2%B4%EC%97%90-%EC%A0%91%EA%B7%BC%ED%95%98%EB%8A%94-%EB%B2%95-%EC%98%B5%EC%85%94%EB%84%90-%EC%B2%B4%EC%9D%B4%EB%8B%9D-optional-chaining)

<br>

## Reference

- 이 프로젝트는 [플리츠마마](https://pleatsmama.com/) 사이트를 참조하여 학습목적으로 만들었습니다.
