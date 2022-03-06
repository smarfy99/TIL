# 번역-googletrans

**function < module < library**

### googletrans

- 언어 감지 : 안녕하세요 → 한국어
- 언어 번역 : 안녕하세요 → Hello

순서

1. 번역기 만듦
2. 언어 감지를 원하는 문장을 설정
3. 언어를 감지
4. 번역하기

- `translate(text, dest, src)`
    - text : 번역을 원하는 문장
    - dest : 어떤 언어로
    - src : 텍스트의 언어(생략 가능)

```python
from googletrans import Translator

#1.googletrans의 번역기 제작
translator = Translator()
#2.언어 감지를 원하는 문장을 설정
sentence = input("언어를 입력하세요")
#3.언어를 감지
dest = input("어떤 언어로 번역을 원하시나요?")

result = translator.translate(sentence, dest)
detected = translator.detect(sentence)

print("===========출 력 결 과===========")
print(detected.lang, ":", sentence)
print(result.dest, ":", result.text)
print("=================================")
```