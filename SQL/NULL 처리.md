# NULL 처리

### IFNULL(MySQL)
해당 컬럼의 값이 NULL을 반환할 때, 다른 값으로 출력할 수 있도록 하는 함수

> ```
>ex)
>SELECT IFNULL(NAME, "김수빈")
>FROM STUDENT
>```
>NAME 컬럼의 값이 NULL이라면 "김수빈"이라는 값으로 대체

MySQL 환경에서는 IFNULL을 사용한다.

- Oracle 환경 : NVL
- MS SQL 환경 : ISNULL

다 같은 의미로 사용되지만 환경에 따라 사용하는 함수가 다르다.

### COALESCE(모든 DBMS 사용 가능)
지정한 표현식들 중에 NULL이 아닌 첫 번째 값을 반환한다.

>```
>ex)
>SELECT COALESCE(Column1, Column2, Column3)
>FROM 테이블명
>```
>지정한 3개의 Column 중에 NULL 값이 아닌 첫 번째 값 반환