# 1차. 파이썬 기초 문법과 자료형에 대한 이해
## 데일리과제 1-2. 평균 성적 구하기

김해피의 성적은 아래와 같다.

1. 신규 과목인 'algorithm'을 시험 보았더니 90점을 받았다. 성적 딕셔너리에 이를 추가하여라.
2. python 과목의 점수가 80점이 아닌 85점으로 정정되었다. 주어진 성적 딕셔너리를 수정하여라.
3. 김해피의 전체 과목 평균 점수를 출력하라.

```python
score = {
    'python': 80,
    'django': 89,
    'web': 83
}
```
=> 정답
```python
score = {
    'python': 80,
    'django': 89,
    'web': 83
}
score['algorithm'] = 90
score['python'] = 85
# 파이썬 딕셔너리 순회
acc = 0
for value in score.values(): # .values 이용
    acc = acc + value
# print(acc) # 347
# print(len(score)) #4
print(acc / len(score))
```

## 데일리과제 1-4. 자릿수 출력 예제

사용자가 입력한 각 자릿수를 더해 출력하는 코드를 작성하라
```python
s = input('숫자를 입력해주세요 : ')
```
=> 정답
```python
s = input('숫자를 입력해주세요 : ')
# print(list(map(int, s))) # [1, 2, 3] #아직 map이 어떤 기능인지 모르겠음
print(sum(map(int, s)))
```

## 데일리과제 2-2. 카페 주문 건수 출력하기 예제

다음은 한 커피전문점의 주문 대기목록입니다. 주어진 문자열을 가지고, 아래 문제에 대한 프로그램을 작성하세요.
1. 총 몇잔의 주문이 들어왔는지 확인하세요.
2. 중복을 제거한 메뉴만을 리스트 형식으로 출력하세요. (단, 내림차순 정렬하여 출력하라)

orders = '아이스아메리카노,카라멜마키야또,에스프레소,아메리카노,아메리카노,아이스라떼,핫초코,아이스아메리카노,아메리카노,아이스카라멜마키야또,아이스라떼,라떼마키야또,카푸치노,라떼마키야또'

=> 정답
```python
orders = '아이스아메리카노,카라멜마키야또,에스프레소,아메리카노,아메리카노,아이스라떼,핫초코,아이스아메리카노,아메리카노,아이스카라멜마키야또,아이스라떼,라떼마키야또,카푸치노,라떼마키야또'
orders_list = orders.split(',')
print(len(orders_list))

set(orders_list)
result_list = list(set(orders_list))
result_list.sort(reverse=True)
print(result_list)
```