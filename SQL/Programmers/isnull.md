# IS NULL

π’ νλ‘κ·Έλλ¨Έμ€μ [SQL ν€νΈ](https://programmers.co.kr/learn/courses/30/parts/17045)λ₯Ό ν΅ν΄ μ°μ΅νμ΅λλ€.

### μ΄λ¦μ΄ μλ λλ¬Όμ μμ΄λ
```sql
SELECT ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NULL
```

### μ΄λ¦μ΄ μλ λλ¬Όμ μμ΄λ
```sql
SELECT ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NOT NULL
```

### NULL μ²λ¦¬νκΈ°
```sql
SELECT ANIMAL_TYPE, IF(NAME IS NULL, 'No name', NAME), SEX_UPON_INTAKE
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
```