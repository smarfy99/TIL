# 날씨 API 크롤링

### API(Application Programming Interface)

---

응용 프로그램, 프로그래밍, 인터페이스

: 프로그램과 프로그램을 이어주는 인터페이스

- 클라이언트와 서버 간에 데이터를 원활하게 교환될 수 있도록 도와주는 것

**API Key**

- OpenAPI를 사용하기 위한 방명록
- 특정 사용자를 구분할 수 있는 Key
- API를 call 한다고 함

**json(javascript object notation)**

- 문자 기반의 데이터 포맷
- 데이터를 주고 받을 때 사용하는 포맷
- `json.loads(문자열)` : 문자열을 json 포맷으로 변환

![Untitled](%E1%84%82%E1%85%A1%E1%86%AF%E1%84%8A%E1%85%B5%20API%20%20d75c6/Untitled.png)

```python
import requests
import json

city = "Seoul"
apikey = "################################"
# f-string으로 apikey에 나의 apikey를 삽입
api = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={apikey}"

result = requests.get(api)
print(result.text)

#json 형태로 변환
data = json.loads(result.text)

# print(type(result.text))
=> string
# print(type(data))
=> dictionary
(json이 string을 딕셔너리 형태로 변환시킨 것)

print(data["name"],"의 날씨입니다.")
print("날씨는 ",data["weather"][0]["main"],"입니다.")
print("현재 온도는 ",data["main"]["temp"],"입니다.")
print("하지만 체감 온도는 ",data["main"]["feels_like"],"입니다.")
# 최저 기온 : main - temp_min
print("최저 기온은 ",data["main"]["temp_min"],"입니다.")
```