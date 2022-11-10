# 1110_timeattack

# 11/09 타임어택

## 간단한 인증 서버 구현

### 회원가입

[http://127.0.0.1:8000/users/signup/](http://127.0.0.1:8000/users/signup/) 로 **username이 아닌** email 과 password를 포함한 json으로 POST 요청 보내서 회원 가입 처리를 해주세요.

조건1. 회원가입 성공 시 “회원 가입이 완료되었습니다” 메세지를 Response 해주세요

조건2. 회원 가입이 완료된 user 객체에서 생년월일 (date_of_birth column)은 필요하지 않습니다.

조건3 **회원 가입이 완료된 user의 password는 해싱되어 있어야 합니다.**

### 로그인

[http://127.0.0.1:8000/users/api/token/](http://127.0.0.1:8000/users/api/token/) 로 **username이 아닌** email 과 password를 포함한 json으로 POST 요청 보내서 accesstoken을 발급받으세요. (힌트: User model을 customize하세요)

### access token customizing

access token의 Payload에 아래와 같이 email과 token_message를 포함시키세요.

([https://jwt.io/](https://jwt.io/) 에서 확인 가능)

```jsx
**"email": "로그인 이메일",
"token_message": "sparta_time_attack"**
```

을 포함시키세요.


### (선택) customized 된 user를 admin page에서 조회가 가능하도록 만들어보세요.

당연하게도 admin 페이지 안에서의 password도 hashed된 상태여야만 합니다.


참고 사이트

[https://django-rest-framework-simplejwt.readthedocs.io/en/latest/getting_started.html](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/getting_started.html)

[https://docs.djangoproject.com/en/4.1/topics/auth/customizing/](https://docs.djangoproject.com/en/4.1/topics/auth/customizing/)

[https://django-rest-framework-simplejwt.readthedocs.io/en/latest/customizing_token_claims.html](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/customizing_token_claims.html)

[https://jwt.io/](https://jwt.io/)
