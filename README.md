# 목적
**마스터 브랜치랑 다른 브랜치의 파일 수가 다를 때 어떻게 관리 해야 하는가? (다르게 유지하고 싶음)**

# 계기
스터디 모임에서 사용하는 깃허브 레포지토리와 관련되서 화제가 있었다.    
그래서 master branch와 다른 branch들의 스냅샷을 어떻게 하면 다르게 잘     
관리할 수 있을까?

# 테스트 방법 1
1. 테스트에 사용할 java project를 생성
2. 패키지 두 개를 생성 후 목적 없는 파일을 생성
3. master branch에 push requst -> merge
4. master branch를 기준으로 test1 branch 생성
5. test1 branch에서 두 개의 패키지 중 한 개의 패키지를    
   삭제 후 push requst -> merge
6. test1 branch에서 master branch에 pull requst -> merge
7. 결과를 확인한다.




