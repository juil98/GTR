# Git 오류 
<!--22.12.27.Tue -->


## Username for 'https://github.com'
<!--작성일 : 22.12.27.Tue -->
### 요약
1. 깃허브 약관 변경으로 인하여 비밀번호를 토큰으로 추가 생성하여 기입하면 해결.
2. 깃허브 로그인 
3. 세팅
4. developer settings 
5. Personal Acess Token 생성
### 주의점
- 토큰은 만들어지면 **1번만** 보여주기에 따로 복사해두거나
- 필요할때마다 재발급하자.


---
## git에서의 대소문자 에러 
<!--작성일 : 22.12.27.Tue -->
### 요약
git은 기본적으로 파일명 또는 폴더명의 대소문자를 구분하지 못한다.
그런데 만약 프로젝트의 모든 첫글자가 대문자인 상황에 한개의 파일을 소문자로 설정한채 commit push를 했다..?
잠시후 팀원들로 부터 생명의 위협을 느껴도 겸허히 받아들이면 된다..
물론 나는 모든 파일이 초기 셋팅 상태로 돌아가버렸지만 위협을 주진 않았다...(사실 너무 당황스러워서 위협줄 생각조차 못함).
이참에 Git 공부할수 있어서 오히려 좋아.
그럼 이런 소문자 공격을 받았을 때 어떻게 하면되는지 알아보자.!

---
1. git config --global core.ignorecase
=> git아 제발 대문자랑 소문자 무시하지 말아줘....
1. git rm -r --cache .
=> 저장된 캐시를 모두 지워버린다. 사실 처음에는 아무것도 모르고 이 명령어를 따라 쳤었는데 나중에 알고보니 로컬에는 파일을 남기지만 원격저장소에는 파일을 모두 삭제해버리는 어마무시한 명령어였다.. 진작 알았다면 치기전에 이백만번 고민했을듯... 여튼 어쩔수 없다 용기가 없다면 나는 대소문자 지옥에 빠져서 돌아오지 못할수도 있으니... 일단 친다.
1. git add .
=> add 하고 (여기서 무시하지말라고하긴했지만 혹시 모르니까 슬쩍 소문자를 대문자로 바꿔서 add했다. 만약을 대비해서 나쁠건 없으니까)
1. git commit -m "remove all cache"
=> 원격저장소에 다 삭제했다고 하니까 벌벌떨면서 빨리 커밋하기!


Source : [https://velog.io/@4_21ee/TIL-27-Git찮아도-알아둬야할-Git명령어](https://velog.io/@4_21ee/TIL-27-Git찮아도-알아둬야할-Git명령어)


---

## ! [rejected] main -> main (fetch first)
<!--작성일 : 22.12.27.Tue -->
### 요약
1. 저장소 간에 동기화를 해주면 해결
   - git pull --rebase origin main

2. 강제로 push 하면 해결 되긴 하지만, 원격 저장소의 데이터가 소실 될 우려가 있다.
   - git push origin +main


Source : [https://byul91oh.tistory.com/231](https://byul91oh.tistory.com/231)


---

