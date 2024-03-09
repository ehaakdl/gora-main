querydsl repository 객체 모듈 분리 실패
- JPAQueryFactory 객체 주입 보다 repository 객체를 참조하는 클래스가 먼저 호출됨
순서를 임의로 조정하는 방법보단 처음 상태 그대로 두는것이 좋을거 같음