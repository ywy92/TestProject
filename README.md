# 목적
**마스터 브랜치랑 다른 브랜치의 파일 수가 다를 때 어떻게 관리 해야 하는가? (다르게 유지하고 싶음)**

# 계기
스터디 모임에서 사용하는 깃허브 레포지토리와 관련되서 화제가 있었다.    
그래서 master branch와 다른 branch들의 스냅샷을 어떻게 하면 다르게 잘     
관리할 수 있을까?

# 테스트 방법 1(실패...)
1. 테스트에 사용할 java project를 생성
2. 패키지 두 개를 생성 후 목적 없는 파일을 생성
3. master branch에 push request -> merge
4. master branch를 기준으로 test1 branch 생성
5. test1 branch에서 두 개의 패키지 중 한 개의 패키지를    
   삭제 후 push request -> merge
6. test1 branch에서 master branch에 pull request -> merge
7. 결과를 확인한다.

# 테스트 방법 2(성공)
1. 다시 master 패키지를 생성
2. master branch에 push request -> merge
3. master branch를 기준으로 test2 branch 생성
4. test2 branch에서 패키지를 생성 후 push request -> merge
6. test2 branch에서 master branch에 pull request -> merge
7. test1 branch에서 test1 패키지 외 제거 후 master branch    
   pull request -> merge
8. 결과를 확인한다.

# 테스트 방법 3(실패)
1. test2 branch에서 파일 추가 push request -> merge
2. test2 branch에서 master branch에 pull request -> merge
3. test1 branch에서 master branch를 pull
4. test1 workingTree에 test2 branch가 추가한 파일이 pull
5. 결과를 확인한다.
6. test1 branch에서 master, test2 package 제거 후    
   master branch에 pr merge하면 master branch에 반영됨

# 테스트 방법 4
1. 브랜치 단위가 아닌 협업(다른계정) 상황으로 범위를 넓임
2. ywy92계정과 ywyi1992계정 협업
3. 내일... 해야겠다...

