# SELECT

๐ข ํ๋ก๊ทธ๋๋จธ์ค์ [SQL ํคํธ](https://programmers.co.kr/learn/courses/30/parts/17042)๋ฅผ ํตํด ์ฐ์ตํ์ต๋๋ค.

### ๋ชจ๋  ๋ ์ฝ๋ ์กฐํํ๊ธฐ
```sql
SELECT * FROM ANIMAL_INS ORDER BY ANIMAL_ID;
```

### ์ญ์ ์ ๋ ฌํ๊ธฐ
```sql
SELECT NAME, DATETIME FROM ANIMAL_INS ORDER BY ANIMAL_ID DESC;
```

### ์ํ ๋๋ฌผ ์ฐพ๊ธฐ
```sql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION = "Sick"
ORDER BY ANIMAL_ID;
```

### ์ด๋ฆฐ ๋๋ฌผ ์ฐพ๊ธฐ
```sql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION != "Aged"
ORDER BY ANIMAL_ID;
```

### ๋๋ฌผ์ ์์ด๋์ ์ด๋ฆ
```sql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
```

### ์ฌ๋ฌ ๊ธฐ์ค์ผ๋ก ์ ๋ ฌํ๊ธฐ
```sql
SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME, DATETIME DESC;
```

### ์์ n๊ฐ ๋ ์ฝ๋
```sql
SELECT NAME
FROM ANIMAL_INS
WHERE DATETIME = (SELECT MIN(DATETIME) FROM ANIMAL_INS);
```


