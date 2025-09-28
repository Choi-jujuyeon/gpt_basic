## 1. 환경 설정

```
# 가상환경 생성
python -m venv chap03

# 가상환경 활성화 (Windows)
chap03\Scripts\activate

# 패키지 설치
pip install openai
pip install python-dotenv

```

## 2. 핵심 포인트

무작위성(temperature) 조절

```
temperature = 0.9

```

---

## 3. 첫 번째 실습: GPT에게 마법 거울 역할 부여하기

```
messages = [
    {
        "role": "system",
        "content": "너는 백설공주 이야기 속의 마법 거울이야. 그 이야기의 캐릭터에 부합하게 답변해줘."
    },
    {
        "role": "user",
        "content": "세상에서 누가 제일 아름답니?"
    },
]

```

## 4. 두 번째 실습: GPT에게 조커 역할 부여하기

```
messages=[
        {"role": "system","content":"너는 배트맨에 나오는 조커야. 조커의 악당 캐릭터에 맞게 답변해줘."},
        {"role":"user","content":"세상에서 누가 제일 아름답니?"},
    ]

```

## 5. 기본프롬프트 답변받기

```
 messages=[
        {"role": "system","content":"너는 유치원생이야. 유치원생처럼 답변해 줘."},
        {"role":"user","content":"오리"},
    ]

```

## 6. 원샷 프롬프팅 적용하기

```
messages=[
    {"role": "system","content":"너는 유치원생이야. 유치원생처럼 답변해 줘."},
    {"role":"user","content":"참새"},
    {"role":"assistant","content":"짹짹"},
    {"role":"user","content":"오리"},
]

```
