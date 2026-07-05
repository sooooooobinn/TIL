# 문자열 자르기
- SUBSTR(Oracle)<br>

    문자열을 자르는 함수

    ```
    ex)
    SUBSTR(NAME, 1, 2)
    ```
    > NAME 컬럼의 1번째부터 2번째까지의 2글자를 출력한 결과

- SUBSTRING, LEFT, RIGHT(MySQL)<br>

    SUBSTR과 동일한 함수

    - SUBSTR
    ```
    ex)
    SUBSTRING(NAME, 1, 2)
    ```
    > NAME 컬럼의 1번째부터 2번째까지의 2글자를 출력한 결과


    - LEFT
    ```
    ex)
    LEFT(NAME, 1)
    ```
    >NAME을 왼쪽부터 1글자 출력

    - RIGHT
    ```
    ex)
    RIGHT(NAME, 1)
    ```
    >NAME을 오른쪽부터 1글자 출력