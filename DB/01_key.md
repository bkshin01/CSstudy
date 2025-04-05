# ✔️ 키(Key)

## Super Key에 대해서 말해 보세요.
슈퍼키는 각 row를 유일하게 식별할 수 있는 하나 또는 그 이상의 속성들의 집합입니다. 유일성만 만족하면 슈퍼키가 될 수 있습니다.

<br>

## Candidate Key는?
후보키는 슈퍼키 중에서 더이상 쪼개질 수 없는 최소성을 가지는 키들을 말합니다. 유일성과 최소성을 모두 만족해야 합니다.

<br>

## Primary Key는?
기본키는 후보키 중 선택한 메인 키로써, 각 row를 유일하게 식별하는 컬럼 또는 컬럼의 집합을 말합니다.<br>
따라서 기본키는 Null을 가질 수 없습니다.

<br>

## Alternate Key는?
여러 후보 키들 중 기본키로 선택되지 못한 나머지 후보키들을 말합니다.

<br>

## Foreign Key에 대해서 설명해 보세요.
외래키는 다른 테이블의 기본키를 참조하는 키입니다.<br>
외래키 필드의 값은 외래키가 참조하는 기본키의 필드값과 동일하거나 Null이어야 합니다.

<br>

## Composite Key는?
두개 이상의 컬럼을 키로 지정하는 것을 말합니다.<br>
기본키는 한 테이블에 한 개만 존재할 수 있지만, 꼭 한 테이블에 한 컬럼만 기본키로 지정할 수 있는 것은 아닙니다.

<br>

```
mysql> create table test (
    -> id bigint primary key,
    -> seq bigint primary key);
ERROR 1068 (42000): Multiple primary key defined
```
위의 경우는 기본키를 두 개 지정하여 에러가 발생했지만, 아래의 경우는 두 개의 컬럼을 함께 기본키로 지정하여 오류가 발생하지 않습니다.

```
mysql> create table test (
    -> id bigint not null,
    -> seq bigint not null,
    -> primary key(id, seq)
    -> );
Query OK, 0 rows affected (0.01 sec)
```
