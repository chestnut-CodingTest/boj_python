## ๐ด ๋ฌธ์ 
> [์ฒด์คํ ๋ค์ ์น ํ๊ธฐ](https://www.acmicpc.net/problem/1018)


<br/>

## ๐ก Sol
```python
N, M = map(int, input().split())
board = []
newboard = []
newboard_str = ''
check_chess1 = list("WBWBWBWBBWBWBWBWWBWBWBWBBWBWBWBWWBWBWBWBBWBWBWBWWBWBWBWBBWBWBWBW")
check_chess2 = list("BWBWBWBWWBWBWBWBBWBWBWBWWBWBWBWBBWBWBWBWWBWBWBWBBWBWBWBWWBWBWBWB")

## 1
for i in range(N):
  board.append(input())
## 2
for i in range(M-7):
  for j in range(N-7):
    for k in range(j, j+8):
      newboard_str = newboard_str + board[k][i:i+8]
    newboard.append(newboard_str)
    newboard_str = ''
## 3
result = []
for i in newboard:
  min = 0
  i = list(i)
  for j in range(64):
    if(check_chess1[j] != i[j]):
      min += 1
  result.append(min)
  min = 0
  for j in range(64):
    if(check_chess2[j] != i[j]):
      min += 1
  result.append(min)
## 4
result.sort()
print(result[0])
```
<br/>

## ๐ข ํ์ด
1. ์ฒซ๋ฒ์งธ for๋ฌธ์์ ํ์ค์ฉ input ๋ฐ๊ธฐ
2. input๋ฐ์ ๊ฐ์์ 8x8 ํฌ๊ธฐ์ ์์๋ฅผ ๋ฝ์๋ด๊ธฐ
  ๊ทธ๋์ ๋ฒ์๋ ๊ฐ๊ฐ 0๋ถํฐ M-7, 0๋ถํฐ N-7 ๋ํฉ (M-7)*(N-7)๊ฐ์ ๋ฌธ์์ด์ newboard์ appendํ๋ค.
  newboard์๋ ํฌ๊ธฐ๊ฐ 64(8x8์ด๊ธฐ ๋๋ฌธ์)์ธ ๋ฌธ์์ด์ด ์ด (M-7)*(N-7)๊ฐ ๋ค์ด์๋ค.
3. newboard์ ์์๋ฅผ ํ๋์ฉ ์ ๊ทผํด ๋ฆฌ์คํธ๋ก ๋ณํํ๋ค, ๋ฏธ๋ฆฌ ๋ง๋ค์ด๋ check_chess1๊ณผ check_chess2์ ๋น๊ตํ๋ค.
๋ธ๋์ผ๋ก ์์ํ๋๊ฒฝ์ฐ, ํ์ดํธ๋ก ์์ํ๋ ๊ฒฝ์ฐ ๋๊ฐ์ง์ด๋ฏ๋ก ๋๋ฒ ๋น๊ตํด min๊ฐ์ result ๋ฆฌ์คํธ์ ์ ์ฅ
4. ๋ฆฌ์คํธ ์ ๋ ฌํ๋ค ์ต์๊ฐ ์ถ๋ ฅ

์ด๋ ๊ฒ ์ฐ๋ ๊ธฐ ์ฝ๋๋ฅผ ์ง๋๋๋๊ฑธ๊น ์ถ๋ค..
๊ทธ๋๋ ๋ฉ์น๋ ๋๊น์ง ๋ชปํ์์ง๋ง ์ด๊ฑด ๋๊น์ง ํ์๋ค.
์ฒด๊ฐ์ ๋ฉ์น๊ฐ ๋์ด๋ ค์ ๋๋ฐ ๋ฌธ์  ์ ๊ทผ์ ์๋ชปํด์ ๊ทธ๋ฐ๋ฏ ..
<br/>

## ๐ต Ref
> 