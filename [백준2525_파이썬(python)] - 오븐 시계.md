## π΄ λ¬Έμ 
> [μ€λΈ μκ³](https://www.acmicpc.net/problem/2525)


<br/>

## π‘ Sol
```python
A, B = map(int, input().split())
C = int(input())

hours = int((A*60+B+C)/60)
if(hours>23):
    hours = hours-24
minutes = int((A*60+B+C)%60)
print(hours, minutes)
```
<br/>

## π’ νμ΄
μ°λ¦¬ νμ μ κΈ°λ€μ΄ νΈλ λ¬Έμ ..
μ€λΈμκ³λ μλλ° μΈκ³΅μ§λ₯ μκ³λ μλ€...

<br/>

## π΅ Ref
> 