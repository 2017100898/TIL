# GROUP BY

๐ข ํ๋ก๊ทธ๋๋จธ์ค์ [SQL ํคํธ](https://programmers.co.kr/learn/courses/30/parts/17044)๋ฅผ ํตํด ์ฐ์ตํ์ต๋๋ค.

### ๊ณ ์์ด์ ๊ฐ๋ ๋ช ๋ง๋ฆฌ ์์๊น
```sql
SELECT ANIMAL_TYPE, COUNT(ANIMAL_ID) AS 'count'
FROM ANIMAL_INS
WHERE ANIMAL_TYPE IN ('Cat', 'Dog')
GROUP BY ANIMAL_TYPE
ORDER BY ANIMAL_TYPE;
```

### ๋๋ช ๋๋ฌผ ์ ์ฐพ๊ธฐ
```sql
SELECT NAME, COUNT(ANIMAL_ID) AS COUNT
FROM ANIMAL_INS
WHERE NAME != 'Null'
GROUP BY NAME HAVING COUNT >= 2
ORDER BY NAME;
```

### ์์ ์๊ฐ ๊ตฌํ๊ธฐ(1)
```sql
SELECT HOUR(DATETIME) AS HOUR, COUNT(ANIMAL_ID) AS COUNT
FROM ANIMAL_OUTS
GROUP BY HOUR(DATETIME) HAVING HOUR >= 9 AND HOUR <20
ORDER BY HOUR(DATETIME);
```
