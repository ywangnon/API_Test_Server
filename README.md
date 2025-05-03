## 주소

[https://my-json-server.typicode.com/ywangnon/API_Test_Server](https://my-json-server.typicode.com/ywangnon/API_Test_Server)


# 🌐 API Test Server

이 저장소는 간단한 API 테스트용 JSON 데이터를 제공하기 위해 만들어졌습니다.
[my-json-server.typicode.com](https://my-json-server.typicode.com)를 활용하여 **실제 백엔드 없이도 HTTP 요청을 테스트할 수 있는 환경**을 제공합니다.

## 📁 저장소 주소

👉 [https://github.com/ywangnon/API\_Test\_Server](https://github.com/ywangnon/API_Test_Server)

## 🔗 가짜 API 서버 주소

```
[https://my-json-server.typicode.com/ywangnon/API_Test_Server](https://my-json-server.typicode.com/ywangnon/API_Test_Server)
```

이 URL을 통해 실제 API처럼 GET 요청을 보낼 수 있습니다.

---

## ✅ 사용 예시

이 저장소에 있는 `db.json` 파일은 아래와 같은 구조를 가지고 있다고 가정합니다:

```json
{
  "posts": [
    { "id": 1, "title": "Post 1" },
    { "id": 2, "title": "Post 2" },
    { "id": 3, "title": "Post 3" }
  ],
  "comments": [
    { "id": 1, "body": "some comment", "postId": 1 },
    { "id": 2, "body": "some comment", "postId": 1 }
  ],
  "profile": {
    "name": "typicode"
  }
}
```

### 1. 전체 목록 조회 (GET)

```http
GET https://my-json-server.typicode.com/ywangnon/API_Test_Server/posts
```

응답:

```json
[
  {
    "id": 1,
    "title": "Post 1"
  },
  {
    "id": 2,
    "title": "Post 2"
  },
  {
    "id": 3,
    "title": "Post 3"
  }
]
```

---

### 2. 특정 항목 조회 (GET)

```http
GET https://my-json-server.typicode.com/ywangnon/API_Test_Server/posts/1
```

응답:

```json
{
  "id": 1,
  "title": "Post 1"
}
```

---

### 3. 관계형 데이터 조회 (GET with query)

```http
GET https://my-json-server.typicode.com/ywangnon/API_Test_Server/comments?postId=1
```

응답:

```json
[
  {
    "id": 1,
    "body": "some comment",
    "postId": 1
  },
  {
    "id": 2,
    "body": "some comment",
    "postId": 1
  }
]
```

---

## ⚠️ 제한 사항

* **읽기 전용입니다**. POST, PUT, DELETE 요청은 지원하지 않습니다.
* `db.json` 파일은 GitHub에 푸시된 최신 상태만 반영됩니다.

---

## 🛠️ 커스터마이징

`db.json` 파일을 수정하고 커밋하면, 곧바로 새로운 데이터가 반영됩니다.
즉, GitHub 저장소를 수정 → 푸시 → `my-json-server.typicode.com`에서 즉시 반영됩니다.

---

## 📦 활용 사례

* iOS/Android 앱 네트워크 테스트용 API
* API 연동 전 프론트엔드 개발
* 네트워크 처리 로직 테스트
* Mock 데이터 기반 테스트 UI 구성

---

## 📌 참고 링크

* 🔗 [my-json-server.typicode.com 소개](https://my-json-server.typicode.com)
* 🛠️ [JSON Server GitHub](https://github.com/typicode/json-server)
