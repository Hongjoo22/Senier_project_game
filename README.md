# InsideTheDark
숭실대학교 졸업작품 멀티 공포 게임

## 기간 (약 10개월)
2020.08.01 ~ 2021.05.23

## 분업
이홍주, 윤민근, 박주연
3명 모두 기획, 디자인, 모델링, 애니메이션, 개발, 최적화에 기여하였습니다.

## 사용 기술
* 플랫폼: Unity 3D
* 형상관리: GitLaB, Github DeskTop
* 3D Modeling: Maya
* network: photon2 assets
* 기타 UI 작업 : photoshop
* 사용언어: C#
* 기타모델링: 무료 및 유료 asset 사용

## 팀이름 Tri
세명이라는 뜻의 Triple, '시도하다' 단어 Try의 발음을 따와 Tri(트라이)

## 작품 개요
좀도둑과 집주인을 나눠서 플레이하는 죽음의 술래잡기, 2인 멀테 공포게임(러닝타임 약 15분~20분)
좀도둑은 집주인의 눈을 피해 집에 있는 3가지의 랜덤 물건을 훔쳐 달아나면 이기고
집주인은 좀도둑이 물건을 훔쳐 달아나기 전에 3번 찔러 죽이면 이기는 게임입니다.

## 기획 의도
졸업전시회는 보통 2명 이상씩 오는데 둘이서 재밌게 즐기다 갈 수 있는 게임을 만들어 보고 싶었습니다.
또한 네트워크가 어떤식으로 작동이 되고 적용이 되는지 공부하고자 하는 취지에서 멀티 공포 게임을 기획하였습니다.

## 구현한 주요 기능
<공통>
* 멀티 플레이를 위한 랜덤 방 생성 및 join 하기
* 모든 기능은 Photon RealTime을 활용하여 개발하였습니다.
* 캐릭터(플레이어) 선택 및 이름 작성
* 걷기, 달리기, 웅크리기, 웅크리며 걷기, 손전등 키고 끄기
* 특정 구간에 도달하면 해당 배경소리 듣기 

<좀도둑>
* 게임 시작 시 랜덤 물건 3가지 UI 실루엣으로 제공하기
* 문 열고 닫기 및 열쇠, 물건 획득 기능
* 스킬1(먹물 뿌리기: 집주인 UI 시야 방해 하기)
* 스킬2(투명화: 5초동안 좀도둑 캐릭터 안보이게 하기)
* 맞으면 3초 질주 기능
* 물건을 다 훔칠 시 도망치라는 문구 뜨기

<집주인>
* 마우스로 조정하여 화면 가운데를 클릭하면 때리는 기능
* 달릴 때 체력바 소진되는 기능
* 좀도둑이 물건을 훔칠때마다 맵에 해당 물건의 위치 표시
* 물건을 다 훔칠 시 빨리 잡으라는 문구 뜨기

## 내가 작품에 기여한 부분(주요 기능만)
* 기획: 시스템과 밸런스 부분에서 구체적인 의견 덧붙이기
* 모델링 및 애니메이션: 좀도둑 의상 제작, 애니메이션 및 상호작용 작업
* 네트워크: Photon을 사용하여 멀티플레이 방 구성 및 각 플레이어 간 RealTime 구성(문 열기, 손전등, 스킬쓰기, 찌르기 등)
* 게임 맵: 2층 구조 생성 및 인테리어, 전반적인 최적화 작업(occlusion culling 및 카메라 범위 조정)
* 포토샵: 게임설명, 키세팅, 캐릭터 설명 등 게임 진행에 필수적인 내용 UI 작업
* 버그 수정: 낙사문제를 리스폰으로 해결하였습니다.

## 내가 고민했던 부분(일부)
1. Collide를 촘촘하게 하여도 물리 가속도에 법칙에따라 collide가 통과되는 현상이 있었습니다. 
충돌 감지를 연속적으로 하기위해 해당 캐릭터 Rigidbody의 Collision Detection을 Continuous로 변경하였으나 CPU에 부담을 준다고 판단하여
물체의 속도를 줄이고, 만약 떨어지면 초기 위치로 리스폰하는 식으로 해결하였습니다.

2. photon을 사용하는 기능을 구현할 때 종종 상대방의 움직임을 컨트롤하는 문제가 있었습니다. 
해당 문제의 원인은 photon의 경우 해당 게임 신에 있는 리소스 폴더 안에 있는 프리팹들을 인식했기 때문에 
해당 프리팹(플레이어)이 자신의 Photonview인지 아닌지를 확인하는 작업을 추가하였습니다.

## 성과
졸업전시회 3일동안 하루에 130명씩 약 400분들이 체험셨습니다.

## 배운점
1. 기획을 시스템 단위로 더 구체적으로 해야 나중에 개발할 때 편하다는 것을 깨달았습니다.
2. 모든 프로젝트를 gitlab에 올려서 형상관리를 하는 것이 아닌 소스코드만 공유하는 방식이 효율적이라는 것을 깨달았습니다
3. 모든 과정이 처음이었지만 팀원끼리 서로 소통을 많이 하고 시행착오를 많이 겪어보면 좋은 성과를 얻을 수 있다는 것을 깨달았습니다.

## 인게임 사진
![storyline](https://user-images.githubusercontent.com/65024497/174811771-06e88a0d-bd96-42d3-bf66-cdc429820fc3.png)
![key_setting](https://user-images.githubusercontent.com/65024497/174811832-f46ea80f-1097-4805-905b-bdfeb80b6638.png)
![storytelling](https://user-images.githubusercontent.com/65024497/174812393-cc8c7b3a-d3d0-41fd-af19-2f65eb485305.png)

<캐릭터 선택창>
![11](https://user-images.githubusercontent.com/65024497/174815004-2c6e5b92-fcd6-41c8-b959-fa5fb5f0f00c.jpg)
<좀도둑 UI>
![222](https://user-images.githubusercontent.com/65024497/174815012-95ec4dd3-d500-4d19-9b3d-fe751df7c9d5.jpg)
<집주인 UI>
![333](https://user-images.githubusercontent.com/65024497/174815017-bf899dac-8118-457f-bd75-db55215494ca.jpg)
![555](https://user-images.githubusercontent.com/65024497/174815033-1ec824c2-9929-4be2-be8c-9b97fdf81768.jpg)
<실제 졸업 전시 플레이 사진>
![666](https://user-images.githubusercontent.com/65024497/174815065-396129a8-7317-4354-a0c1-59791962b908.png)


