BASIC

new 3.0
---------

1. Custom shape 변형

.. image:: https://user-images.githubusercontent.com/30430227/148144258-d0ac3416-a262-444d-8a49-a8446ff319f8.png


2. Clear Constraint:  Ctrl-Alt-C


3. Bendy bone / Scale

.. image:: https://user-images.githubusercontent.com/30430227/148144931-9218b029-727d-46c4-98dc-d7ae3b476edd.png
.. image:: https://user-images.githubusercontent.com/30430227/148144956-f72e6e7a-92a8-4654-a724-d554ced3f772.png

.. image:: https://user-images.githubusercontent.com/30430227/148145233-a43ac1f9-beb5-45d8-8494-f2dae4b85c20.png
.. image:: https://user-images.githubusercontent.com/30430227/148145275-29a0a708-8981-4180-8ffd-b298f729c682.png


4. Pose Library - 애드온, 기본으로 설치되어 있음

`생성은 프로퍼티 'Create Pose Asset'버튼 , 사용은 어셋 Browser에서`

.. image:: https://user-images.githubusercontent.com/30430227/148146128-776e923a-a44c-42c6-b6fb-6d10f6c4a157.png
.. image:: https://user-images.githubusercontent.com/30430227/148146147-3aa1c775-10d0-4c39-95f8-0116b80448d8.png

`Thumnail: Camera View > Pose Library - 라이브러리에 생성안될 때는 키프레임 생성`

.. image:: https://user-images.githubusercontent.com/30430227/148146433-23552b3d-1d46-4bb3-b9c2-337fcecd46b1.png
.. image:: https://user-images.githubusercontent.com/30430227/148146418-0e3d5a6d-e69f-4e5f-999e-5a62257f154d.png


5. Stretch to 컨스트레인트에 Swing(그네 옵션 추가?

.. image:: https://user-images.githubusercontent.com/30430227/148146939-c8fcd038-fbf3-40ff-ace2-5d97bf7cab8b.png


6. 옷에 Weight 복사 시 'Bone Heat Weighting' 에러나면..(VRoid 중복 버텍스 문제

`모델 복사 > Merge by Distance > Armature Deform >>`
`원본모델 > With Empty Group > 원본/복사모델 선택 > Transform Weight(NearestFace, SourceLayer:By Name`

.. image:: https://user-images.githubusercontent.com/30430227/148148922-9e4019c3-f648-4a03-9621-4ea8b3ed416e.png


7. 포니테일 - basic.copy_chain(Rigify 

.. image:: https://user-images.githubusercontent.com/30430227/148182797-3fd5dc7e-aa60-446d-84dd-b610a045fccd.png


`Multi Rename - Ctrl-F2`

.. image:: https://user-images.githubusercontent.com/30430227/148182907-b5f24559-962a-46fb-aa2c-e886d43eccda.png


`테일본 > Move New Layer > Rig Layers 에 추가하기 - Text Editor 'rig_ui.py' 파일 수정`

.. image:: https://user-images.githubusercontent.com/30430227/148184783-ad54789f-6247-41f6-b543-1d8dc30ec7b9.png
.. image:: https://user-images.githubusercontent.com/30430227/148185393-e4de20c7-677a-48e0-9dcb-17919871a53d.png

.. image:: https://user-images.githubusercontent.com/30430227/148185364-2a5676cc-7871-4771-8e2b-5dbc1d15e163.png


8. Wiggle Bone - 키프레임 가능, Spring Bone - 키프레임 불가능, 자연스런 모션 - Pose Mode에서 적용해야한다`


9. 근육 - Shape Key 

.. image:: https://user-images.githubusercontent.com/30430227/148206635-3eef3ade-069d-496d-aa1f-0b49a5e2695e.png
.. image:: https://user-images.githubusercontent.com/30430227/148206588-7759b645-778c-4b55-bfa1-b9e9a2d96219.png

`Shape Key > Value 오른클릭 Add Driver`

.. image:: https://user-images.githubusercontent.com/30430227/148206750-21a32ffa-43ad-4239-bfe2-2a8879a2e092.png
.. image:: https://user-images.githubusercontent.com/30430227/148206813-629ee1c7-8f65-4186-a2f1-924b38e27ad8.png


New 3.1
--------

.. image:: https://user-images.githubusercontent.com/30430227/158087579-80579db4-9908-4ed8-ab02-35a29ecb1034.png

`Add Shape(PoseMode`

.. image:: https://user-images.githubusercontent.com/30430227/158087726-89cbe126-0519-4e74-b8a7-321d81820be8.png

`delete Armature`

.. image:: https://user-images.githubusercontent.com/30430227/158087782-88b58046-705e-46ce-9af1-b68033accb23.png

`Inflate`

.. image:: https://user-images.githubusercontent.com/30430227/158088112-f85c5d9d-1b54-457a-9e11-07d1a6356a35.png


Rigging Basic
--------------


1. Custom Property

Rot > Property Value '1.0,' 입력하면 아래쪽에 나타남 > Euler Angles 선택  

.. image:: https://user-images.githubusercontent.com/30430227/130902550-5b991d78-b7ed-4f52-af95-ec893ce60c81.png

Property Value '1.0, 1.0,1.0' XYZ 

'.0,.0,.0,.0 Linear Color RGB로 바꾼 후  

.. image:: https://user-images.githubusercontent.com/30430227/130913389-94abea42-9307-4701-b15f-c34f093a31e5.png

1 정수, 1.0 실수

커스텀 값에서 Copy As Driver  

.. image:: https://user-images.githubusercontent.com/30430227/130905238-b21ad6f9-28ad-4bd5-91a5-7fa335743f30.png

대상에 붙여넣기  

.. image:: https://user-images.githubusercontent.com/30430227/130905298-88b96740-88c0-49f1-9874-e3f15135e81a.png

0/1 Boolean 뷰포트 디스플레이/모디파이 디스플레이 온/오프


Child of
----------

.. image:: https://user-images.githubusercontent.com/30430227/131270242-53817b55-12b4-4276-a208-1268c353d111.png  
.. image:: https://user-images.githubusercontent.com/30430227/131270322-2496e15c-ee47-4e40-9800-9007bce7757c.png

밀대가 닿는 시점에서 키프레임  

.. image:: https://user-images.githubusercontent.com/30430227/131270425-40944619-515f-463f-8fe4-c372464c0f60.png  
.. image:: https://user-images.githubusercontent.com/30430227/131270412-b5e37d0d-4842-4cac-8843-e50032d5efbb.png  

한 프레임 이동 후 키프레임-Clear Inverse>Set Inverse(기존 원점을 지우고 타킷에 원점설정 

.. image:: https://user-images.githubusercontent.com/30430227/131270552-e35f0559-6bfd-427f-915d-ed139f77defe.png  
.. image:: https://user-images.githubusercontent.com/30430227/131270494-7da9aa06-8e39-4ef3-9e11-4a78eb0e4b4e.png  
.. image:: https://user-images.githubusercontent.com/30430227/131270522-1d0c8302-49b3-44c5-9040-9c105c32a5aa.png  

다음 타킷에 전달 -한 프레임 이동 후 새타킷에 위와같은 키프레임(Clear->Set Inverse  
Visual Transform(부모 상대적 위치 벗어남 후 키프레임(Transform, Influence  

.. image:: https://user-images.githubusercontent.com/30430227/131271315-e9dd8ead-3d61-4685-9cef-f7d1e1625aef.png  
.. image:: https://user-images.githubusercontent.com/30430227/131271358-21f0d3fe-351a-454d-812d-9baea1b32be4.png  

다음 타킷도 마찬가지  

.. image:: https://user-images.githubusercontent.com/30430227/131271790-325a724d-a069-4818-98f8-57f4bc3bd93e.png


Transfer Weights
------------------

- 몸과 옷을 따로 웨이트 적용  
몸을 먼저 본에 적용한 후  
옮길 오브젝트(옷같은는 Empty 적용  

.. image:: https://user-images.githubusercontent.com/30430227/131273429-604cf4e5-2316-4f13-b9ec-c9979f571cca.png  

몸 선택 후 옷 선택 후 Weight Paint 모드  

.. image:: https://user-images.githubusercontent.com/30430227/131273759-1ce4dd4e-1a92-4223-b638-13f7216fadfb.png  
.. image:: https://user-images.githubusercontent.com/30430227/131273848-9755f8ae-5fe2-4ada-b6d9-693b19e7afe6.png  


카메라 드라이브 
---------------

1. Copy as New Driver  

.. image:: https://user-images.githubusercontent.com/30430227/137431840-fcefb907-7949-495e-95fa-e3bba085ef5f.png  
.. image:: https://user-images.githubusercontent.com/30430227/137431983-f6ce03da-d296-4e38-9f72-6c6a04a2e33d.png  



2. Paste Driver  

.. image:: https://user-images.githubusercontent.com/30430227/137432066-41102168-5e40-46e6-8bdd-b77ea49b8fcb.png  
.. image:: https://user-images.githubusercontent.com/30430227/137432103-09b0f0c7-f1b4-416b-97bf-a3d2052046c0.png  


3. Edit Driver  

.. image:: https://user-images.githubusercontent.com/30430227/137432233-b78a4edd-967f-49dd-9255-fb904083033a.png  
.. image:: https://user-images.githubusercontent.com/30430227/137433397-5c048be0-f398-4dc4-a8d3-d948ed2a33e6.png
.. image:: https://user-images.githubusercontent.com/30430227/137433465-cab7d1cc-c717-49af-aa30-95d422ae2955.png  

`카메라 다가가면 X-방향으로 비킨다`  

.. image:: https://user-images.githubusercontent.com/30430227/137433537-f46e6271-0411-4864-8cdb-0115e92c2c6b.png  


Image Size -가로세로비 
--------------------------

`Boolean Intersect > 상하좌우 vertex Hook > 오른쪽 위 Hook선택 > X- Copy Driver -오른쪽 아래 붙여넣기 > Y-Copy Driver - 왼쪽 위 붙여넣기`

.. image:: https://user-images.githubusercontent.com/30430227/143068897-6489699e-d8fa-4af9-9e59-79ba8a509dea.png


Bow Rig
----------

`한쪽 활 가지부분 뼈 미러 복사`

.. image:: https://user-images.githubusercontent.com/30430227/159624761-bad5f78a-f3d1-4211-af5f-95c606951d7d.png

.. image:: https://user-images.githubusercontent.com/30430227/159625134-cf470e50-1fdb-42e7-8226-0b7af6add73b.png

`IK`

.. image:: https://user-images.githubusercontent.com/30430227/159624858-e61fc254-63b2-4f98-8b08-425b134e66bd.png
.. image:: https://user-images.githubusercontent.com/30430227/159624939-d990988b-d7a8-488e-8fc9-647618515d4d.png

`Limit Distance`

.. image:: https://user-images.githubusercontent.com/30430227/159624893-0117eef4-7909-473d-a30c-10d2e6697643.png
.. image:: https://user-images.githubusercontent.com/30430227/159624925-f51c157c-2af6-4927-8adb-faf035d12a80.png

`양쪽 활 가지 본, stringIK.L, stringIK.R, string 본 Parent -> Root`

.. image:: https://user-images.githubusercontent.com/30430227/159625059-febcc3dc-82eb-45d8-9b4b-77f6b30f6f6f.png



Piston - Damped Track
------------------------

.. image:: https://user-images.githubusercontent.com/30430227/161666524-5dd3a897-6913-4b4c-a29c-04c34577b9cf.png
.. image:: https://user-images.githubusercontent.com/30430227/161666506-540fea02-2106-4f21-992d-c60090508e07.png

.. image:: https://user-images.githubusercontent.com/30430227/161665672-ffffca52-1f1c-4cdc-9a11-9af95a28f99d.png
.. image:: https://user-images.githubusercontent.com/30430227/161666336-eb590fc6-9d32-4bfb-b96b-48a3be85240e.png

`Damped Track`

.. image:: https://user-images.githubusercontent.com/30430227/161666477-fee081cb-7bd1-409d-aaa1-119e59c538ba.png
.. image:: https://user-images.githubusercontent.com/30430227/161666463-11ea7676-29e5-4f03-bc24-5dd8857003d7.png

VCharcater
----------

1. Mixamo

import T-posed mesh model without any animation

.. image:: https://user-images.githubusercontent.com/30430227/139252670-367af16f-1ac6-49d6-b7c4-1ae25950b27e.png

.. image:: https://user-images.githubusercontent.com/30430227/139252754-2b5cf96e-898d-40c3-862b-cd005efe1521.png


VRoid
------

`확장자 .vrm ->glb > import GLTF`

.. image:: https://user-images.githubusercontent.com/30430227/159197392-7f596d29-0ba0-4d35-86eb-7c377710977d.png

`bone heat weighting 에러 시 > Remove Double Vertex`


리깅 캐릭터
-------------


1. 웨이트 리셋

.. image:: https://user-images.githubusercontent.com/30430227/124885153-f08e8200-e00d-11eb-861b-42ac6af28546.png  
.. image:: https://user-images.githubusercontent.com/30430227/124885360-26336b00-e00e-11eb-9c13-b136bd293870.png  

선택 영역(메쉬, 본의 웨이트를 Vertex Groups에서 Remove한다

2. 벨트 웨이트

.. image:: https://user-images.githubusercontent.com/30430227/124885796-98a44b00-e00e-11eb-9efa-5625f4073dd2.png  

힙 본과 척추 본

.. image:: https://user-images.githubusercontent.com/30430227/124885699-7e6a6d00-e00e-11eb-9e67-e3bfaf9bd540.png 

힙 본은 전체에 웨이트 100% Asign

.. image:: https://user-images.githubusercontent.com/30430227/124885947-c2f60880-e00e-11eb-9249-e0a17b1032e7.png  

척추 본은 일단 100% 준 후 아랫부분만 25% 다시 준다


3. 허벅지 웨이트

.. image:: https://user-images.githubusercontent.com/30430227/124886762-870f7300-e00f-11eb-8203-4da4117224a5.png 

오른쪽 허벅지 본에 적용(왼쪽도 마찬가지

.. image:: https://user-images.githubusercontent.com/30430227/124886997-baea9880-e00f-11eb-8b16-6043e850e03e.png 

이 부분은 힙 본에도 적용


4. 머리 웨이트

.. image:: https://user-images.githubusercontent.com/30430227/124887289-fd13da00-e00f-11eb-8aa5-e4fe068fd089.png  
.. image:: https://user-images.githubusercontent.com/30430227/124887339-0ac95f80-e010-11eb-99b2-111281bfc1a3.png 

목 본에는 Remove, 머리 본에는 100%


5. 머리, 팔 본

Inherit Rotation


손가락

.. image:: https://user-images.githubusercontent.com/30430227/124888545-27b26280-e011-11eb-8aa3-1eb252785c13.png  
.. image:: https://user-images.githubusercontent.com/30430227/124888878-77912980-e011-11eb-9981-6b041e1d6dbe.png  

Copy Rotation Constraint  

 
.. image:: https://user-images.githubusercontent.com/30430227/124889183-bfb04c00-e011-11eb-8d83-e9c6068af17a.png  

중지 본도 Constraint 적용(Influence: 20정도  

.. image:: https://user-images.githubusercontent.com/30430227/124889802-64cb2480-e012-11eb-9482-01e05f7a7732.png  
X축 정렬(Roll: Ctrl + r  


.. image:: https://user-images.githubusercontent.com/30430227/124890378-f3d83c80-e012-11eb-8f00-50dd5114e8d0.png  
.. image:: https://user-images.githubusercontent.com/30430227/124890556-1d916380-e013-11eb-8710-f87e452efe48.png 

Constraint, x축만 적용   


.. image:: https://user-images.githubusercontent.com/30430227/124891945-60a00680-e014-11eb-8c75-2fa518ef755a.png  
.. image:: https://user-images.githubusercontent.com/30430227/124891983-6b5a9b80-e014-11eb-9587-012dbde170e6.png  

두 번째 마디는 Limit Rotation Constraint도 적용(세 번째 마디를 회전한 상태에서 한계값을 정한다  


.. image:: https://user-images.githubusercontent.com/30430227/124892652-005d9480-e015-11eb-81a8-0bbad25c1b94.png  
.. image:: https://user-images.githubusercontent.com/30430227/124892697-0b182980-e015-11eb-809e-933acb0fb1b4.png  


오른 손 본만 제거하기 위해서 X-Axis Mirror 체크 해지 다음 제거

.. image:: https://user-images.githubusercontent.com/30430227/124893164-7661fb80-e015-11eb-8e87-9d87a6c6757b.png 

왼 손 본 오른 손 본에 복사  

.. image:: https://user-images.githubusercontent.com/30430227/124895109-369c1380-e017-11eb-91bf-107e679b5b12.png

발 본 복사(Clear Parent, name: foot.IK.L, IK 적용  

.. image:: https://user-images.githubusercontent.com/30430227/124895717-c17d0e00-e017-11eb-810e-acaf9218b5d6.png 

발 본에 Copy Rotation Constraint 적용

.. image:: https://user-images.githubusercontent.com/30430227/124897121-f50c6800-e018-11eb-9642-c277a22d457c.png 

회전용 본 생성  

.. image:: https://user-images.githubusercontent.com/30430227/124897279-1ec58f00-e019-11eb-92fb-c6e9bcd256d9.png 

foot.IK.L 본이 roll.F.L을 아버지라 부르게 됨  

.. image:: https://user-images.githubusercontent.com/30430227/124897645-7663fa80-e019-11eb-86bb-811cc8ad28a8.png

roll.B.L이 할아버지가 됨  

.. image:: https://user-images.githubusercontent.com/30430227/124899128-c7c0b980-e01a-11eb-9449-931f9a3d8308.png 

foot.IK.main.L 이 증조부  

.. image:: https://user-images.githubusercontent.com/30430227/125006847-03e72f00-e09a-11eb-8809-dd384320d886.png  
.. image:: https://user-images.githubusercontent.com/30430227/125006687-ac48c380-e099-11eb-8a88-1f04cee95999.png 

Constraint Local  

  
.. image:: https://user-images.githubusercontent.com/30430227/125006865-0c3f6a00-e09a-11eb-9d6e-5ff6ce6d7421.png  
.. image:: https://user-images.githubusercontent.com/30430227/124918260-ce0d6080-e02f-11eb-813a-3c9ec2e2ae10.png 

Invert

 
.. image:: https://user-images.githubusercontent.com/30430227/125006873-11041e00-e09a-11eb-8aee-749d0be0e7ec.png

.. image:: https://user-images.githubusercontent.com/30430227/124919468-46285600-e031-11eb-9b59-e656fa2e5f2d.png

Invert

 PoleTarget

.. image:: https://user-images.githubusercontent.com/30430227/125007092-7a842c80-e09a-11eb-844c-6d4b43656eca.png
.. image:: https://user-images.githubusercontent.com/30430227/125007118-8839b200-e09a-11eb-827a-34ce28e9e4af.png


6. Copy, SwitchDir, Parent

.. image:: https://user-images.githubusercontent.com/30430227/125007436-26c61300-e09b-11eb-832f-65b6a1cc8edc.png

.. image:: https://user-images.githubusercontent.com/30430227/125007501-48bf9580-e09b-11eb-9eed-d23b9e5e905d.png



LowPloyCharacter
-------------------

1. 바디 1: 2: 4  

.. image:: https://user-images.githubusercontent.com/30430227/133034866-55349946-b5c4-4092-972b-a7441946b2ac.png
.. image:: https://user-images.githubusercontent.com/30430227/133034888-fa104fd2-5792-4266-9b34-a1c6c2122027.png  

2. Side  

.. image:: https://user-images.githubusercontent.com/30430227/133035062-dcdd5079-14de-452d-92ca-c5c92c82f8ca.png
.. image:: https://user-images.githubusercontent.com/30430227/133035185-0d80530b-deb4-4e33-9379-6bee633ea553.png  

`남자`  

.. image:: https://user-images.githubusercontent.com/30430227/133036172-16891134-6000-4946-93ac-3cf2627e8088.png


3. Front  

.. image:: https://user-images.githubusercontent.com/30430227/133035325-ec108764-a385-4b36-8f24-893e60524664.png  

`남자`  

.. image:: https://user-images.githubusercontent.com/30430227/133036207-55d8ae7a-6b2a-45f9-93f6-2cb3188a47d5.png  

4. Loop Cut  

.. image:: https://user-images.githubusercontent.com/30430227/133035682-e83c9122-1b88-44b6-997e-bbcf4aa218a4.png
.. image:: https://user-images.githubusercontent.com/30430227/133035780-b13141f6-e8aa-4211-9aaa-257c351d84c3.png  

5. 남자  

.. image:: https://user-images.githubusercontent.com/30430227/133036436-50b85a30-a46e-4f02-be25-ca8ac5680868.png
.. image:: https://user-images.githubusercontent.com/30430227/133036595-d5f06afe-ba36-4679-82f0-64b3f837319e.png  
.. image:: https://user-images.githubusercontent.com/30430227/133036826-095028ab-aac2-4dd0-8328-e6cee4cf010c.png
.. image:: https://user-images.githubusercontent.com/30430227/133036864-15680a69-0bef-4b7d-916c-c61e9f4ffd62.png  
.. image:: https://user-images.githubusercontent.com/30430227/133036923-3f1ef634-b156-4469-846e-aa1703570a56.png  
.. image:: https://user-images.githubusercontent.com/30430227/133037037-d4bc0c5f-2b6b-4ed7-a773-e486063add2e.png  


6. 등짝  

.. image:: https://user-images.githubusercontent.com/30430227/133037662-71136fef-cf57-41c7-9ab1-2e222f3a45dc.png
.. image:: https://user-images.githubusercontent.com/30430227/133037800-8e2be747-700f-4c85-ba4e-55b0edf08c34.png  
.. image:: https://user-images.githubusercontent.com/30430227/133037870-c8adadfd-17ec-443c-a799-2ae8c581f328.png  

7. 마무리  

.. image:: https://user-images.githubusercontent.com/30430227/133038212-a685e891-1e7a-4674-b808-a758dfa9cbba.png

`참고 이미지`  

.. image:: https://user-images.githubusercontent.com/30430227/133038381-dc147e4a-9a91-44d7-bb0d-7e6081cd286f.png
.. image:: https://user-images.githubusercontent.com/30430227/133038408-0ec667cd-2637-45e2-9f80-11c43df6dfec.png  
.. image:: https://user-images.githubusercontent.com/30430227/133175629-231ec670-d0e5-4c5e-bdba-91c2dbb050e3.png
.. image:: https://user-images.githubusercontent.com/30430227/133175676-39c39fcc-a378-4d97-a7ad-cf2ad7da4272.png  
.. image:: https://user-images.githubusercontent.com/30430227/133175700-862c8f87-b708-459a-aacf-eb65f755993f.png  


참조  
------------

.. image:: https://user-images.githubusercontent.com/30430227/133176460-4f022741-ede7-4385-b518-367e75d09099.png
.. image:: https://user-images.githubusercontent.com/30430227/133176515-46d67c7a-509f-41ce-b93d-b656e3137243.png  
.. image:: https://user-images.githubusercontent.com/30430227/133176541-41f15622-28f4-4b3b-8c63-cea89026abcc.png  
.. image:: https://user-images.githubusercontent.com/30430227/133176559-7a2f7b65-c739-47f2-b7e9-b3566adcb4f5.png  
.. image:: https://user-images.githubusercontent.com/30430227/133176581-1a31f650-2c95-4c03-82e0-8b382520b516.png  
.. image:: https://user-images.githubusercontent.com/30430227/133176665-db18386a-9fb9-41a0-9f04-ba6f8039e273.png  

.. image:: https://user-images.githubusercontent.com/30430227/133176619-4786c01a-0c2f-41ca-95ee-716ac948a6f9.png  



