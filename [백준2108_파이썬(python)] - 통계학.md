## ๐ด ๋ฌธ์ 
> [ํต๊ณํ](https://www.acmicpc.net/problem/2108)


<br/>

## ๐ก Sol
```python
import sys
N = int(input())
N_List = []
mode_List = [0]*8001
mode = []

for _ in range(N):
    N_List.append(int(sys.stdin.readline()))

N_List.sort()

for i in N_List:
    mode_List[i+4000] += 1
for i in range(len(mode_List)):
    if(mode_List[i] == max(mode_List)):
        mode.append(i)

print(round(sum(N_List)/N))
print(N_List[len(N_List)//2])
if(len(mode) == 1):
    print(mode[0]-4000)
else:
    print(mode[1]-4000)
print(max(N_List)-min(N_List))

```
<br/>

## ๐ข ํ์ด
ํ๋ฒ์ ๋ง์๋ค !!
์ฐ์ ํ๊ท , ์ค์๊ฐ, ๋ฒ์๋ ์ฝ๊ฒ ๊ตฌํ ์ ์์๋ค.
๋ฌธ์ ๋ ์ต๋น๊ฐ์ด์๋๋ฐ ํฌ๊ธฐ๊ฐ ์ฃผ์ด์ก๊ธฐ ๋๋ฌธ์ ํฌ๊ธฐ๊ฐ 8001์ธ list๋ฅผ ๋ง๋ค๊ณ , ๊ณ์ ์ ๋ ฌ์ ์ฌ์ฉํด ์ซ์๋ฅผ ์นด์ดํธ ํด์ค๋ค.
๊ทธ ๋ค์ ๋ฐ๋ชฉ๋ฌธ์ ์ฌ์ฉํด ์ต๋น๊ฐ์ธ ์๋ฅผ mode๋ผ๋ ์๋ก์ด list์ ์ถ๊ฐํ๋ค mode์ ๊ฐ์์ ๋ฐ๋ผ ์ถ๋ ฅ์ ๋ฌ๋ฆฌํด์ฃผ๋ฉด ๋๋ค.
์ฌ์ค .count()์ ์ฌ์ฉ๋ฒ์ ๋ชฐ๋ผ์ ์์ผ๊ธฐ ๋๋ฌธ์ ํ๋ฒ์ ๋ง์ ๋ฌธ์ ์ธ๋ฐ .count()๋ฅผ ์ฌ์ฉํ๋ฉด ์๊ฐ ์ด๊ณผ๊ฐ ๋ฐ์ํ๋ค๊ณ  ํ๋ค. 
์๊ฐ ์ด๊ณผ๋ฅผ ๋ฐ์์ํค์ง ์๊ณ  ๊น๋ํ๊ฒ ํด๊ฒฐํ๋ ค๋ฉด Counter์ด๋ผ๋ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ฌ์ฉํ๋ฉด ๋๋ค. (์ด์ฝํ์ collections์ ๊ดํ ๋ด์ฉ์ด ์๋๋ฐ ์ ๋ฆฌํด์ผ๊ฒ ๋ค.)

<br/>

## ๐ต Ref
> https://velog.io/@jaenny/%EB%B0%B1%EC%A4%80-2108-%ED%86%B5%EA%B3%84%ED%95%99-Python%ED%8C%8C%EC%9D%B4%EC%8D%AC