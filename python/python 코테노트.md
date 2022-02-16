# python 코테 노트


- 이차원 배열에서 len()
    
    ```python
    arr = [[1,2,3],[4,5,6]]
    len(arr)
    =>2
    len(arr[0])
    =>3
    ```
    
- 평균 구하기
    - 내장 라이브러리 : **statistics-mean()**
        
        ```python
        import statistics
        
        def solution(arr):
        	result = statistics.***mean***(arr)
        	return result
        ```
        
- 자연수 x를 list에 한자리씩 넣으려면
    - 자연수 x를 string으로 치환하여 list형식으로 담는다
        
        → 자리수를 하나씩 쪼개어 배열에 담기 위해
        
- 소수점 자리수 조절
    - `round(실수, n)` : 소수점 n번째 자리까지 반올림해서 나타냄
    - `math.ceil(i)` : 소수점 올림
    - `math.floor(i)` : 소수점 내림
        
        ex) 0.456이면 소수점 둘째자리에서 내리라고 하면 0.450
        
    - `math.trunc(i)` : 소수점 버림
        
        ex) 0.456이면 소수점 둘째자리에서 버리라고 하면 0.45
        

### 배열에서 중복 제거하기

---

- **set()**
    - 중복을 허용하지 x
    - 순서 x
    
    ```python
    my_list = ['A','A','B','C']
    my_set = set(my_list)
    new_list = list(my_set)
    print(new_list)
    
    =>['B','C','A']
    ```
    
- for문 이용
    - 순서 o
    - my_list의 모든 요소를 순회하며 해당 요소가 new_list에 있는지 확인한 다음 해당 요소가 존재하지 않으면 new_list에 추가
    
    ```python
    my_list = ['A','A','B','C']
    new_list = []
    for i in my_list:
    	if i not in new_list:
    		new_list.append(i)
    print(new_list)
    
    => ['A','B','C']
    ```
    
- 문자열이 ‘숫자’로만 이루어져 있는지
    - str.isdigit(”문자열”)
        - 숫자 or 음수 판단 x
    - “문자열”.isdigit()