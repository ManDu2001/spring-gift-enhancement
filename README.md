# spring-gift-enhancement

### 1단계 구현사항
-[x] application.properties, build.gradle 수정
-[x] [Domain] 기존 domain 클래스인 Member, Product, WishList를 JPA 어노테이션을 적용
-[x] [Repository] 기존 Repository 인터페이스(총 3개 - Member, Product, WishList) 내용 삭제후, Spring Data JPA의 JpaRepository를 상속 및 필요에 따라 커스텀 쿼리 메서드 작성
-[x] [Service] 기존 Service 클래스(총 3개 - Member, Product, WishList)에서 Repository 호출시 사용되는 함수 이름 변경 및, Repository 함수 파라미터에 맞게 전처리 작업 추가
-[x] [Dto] WishListRepository 에서 반환하는 WishList 를 편리하게 바꿀 수 있도록 WishListResponseDto에 생성자 추가
-[x] [Test] WishListRepository에 대한 테스트 추가

### 2단계 구현사항
-[x] [Repository] WishListRepository에 findAllByMember 이름을 갖지만, 파라미터로 Pageable을 받는 메소드 오버로딩 (단, ProductRepository에는 findAll 을 사용하고, 이는 JPA에서 기본 제공하므로 선언하지 않음)
-[x] [Service] ProductService 인터페이스와 이에 대한 구현체 ProductServiceImpl에서 기존 List를 반환하는 searchAllProducts 에 Page 반환 및 Pageable 파라미터로 요구하도록 변경
-[x] [Service] WishListService 인터페이스와 이에 대한 구현체 WishListServiceImpl에서 기존 List를 반환하는 getWishList 에 Page 반환 및 Pageable 파라미터로 요구하도록 변경
-[x] [Controller] ProductController의 searchAllProducts와 ProductAdminController의 productList에서 페이지네이션 사용하도록 변경
-[x] [Controller] WishListController의 getWishList에서 페이지네이션 사용하도록 변경
-[x] [Resource/admin] 상품 관리자 페이지에서 페이지네이션 기반 html, css 수정 
-[x] [Test] 기존 WishListTest에서 WishListController 사용하는데 List -> Page 변경에 따른 테스트 코드 원활히 동작하도록 변경
