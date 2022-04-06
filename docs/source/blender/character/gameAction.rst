GameAction
------------

.. code-block:: console

Pose Library
$포즈 라이브러리에는 현재 레이어 본의 정보를 저장한다.
저장: 저장할 본을 선택하고 '+' 버튼을 누른다
적용: 돋보기 버튼(선택한 본만 적용된다, 아무것도 선택하지 않으면 전체 본에 적용된다
#Pose 미러복사(오른 클릭 Copy, Paste X-Flip Pose
뼈의 이름 끝에 .L, .R 붙여야된다 
#Pose 자동선택 // Ctrl + L + MouseWheel(순차적으로 선택된다
#라이브러리 저장 안될 때 // 회색방패 아이콘을 켜고 저장한다.
#Shift + E :: pose.breakdown, DopeSheet에서는 Set Keyframe Extrapolaton(보외법
※ 보외법 또는 외삽은 수학에서 원래의 관찰 범위를 넘어서서 다른 변수와의 관계에 기초하여 변수의 값을 추정하는 과정.
#Child Of Constraint 에서 Set Inverse 시 부모의 위치로 이동하지 않는 경우 
// 위치를 원점으로 옮긴다음 실행해본다Select to Cursor(원점
#Reset Pose 문제(모션캡쳐용 T-포즈를 키애니용으로 변환할 때 필요
포즈를 잡은 상태에서 메쉬모드로 나와 메쉬를 선택한다
Modifier에서 Armature를 Copy한 후 원래 Armature Modifier를 'Apply'한다음
포즈모드로 들어가 Apply Reset Pose한다
#IK 로테이션 문제
=Edit 모드에서 Bone을 꺽어야한다(포즈모드에서하면 안됨
#손과 발의 IK 본은 Root본에 Parent하고 Target은 힙본에 한다

.. image:: https://user-images.githubusercontent.com/30430227/159687653-343efa55-ff03-4cf0-bab5-b5c6f18788a1.png
.. image:: https://user-images.githubusercontent.com/30430227/159688362-0e0fa0b6-2005-447d-8fce-0003cf61b4d6.png

.. image:: https://user-images.githubusercontent.com/30430227/159687676-75d4d8d0-cd34-4a62-b95c-88093ef33219.png
.. image:: https://user-images.githubusercontent.com/30430227/159687711-50b8e887-9f27-49fb-af8b-cc534b6d59a9.png


>>> Timeline Editor - 키프레임 마름모 컬러 바꾸기 단축키 'R'
Marker - M > Ctrl-M(Rename
Curve Editor - 특정 요소의 커브만 보이게 Shift-H, 모두 나타나게 Alt-H

>>>툴아이콘 메뉴(기즈모 단축키 설정 E-Move, D-Rotate
Select Mirror 단축키 변경 Alt-M
뼈 선택 이동 '[', ']' 


`Breakdown - 메인키 중간에 키프레임 추가, 예진자 운동`

`Pose Breakdowner 'Shift-E 후 드랙 하거나 수치%입력(모든 변형에 G,R,S-선택' Pose>Inbetweens 참고`

.. image:: https://user-images.githubusercontent.com/30430227/159848870-2f70bd84-4ec6-4142-ae90-634ed4d0d1d1.png


포즈 생성
----------

`저장할 본들을 선택하고 >Create Pose Asset - 손만 선택하면 손만 적용된다`

.. image:: https://user-images.githubusercontent.com/30430227/159226043-3684d1e1-7198-4f35-abae-9f57a4313e25.png
.. image:: https://user-images.githubusercontent.com/30430227/159226084-13ab206c-278c-4d78-bd64-d4027ff39965.png

.. image:: https://user-images.githubusercontent.com/30430227/159225890-b418feca-2fb4-412b-b7bd-beb6e082996a.png

`Thumbnail - Asset Browser > Generate Preview Icon`

.. image:: https://user-images.githubusercontent.com/30430227/159226206-7dd48971-e808-49bb-9497-d75990fd68f4.png

`Interactive Blend - 드랙하면 대상 포즈로 점점 바뀐다, 3D뷰의 프로퍼티에서는 아이콘에서 바로 드랙> FlipPose 미러 `

.. image:: https://user-images.githubusercontent.com/30430227/159226697-a00b30d0-a181-4ac2-a146-f5a21ac9740e.png
.. image:: https://user-images.githubusercontent.com/30430227/159226737-28302d83-1096-4fb9-8a17-b04d59c00689.png

`Active Keying Set - 전체 본 선택 positionRotate> 이후 Available, AutoKey `

.. image:: https://user-images.githubusercontent.com/30430227/159884036-38005e04-48cd-41b1-b726-df6173d1fdf9.png
.. image:: https://user-images.githubusercontent.com/30430227/159884429-e653d970-6bad-4b56-b57a-47fb0fa31f11.png


펀칭 동작 - AutoKey
---------------------

1. Staging - 펀칭 동작은 정면보다 옆 방향이 보기 좋다

.. image:: https://user-images.githubusercontent.com/30430227/159426288-64375e21-fd13-4b05-9cb2-cf31d8cceb63.png

5. Anticipation - 준비자세(기대-사전동작, 동작을 예측하게하는 역할

.. image:: https://user-images.githubusercontent.com/30430227/159428690-0cd8974b-80d6-4b53-b9aa-7c566f7b9389.png

15. 머무는 타이밍 - 스쿼시(준비 동작을 좀 더 크게 준다, break down

18. 공격 - 뒷 발 앞으로 내딛고 > 팔은 몸과 동시에 움직이지 않는다

.. image:: https://user-images.githubusercontent.com/30430227/159431220-796e6b83-f2d8-43c9-a4c3-abb96439099a.png

20. 팔 뻗기 - Squash & Stretch 

`팔 IK 모드로 바꿈 - 스트레치 전에 스쿼시를 준다, 머리와 허리를 살짝 숙인다`

.. image:: https://user-images.githubusercontent.com/30430227/159435615-c8ffd91d-0511-48a3-83f8-188bc028e5bb.png

25. Stretch > 돌아옴, 머리와 허리도 살짝 편다

.. image:: https://user-images.githubusercontent.com/30430227/159435767-6d136c44-a522-4256-88b9-510222c04e2a.png

30. 머리와 허리 다시 살짝 숙인다(반동


점프 동작 
-----------

5. Anticipation - 허리, 머리는 숙이고

.. image:: https://user-images.githubusercontent.com/30430227/159442900-71687f70-2b5f-47c9-922e-615061a7079e.png

10. 머무는 동작 - 준비자세 좀 더(Moving hold, Extream

.. image:: https://user-images.githubusercontent.com/30430227/159443413-6ec5d6eb-9c06-4d85-982c-851f15d5238d.png

13. 점프 - 허리, 머리를 편다

.. image:: https://user-images.githubusercontent.com/30430227/159444086-2d09e149-067a-43f6-8208-86dc8cf61513.png

18. 최고점 

.. image:: https://user-images.githubusercontent.com/30430227/159444645-475910d3-979a-495c-84fa-477c315d53c0.png



활 쏘기
-----


>>> Child Of > Visual Transfrom(현재 위치를 자식의 원점으로, Position/Influence Set Key
>Next Frame > Clear Inverse(부모 영향 벗어남, Influence ->0`


5. Anticipation - 화살/활은 위치를 잡은 후 Child of> Set Inverse

.. image:: https://user-images.githubusercontent.com/30430227/159646040-90ba619d-951b-4232-94ed-c005e021e506.png
.. image:: https://user-images.githubusercontent.com/30430227/159647090-967146b1-7fb1-4a00-842f-411ba9764770.png

15. 시위 당긴다(Moving hold, Extream - 발을 벌린다, 고개를 활 쪽으로 기울인다, 움츠림

.. image:: https://user-images.githubusercontent.com/30430227/159647161-a7fd7a02-f9cb-4d0d-ad26-f9a990265ff4.png

17. 시위를 놓는다 - 오른 팔/머리도 뒤로 젖히고, 몸은 화살에 이끌리듯 살짝 앞으로 나간다(Follow Through. 움츠림 

`화살 > 15-Visual Transform, Clear Inverse , SetKey(Influence > 16-SetKey(Influence:0`

`활현 -반동으로 앞쪽으로 > 22 - 뒤쪽 반동 > 25 - 제자리`

.. image:: https://user-images.githubusercontent.com/30430227/159647182-d4e90683-318d-4ced-927b-3f0e27b36ff8.png
.. image:: https://user-images.githubusercontent.com/30430227/159648277-cf65523a-8f09-47c4-ad7e-10ebd95a0dde.png

25. 팔 내린다, 몸 원래위치로

.. image:: https://user-images.githubusercontent.com/30430227/159649793-5a88c04e-ddd1-4550-9520-34804204213e.png


봉 돌리기
----------

`카메라-Stage >키 pose 생성-Frame by Frame > 키 사이 간격 벌림-Timing > Break down>설득력-Stage`

0. 봉의 위치를 오른손 > Child Of 'hand_fk.R > Set Inverse(손에 붙인다

.. image:: https://user-images.githubusercontent.com/30430227/159819108-e79310fe-5e16-4781-9314-2da86f9401fc.png
.. image:: https://user-images.githubusercontent.com/30430227/159817326-a374356f-59be-46b6-8366-2ebada5c8203.png

1. 기본 자세 

.. image:: https://user-images.githubusercontent.com/30430227/159819248-03b79ab7-99e5-4bd4-826c-53fa649424bf.png

2. 공격 준비 - 왼발 축으로 180도 회전 오른발 앞으로 딛는다, 시선 정면

.. image:: https://user-images.githubusercontent.com/30430227/159823439-546e408b-dc7f-4750-aae6-06aa92f480db.png

3. 공격 - 시계방향으로 회전 

.. image:: https://user-images.githubusercontent.com/30430227/159824514-5738a0ee-d08f-415e-89ca-98c6459b94f1.png
.. image:: https://user-images.githubusercontent.com/30430227/159824525-e5070a0f-2acd-4b11-b5e4-29e4cbc6b530.png

`Timing`

.. image:: https://user-images.githubusercontent.com/30430227/159824869-8be9fd80-1da9-4249-bffd-7db285b7ee62.png

5. Break Down - 머리, 오른팔, 왼팔 순으로 돌아간다(웨이브-Overlapping, 무게중심 뒤쪽

.. image:: https://user-images.githubusercontent.com/30430227/159826254-bcf62550-837e-41f6-9791-d10e8a3117c0.png

7. 손목 Break Down - 봉 회전

.. image:: https://user-images.githubusercontent.com/30430227/159826773-f81e57e0-03cb-45d7-a421-17b7c81e02d8.png
.. image:: https://user-images.githubusercontent.com/30430227/159826984-55f64d21-f9ae-48a0-9676-6e54402947be.png

28. Follow Throuth, 마무리 동작 - 몸이 펴진다(Overlapping, 팔등의 긴장이 풀린다

.. image:: https://user-images.githubusercontent.com/30430227/159828558-bdf47bb6-3883-481a-a4dc-dd2a5a68ec6d.png

19.  Extream 

.. image:: https://user-images.githubusercontent.com/30430227/159828859-d9d10207-42bb-4798-8cb3-3bc43d37927a.png


도끼질 
-------

.. image:: https://user-images.githubusercontent.com/30430227/160030771-f1ded3d5-f76a-442f-9b54-e33d66856b53.png
.. image:: https://user-images.githubusercontent.com/30430227/160030798-c95b8075-41b4-41f6-9cc9-5fa2bd26b4b9.png

`Rig - 기존 Armature에 본 추가 > 도끼를 본에 Parent Bone > 왼 손-FK, 오른 손-IK > ChildOf`

1. Anticipation 

.. image:: https://user-images.githubusercontent.com/30430227/160031338-2ee73944-e302-4afa-976d-3526776d34cd.png

2. 휘두름

.. image:: https://user-images.githubusercontent.com/30430227/160032259-368f0711-f350-42d0-a2bc-c4019aeca861.png

10. Moving Hold > 2번 키프레임을 25, 1 키를 복사 > 충전...

.. image:: https://user-images.githubusercontent.com/30430227/160033352-b5ab759f-24d7-4ec0-b83e-5cd5c1167d75.png

13. Breakdown - Shift-E > 공격 포즈 Extream

.. image:: https://user-images.githubusercontent.com/30430227/160034488-bdbb1dbd-b9de-426d-b441-a7c925503e4d.png

28. Follow Through

.. image:: https://user-images.githubusercontent.com/30430227/160034969-2f566c50-42a9-49b1-aa6a-6a5ed0ad30f9.png


기본숨쉬기 
----------

0. 기본 자세 - 좌우 대칭되지 않게, 양팔은 벌리고 무릎 살짝 굽힘, 양발은 앞뒤로 벌리고

`C-idle은 상체를 구부린다(공격전 자세, 골반은 뒤/측면 흉골은 앞/정면`

.. image:: https://user-images.githubusercontent.com/30430227/160510242-c6a1c762-c610-4f86-ba5c-3580567b7bea.png

40. 기본 자세 키 복사

20. torso 컨트롤을 대각선 위로 이동, 골반 회전, spine.002 반대회전

.. image:: https://user-images.githubusercontent.com/30430227/160510613-97e16a5d-e01c-443a-afee-e2546dd242bb.png

10. 30 chest를 숙였다가 펴면 웨이브, 머리도 같은 방법

.. image:: https://user-images.githubusercontent.com/30430227/160528902-2dce1b76-5a37-481d-8f39-e302a730a5b1.png
.. image:: https://user-images.githubusercontent.com/30430227/160528920-b34869d9-b9c1-4083-a807-b51aa9df16c4.png

20. 어깨와 팔을 굽혔다 편다, 팔을 손바닥 윗방향으로 회전 - 날개짓?

10. 30 전완을 반대방향으로 틀고 굽혔다 편다 - 웨이브

.. image:: https://user-images.githubusercontent.com/30430227/160528956-919d805a-3e8a-4880-9658-94921d08f54b.png
.. image:: https://user-images.githubusercontent.com/30430227/160528988-2079c958-1ad4-4f38-be80-7d0f77c0b71e.png



기존 Pose Library 등록 포즈 순차(사이클 선택  Alt-L > 마우스 휠 or 키보드 Left/Right


.. image:: https://user-images.githubusercontent.com/30430227/160534842-3e4d1891-2f25-4c0d-a7b2-61c5121397a1.png


걷기 
-----


>>>Pose Library
Contact > Down > Pass > Up > Contact (0~24프레임
상체를 살짝 앞으로 구부리고 얼굴은 정면, heel_ik를 사용해 발가락 구부린다
Up포즈에서 앞으로 추진하기위해 Pass포즈에서는 약간 뒤로 즁심이동(Torso
Pass,Up 시 골반은 올라간 발쪽으로 기울어지며 무게중심(torso은 반대로 이동
Paste Pose Flipped
Down,Up은 없는게 자연스러운가..


.. image:: https://user-images.githubusercontent.com/30430227/160539612-9801a095-c102-4fda-ac7a-7cb19e8d51f0.png
.. image:: https://user-images.githubusercontent.com/30430227/160539587-90405510-5a0d-43ac-94e0-eb986bbe9aed.png

`0,24프레임Contact > 12프레임Flip> 6,18프레임Pass ...순으로 Alt-L, Pose Copy는 해당프레임PlayHead`

.. image:: https://user-images.githubusercontent.com/30430227/160538607-284751bd-4f10-4359-9e99-f6113306bf8d.png
.. image:: https://user-images.githubusercontent.com/30430227/160538632-5f6706cd-9002-4236-bcc4-cc8ff4ff2975.png
.. image:: https://user-images.githubusercontent.com/30430227/160538660-7746fa36-3a63-4118-b659-1e253b9a48c3.png
.. image:: https://user-images.githubusercontent.com/30430227/160540144-3707a206-e721-4b3e-8203-69f707c092aa.png

`Tip. Pass전에 뒷 발을 힘차게 차주면 추진력이 생긴다`

.. image:: https://user-images.githubusercontent.com/30430227/160543735-d52a626b-6e40-48b5-8203-3a9841f8303e.png


뛰기 
-----

`Contact > (Down > Kickoff >(Up> Contact`

.. image:: https://user-images.githubusercontent.com/30430227/160557223-8791cd65-c9d5-4cd6-a1b6-c1a7048e73ff.png

`팔은 덩치 크면 밖으로 벌린다, 앞 뒤 홀드하고 휘두르는 동작을 빠르게한다`

.. image:: https://user-images.githubusercontent.com/30430227/160557310-2b18c8e1-c351-4c18-80f5-2f1d11cd037a.png
.. image:: https://user-images.githubusercontent.com/30430227/160557344-a6feb1f6-e2eb-4735-9814-f8f0f4847348.png
.. image:: https://user-images.githubusercontent.com/30430227/160558478-4840d2e3-80f6-4269-94a3-9d1059f22551.png

`허리 구부리기 Nonlinear::Combine > Tab Key 키프레임 편집`

.. image:: https://user-images.githubusercontent.com/30430227/160564752-f8703e51-ecd5-4a66-9a93-d1ec17bbd5ea.png

.. image:: https://user-images.githubusercontent.com/30430227/160564857-6b8edbaf-8959-43e7-9641-b99139bad6b3.png

`팔 앞으로 왔을 때 구부린다`


몬스터 모션
-----------

`rig에 Bone추가 'shield' > 메쉬 & rig 선택 후 Pose모드> shield본 Parent>ChildOf-Set Inverse`

.. image:: https://user-images.githubusercontent.com/30430227/160578069-c69053a7-9f0f-4dd6-975d-f6cd68f068c9.png
.. image:: https://user-images.githubusercontent.com/30430227/160578171-ace0d19d-a6de-4c50-b04a-38b9793565f6.png

1. 숨쉬기 

`0, 24프레임 기본 포즈 전체 키 > AutoKey`

.. image:: https://user-images.githubusercontent.com/30430227/160595704-e20cddbb-30df-41d2-add4-99cead10cffb.png

`12 torso 대각선 위/아래, 올라갈 때 - 머리 숙이고, 가슴 펴고, torst(척추 숙이고`

`6, 18 방패-상완(펴짐회전,팔 구부림/(꼬임회전, 팔 펴짐`

.. image:: https://user-images.githubusercontent.com/30430227/160597410-0ca608ed-7ca7-410b-a76f-5dfb3aae6aff.png
.. image:: https://user-images.githubusercontent.com/30430227/160597429-49774dd2-e9e4-4ac3-8dd0-61c0d036911c.png


2. 공격 

`얼굴은 정면, 몸은 뒤로 뺐다가 앞으로 나간다, 양 팔은 수평, 공격전 breakdown-칼을 뒤로 쭉편다`

.. image:: https://user-images.githubusercontent.com/30430227/160728639-08ccdef0-b220-4c1a-92fa-7ad8c1ca0662.png

.. image:: https://user-images.githubusercontent.com/30430227/160728548-73777954-1654-4904-a485-7e0cf7bef97d.png
.. image:: https://user-images.githubusercontent.com/30430227/160728588-746f4d10-49a1-4e11-86fb-3d788c08ab49.png
.. image:: https://user-images.githubusercontent.com/30430227/160728616-72927b56-0a5d-4b7e-9b45-a2524cf997e2.png

`0.idle > 5.anticipation > 10.hold > 12.attack>14.followthrough(팔 끝까지 회전 >20.hold>24.idle`

`5프레임 breakdown 수정(오른팔 살짝 내리고, 왼팔 펴고>공격 시 웨이브-torst..arm>14.방패(팔 회전`


3. 피격 

`0.idle > 2.damage > 7.hold > 16.idle`

.. image:: https://user-images.githubusercontent.com/30430227/160735100-929daab6-bbdd-443a-be25-29cd52043a11.png
.. image:: https://user-images.githubusercontent.com/30430227/160735133-f0ac72f8-50d8-4416-bc6c-1da8b23e6dde.png

`1.방패로 막을려다가 팡>waist다음에 가슴,머리,팔...돌아올 때도`


캐릭터 모션 
-----------

1. 공격 대기 동작 - 좌우(정면이 아니라 발 벌린 방향 폴짝폴짝..TOP뷰에서

`0.18.36.torso & footIK선택 이동`

.. image:: https://user-images.githubusercontent.com/30430227/160760565-75766db4-785f-44f3-bc03-e3403fe54a94.png
.. image:: https://user-images.githubusercontent.com/30430227/160760531-47a0d3ed-be4c-4497-8212-297802230d7b.png

`2.20.hold > 9.27.폴짝 - torso,spine,chest 펴고 머리 내린다`

.. image:: https://user-images.githubusercontent.com/30430227/160761578-d9fd0c41-9af5-4ea4-9663-34853b98ed25.png

`좌우 발 Overlapping - Shift-E 앞발(hold.2>heel.2>off, 뒷발은 2프레임 Offset 출발`

`좌우 팔은 몸과 Overlapping - 올라가는 중간 프레임에 내려간다`

.. image:: https://user-images.githubusercontent.com/30430227/160764300-ab402f04-0ed9-42f3-a0ca-fd46a353f81d.png


2. 기본 공격 - 과하지 않게, 스킬공격의 체감효과를 높이기 위해

`5.anticipation - torso와 뒷발 선택, 뒤로 뺀다 > 10.hold`

.. image:: https://user-images.githubusercontent.com/30430227/160768651-486774da-5e6b-4f32-9d2a-2db1cf1ad87e.png
.. image:: https://user-images.githubusercontent.com/30430227/160768684-a99cf4c5-a629-4514-bde4-6acd7935cf9c.png

`12. 14.공격-펼친다`

.. image:: https://user-images.githubusercontent.com/30430227/160773060-25fcf427-c85a-434e-bd9d-dc2554d7bc34.png

.. image:: https://user-images.githubusercontent.com/30430227/160772876-0e933271-c1c2-499e-b4b9-37d9178c8c62.png
.. image:: https://user-images.githubusercontent.com/30430227/160773878-21bb32e1-fae6-4d1f-a12c-75e7fa3244bd.png

`22. hold - Extream>오른팔을 돌린다-스타일리쉬한 재미`

.. image:: https://user-images.githubusercontent.com/30430227/160776967-ffa9102a-b9de-4bc6-9346-4487b67f7f37.png



