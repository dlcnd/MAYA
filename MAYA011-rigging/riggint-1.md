# Rigging 01
* 애니메이션하기 전 구조를 짜서 원하는대로 움직이게끔 만드는 작업
* 모델링 이후 작업.
* Parent 구조를 이용해서 작업.
* Outliner를 이용해서 짠다.

* Object를 전부 정리가 된 상태에서 작업하는 게 중요하다(!!)
  * Freeze
  * History Delete
  * Object name
  * Group
  * Pivot 위치 

* Controller > Joint > Object (Constraint Parent로 연결되어 있다)


### Parent 구조
* Outliner상황에서 그룹이나 오브젝트 간 상하관계를 갖는 걸 Parent라고 한다.
  #### Parent
    * 자식을 추가 : 자식 선택 > 부모 선택 > P
    * 자식을 빼내고 싶을 때: 자식 선택 후 shift + p
    * 자식의 pivot이 부모를 따라간다☆☆☆
  #### Constraint Parent(Tool을 이용한 Parent 관계)
    * 부모를 먼저 선택 후 자식을 선택 constraint> parent
    * 연결을 해제하고 싶으면 자식이 가지고 있는 Parent Node 삭제
    * Parent보다 귀속력이 강하다.
    
    
### Joint
  * Skeleton > create joints
    * 절대 perspective view에서 작업하지 않는다
    
  * 클릭해서 만든 후 enter로 완성
    * 가장 먼저 찍은 joint가 parent
    * object는 자식으로 들어갈 수 없다. 그래서 constraint parent로 짜야 한다.
    
  * 이름 짓기 - prefix hierarchy
    * joint의 상하구조 뿐만 아니라 모든 그룹 등에서 쓸 수 있다.
    * modify > Prefix Hierarchy names
    * 이름을 고치고 싶을 땐 modify> Search and replace name
    
  * controller만들기
    * create>NURBS primitives>circle
    * 관절마다 만들어 준다.
    * 가장 아래에는 main controller를 꼭 두어야 한다.
     * controller를 다 위치시킨 후(더 이상 수정할 게 없어진 후)에는 반드시 freeze, delete History!!
    
  * Object와 Joint, Controller에 각각 레이어를 할당
  * Object &rarr; Joint &rarr; Controller
  
  
  * Joint Size 조절하기
    * Display > animation> joint size
    
  * 작업이 끝나면 히스토리 삭제, freeze
