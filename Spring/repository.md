# repository란 무엇일까
먼저 repository란 데이터베이스 테이블에 접근하는 메서드들을 사용하기 위한 인테페이스이다.

ex) CRUD 등을 사용하기 위해서 어떻게 처리할지 정의한다


코드 : ``public interface UserRepository extends JpaRepository<User, Long>``
-  ``JpaRepository``는 JPA에서 제공하는 기본 CRUD 기능 모음이다
- ``<user, long>``는 user : 엔티티를 다룰 것인지, long : 엔티티의 PK 타입이 무엇인지를 나타낸다
> **PK란?** 기본키를 의미한다.

- 자동제공 되는 기능들(JpaRepository 덕분에 쓸 수 있다)
    - ``save(User user)`` : 새로운 유저 저장
    - ``findById(Long id)`` : ID로 유저 검색 
    - ``findAll()`` : 모든 유저 조회
    - ``delete(User user)`` : 유저 삭제