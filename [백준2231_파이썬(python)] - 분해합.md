## ๐ด ๋ฌธ์ 
> [๋ถํดํฉ](https://www.acmicpc.net/problem/2231)


<br/>

## ๐ก Sol
```python
N = int(input())
constructor = []

for i in range(1, N+1):
  i_list = list(map(int, str(i)))
  if(N == i + sum(i_list)):
    constructor.append(i)
    break

if(len(constructor) == 0):
  print(0)
else:
  print(constructor[0])


```
<br/>

## ๐ข ํ์ด
input ๋ฒ์๊ฐ 1๋ถํฐ 1000000 ๊น์ง๋ผ์ ๋ฐ๋ณต๋ฌธ์ ๋๋ฆด์๊ฐ์ ๋ชปํ๋๋ฐ ์๊ด์ด ์์๋ค.(์๊ฐ๋ณต์ก๋ ๊ณต๋ถํด์ผ๋ ๋ฏ)
์ํผ.. ๋ง๊ทธ๋๋ก 1๋ถํฐ ๋ชจ๋  ์๋ ฅ๋ฐ์ N๊น์ง ๋ชจ๋  ๊ฒฝ์ฐ์์๋ฅผ ๊ณ์ฐํ์ฌ ์์ฑ์๋ผ๋ฉด ๋น ๋ฆฌ์คํธ์ ๋ฃ์ด์ฃผ๋ ์์ผ๋ก ์ฝ๋๋ฅผ ์ง๋ณด์๋ค.
๋ง์ง๋ง์๋ ๋ฆฌ์คํธ์ ๊ธธ์ด์ ๋ฐ๋ผ ์ถ๋ ฅํ๋ ๋ด์ฉ์ด ๋ฌ๋ผ์ง์ ์๊ฒ ํ๋ค.
์ฝํ ์ค๋นํ ๋ ํ๋  ์ผ์ด์ค๋ฅผ ์ฐพ์๋ณด์ง ์๋๊ฒ์ด ์ข๋ค๊ณ  ์๊ฐํด(์ค์  ์ฝํ์์๋ ํ๋ ์ผ์ด์ค๋ฅผ ์ฃผ์ง ์๋๋ค.) ์๋ ํ๊ป ๋ฐ๋ก๋ฅผ ์ฐพ์์ผ๋ ๊ฒฐ๊ตญ ์ง๋ฌธํญ์์ ๋์์ ๋ฐ์
์ฌ์ง์ด ๋ฐ๋ก๋ ๊ต์ฅํ ์ฌ์ด๋ถ๋ถ์์ ๋ํ๋ฌ๋ค.
์ด๋ฐ๋น

<br/>

## ๐ต Ref
> 