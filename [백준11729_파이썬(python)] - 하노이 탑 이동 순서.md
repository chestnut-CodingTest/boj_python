## π΄ λ¬Έμ 
> [νλΈμ΄ ν μ΄λ μμ](https://www.acmicpc.net/problem/11729)


<br/>

## π‘ Sol
```python
N = int(input())

def hanoi(N, start, end):
    if (N == 1):
        print(start, end)
        return
    hanoi(N-1, start, 6-start-end)
    print(start, end)
    hanoi(N-1, 6-start-end, end)

print(2**N-1)
hanoi(N, 1, 3)
```
<br/>

## π’ νμ΄
μ΄λ €μμ λλ¬Ό νλ°κ°μ§ νλ¦¬λ€κ° νμ΄λ₯Ό κ²μν΄λ΄€λ€.

νλΈμ΄μ νμ μ¬κ·λ‘ νννλ €λ©΄ λ€μ 3λ¨κ³λ‘ νμ΄ κ°λ₯νλ€.
1. n-1κ°μ μνμ 1λ² λ§λμμ 2λ² λ§λλ‘ μ΄λ
2. λ¨μ 1κ°μ μνμ 1λ² λ§λμμ 3λ² λ§λλ‘ μ΄λ
3. 3λ¨κ³ μμλ λ€μ n-1κ°μ μνμ 2λ² λ§λμμ 3λ² λ§λλ‘ μ΄λ
 
<br/>

## π΅ Ref
> https://study-all-night.tistory.com/6