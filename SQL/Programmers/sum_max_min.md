# SUM, MAX, MIN

๐ข ํ๋ก๊ทธ๋๋จธ์ค์ [SQL ํคํธ](https://programmers.co.kr/learn/courses/30/parts/17043)๋ฅผ ํตํด ์ฐ์ตํ์ต๋๋ค.

### ์ต๋๊ฐ ๊ตฌํ๊ธฐ
```sql
SELECT MAX(DATETIME) AS "์๊ฐ"
FROM ANIMAL_INS;
```

### ์ต์๊ฐ ๊ตฌํ๊ธฐ
```sql
SELECT MIN(DATETIME) AS "์๊ฐ"
FROM ANIMAL_INS;
```

### ๋๋ฌผ ์ ๊ตฌํ๊ธฐ
```sql
SELECT COUNT(ANIMAL_ID) AS "count"
FROM ANIMAL_INS;
```

### ์ค๋ณต ์ ๊ฑฐํ๊ธฐ
```sql
SELECT COUNT(DISTINCT NAME)
FROM ANIMAL_INS
WHERE NAME != "NULL";
```