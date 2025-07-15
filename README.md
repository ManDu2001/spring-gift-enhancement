# spring-gift-enhancement

### 1단계 구현사항
-[x] application.properties, build.gradle 수정
-[x] [Domain] 기존 domain 클래스인 Member, Product, WishList를 JPA 어노테이션을 적용
-[x] [Repository] 기존 Repository 인터페이스(총 3개 - Member, Product, WishList) 내용 삭제후, Spring Data JPA의 JpaRepository를 상속 및 필요에 따라 커스텀 쿼리 메서드 작성
-[x] [Service] 기존 Service 클래스(총 3개 - Member, Product, WishList)에서 Repository 호출시 사용되는 함수 이름 변경 및, Repository 함수 파라미터에 맞게 전처리 작업 추가
-[x] [Dto] WishListRepository 에서 반환하는 WishList 를 편리하게 바꿀 수 있도록 WishListResponseDto에 생성자 추가
-[x] [Test] WishListRepository에 대한 테스트 추가
