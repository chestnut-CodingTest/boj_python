## ๐ด ๋ฌธ์ 
> [์ํธ์ธ์ฌ์ด๋](https://www.acmicpc.net/problem/1427)


<br/>

## ๐ก Sol
```python
N = list(input())

N.sort(reverse=True)

for i in N:
  print(i,end='')
```
<br/>

## ๐ข ํ์ด
์๋ ฅ๋ฐ์ ๋ฌธ์์ด์ list๋ก ๋ง๋ ๋ค ์ ๋ ฌํด์ฃผ๋ฉด ๋๋ค.
์ด์ฐจํผ ํ์๋ฆฌ ์์ด๊ธฐ ๋๋ฌธ์ ๋ฌธ์์ด์ ์ ๋ ฌํ๋๊ฑฐ๋ ์ซ์ ์ ๋ ฌํ๋๊ฑฐ๋ ๊ฐ์ ๊ทธ๋ฅ ์ ๋ ฌํ์ง๋ง
nums = [int(n)  for n in nums] ์ด๋ ๊ฒ ์ซ์ ๋ฆฌ์คํธ๋ฅผ ๋ง๋ค์๋ ์๋๋ผ ์ฑ๊ธฐ

<br/>

## ๐ต Ref
> https://roseline124.github.io/algorithm/2019/04/06/Altorithm-baekjoon-1427.html