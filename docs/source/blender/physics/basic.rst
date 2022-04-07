
BASIC
======


Fluid 
-------

``파티클이 메쉬를 둟고 지나갈 때 Thickness, TimeStep Max 10/ Min 4``  

.. image:: https://user-images.githubusercontent.com/30430227/137741517-40925858-e819-4659-9df0-4b9187b1b4f6.png  
.. image:: https://user-images.githubusercontent.com/30430227/137741602-7f206c00-055d-405f-b950-959f25a100bf.png  




1. Liquid  

``모델 배치``  

.. image:: https://user-images.githubusercontent.com/30430227/137734933-d48981da-6e26-4320-a053-28b326d94218.png  

``Effector -3 박스``  

.. image:: https://user-images.githubusercontent.com/30430227/137735112-0deecec9-e71b-4a92-9adc-0b08ff6ee326.png
.. image:: https://user-images.githubusercontent.com/30430227/137735168-5f6d7f5a-2b1e-49b6-917a-3db870bcb340.png  


``Flow -inflow``  

.. image:: https://user-images.githubusercontent.com/30430227/137735275-c0ed4f73-36d8-4ac8-8919-938850a3a85a.png
.. image:: https://user-images.githubusercontent.com/30430227/137735347-02265dcb-4458-408f-ad9a-20e05038d3f0.png  

``Flow - Use Flow - Keyframe``  

.. image:: https://user-images.githubusercontent.com/30430227/137735966-98ec0071-0866-4b72-a4f3-fb4b8573e411.png

.. image:: https://user-images.githubusercontent.com/30430227/137735910-ee706edb-2315-4caf-b814-bd4fe15e559c.png


``Domain -liquid``  

.. image:: https://user-images.githubusercontent.com/30430227/137737484-d9499643-5071-430a-93a6-ee35d2e44471.png  

.. image:: https://user-images.githubusercontent.com/30430227/137737401-150baf3e-6b20-4e82-9115-4ef9a1244b1b.png  


``폼 파티클 생성 - Is esumable 체크`` 

.. image:: https://user-images.githubusercontent.com/30430227/137740927-c2125b9d-5391-4e91-872c-4e815db37d4a.png  

.. image:: https://user-images.githubusercontent.com/30430227/137741038-e48a91c6-43ed-4b6b-9f1e-d5d747703a68.png  
.. image:: https://user-images.githubusercontent.com/30430227/137741093-7c579f61-04ed-42b2-bb4d-c7a36e946504.png  


Particle
---------

1. life Time 파이클 사이즈

.. image:: https://user-images.githubusercontent.com/30430227/144852453-d9fabb10-00ca-4c71-95c1-bc4ff53229a5.png

``Texture > Blend > Influence(Size > Mapping(Strand/Particle > Color(ColorRamp ``

.. image:: https://user-images.githubusercontent.com/30430227/144852536-190c655c-20d7-4e19-8ca9-7d6b8112957d.png

.. image:: https://user-images.githubusercontent.com/30430227/144852825-cbdbb252-ae84-4867-8352-1959e7cd86a7.png


라인 튜브 
----------

1. ico Sphere  

.. image:: https://user-images.githubusercontent.com/30430227/132629225-de709860-db0d-4961-8f27-44045596c465.png  


2. Particle  

``Render:path, Cache:Bake, gravity:0``  

.. image:: https://user-images.githubusercontent.com/30430227/132629753-76bc9133-a54c-4bd2-b886-3632a9899145.png  

``Convert to Mesh``  

.. image:: https://user-images.githubusercontent.com/30430227/132629834-936727d3-45fc-4949-9f3e-511795749372.png

``to Curve``  

.. image:: https://user-images.githubusercontent.com/30430227/132629979-03d8a1f0-2ec7-4485-bf2e-13b8f958846e.png  

3. 커브세팅  

.. image:: https://user-images.githubusercontent.com/30430227/132630309-147b366a-5094-4644-bf8f-fffef7a68aec.png  
.. image:: https://user-images.githubusercontent.com/30430227/132630357-e47041c5-e98d-4810-b92c-7f8dc175757f.png  

4. 응용  

.. image:: https://user-images.githubusercontent.com/30430227/132631804-e1bcbb54-5881-466e-8d78-72931698dcc5.png  

``Empty > Force Field > Vortex`` 

.. image:: https://user-images.githubusercontent.com/30430227/132631146-a967f0ef-4289-4948-b717-1cbc52dc1b72.png
.. image:: https://user-images.githubusercontent.com/30430227/132631160-cd871d43-b655-4c24-9f95-6631721ece9b.png  


5. Cache Bake > Strand Steps  

.. image:: https://user-images.githubusercontent.com/30430227/132631430-c9d826d5-7a5b-4b44-bba1-fd14da44cd69.png  
.. image:: https://user-images.githubusercontent.com/30430227/132631496-802d766a-b0af-47be-b6f0-d6d226a7ee1b.png
.. image:: https://user-images.githubusercontent.com/30430227/132631708-cc1c273f-ccb2-479f-bb82-d1cb8027bf81.png  



적혈구
--------

1. 모델링  

.. image:: https://user-images.githubusercontent.com/30430227/132632421-304e95d7-4ca6-4ea6-acdf-9147a8148443.png
.. image:: https://user-images.githubusercontent.com/30430227/132632602-a8949259-f3b8-48ac-9faf-0cb086d837f8.png  

2. 재질  

.. image:: https://user-images.githubusercontent.com/30430227/132635387-88e49333-1ad3-450d-9cf2-6e389e89b892.png  
.. image:: https://user-images.githubusercontent.com/30430227/132635366-04adee31-24fe-489e-973d-364b594d8357.png  


3. ico sphere > particle  

.. image:: https://user-images.githubusercontent.com/30430227/132635654-482dcdb5-bec7-4b40-82f2-62ef4fcc7730.png  
.. image:: https://user-images.githubusercontent.com/30430227/132635691-0e9cf537-cb13-402a-9963-71c412c4854a.png 

``Particle Normal:0, Rotation:Randomize:1``  

.. image:: https://user-images.githubusercontent.com/30430227/132637233-e4173620-62b7-4795-8d27-f162b04f6c1d.png  

``gravity : off``  

.. image:: https://user-images.githubusercontent.com/30430227/132637285-8d5c1a56-40a1-4d6a-a046-28742ada57d3.png 

``Add Empty > Add Force Field(Turblence``  


4. Make Instances Real > Physics  

.. image:: https://user-images.githubusercontent.com/30430227/132638156-b878e0d3-fd91-4ff6-bc0e-a0f54f80048f.png

5. DOF  

``Empty``  

.. image:: https://user-images.githubusercontent.com/30430227/132640532-97483d54-7010-4f4b-af62-f3598053d881.png  

``Camera``  

.. image:: https://user-images.githubusercontent.com/30430227/132640575-78a1521f-acec-49e6-bbdf-1ae940bf7e6d.png  

6. 배경 노이즈  

.. image:: https://user-images.githubusercontent.com/30430227/132641110-c6ec4407-c990-4f26-ac12-872b039c1270.png  
.. image:: https://user-images.githubusercontent.com/30430227/132641151-0c92428b-0d8d-4c95-b83e-8f1b020f8cf2.png  



모래 디졸브  
------------

1. Boolean  

.. image:: https://user-images.githubusercontent.com/30430227/132645309-f340857c-02fc-478b-b36e-fb4d611eaa95.png  
.. image:: https://user-images.githubusercontent.com/30430227/132645445-454dc3ae-7ae7-477e-86f4-6549242c6aeb.png  
.. image:: https://user-images.githubusercontent.com/30430227/132645529-dfb77fd4-0e9f-46c6-b4f2-76af0bcb9f76.png  

2. Keyframe  

``position & Rotation``  

.. image:: https://user-images.githubusercontent.com/30430227/132646009-22fa7f26-fafe-4cb9-8926-922d91938ec6.png 

``Box 회전하며 내려오는 애니``  

.. image:: https://user-images.githubusercontent.com/30430227/132646276-85ab740b-373f-481f-b4bd-509937467314.png  

3. 파티클 용 Slice  

``수지와 Box 복사``  

.. image:: https://user-images.githubusercontent.com/30430227/132647827-daa7def6-8273-4857-a0bb-a285e03af50b.png  
.. image:: https://user-images.githubusercontent.com/30430227/132647974-c3deabef-e354-4b4c-90c7-3799dabcd83c.png  


4. 파티클  

.. image:: https://user-images.githubusercontent.com/30430227/132648588-d34d9d8b-05fe-4ae2-9620-3bbcff910630.png

``Volume, Random, 파티클 똥 제거 Use Modifier Stack``  

.. image:: https://user-images.githubusercontent.com/30430227/132650561-c2b6c248-6ffe-4584-8d24-f8c521a6f33f.png
.. image:: https://user-images.githubusercontent.com/30430227/132648743-dd4c6eeb-7931-4867-a887-2f0c3d4da5d8.png  


5. Gravity(9.8 -> 1  

``공중에 잠시 멈추다 떨어지는 것 같다``  

.. image:: https://user-images.githubusercontent.com/30430227/132650119-e84ef694-643e-4eae-8366-682753948139.png  


6. 포스가 함께  

.. image:: https://user-images.githubusercontent.com/30430227/132651255-ca343eb4-b033-4f0c-a318-67ffd0148840.png  


7. 파티클 메쉬  

.. image:: https://user-images.githubusercontent.com/30430227/132651543-e66d22af-7080-4a4d-9ccb-666c6ba0e7f5.png  
.. image:: https://user-images.githubusercontent.com/30430227/132651740-3e0a4458-ecf4-4535-b1d0-908dc7cea993.png  


Curve Force Field
-------------

``Meal Radius 에 영향받는다(Ctrl -Alt -S``

1. 커브를 선택 > Force 적용 - Shape Curve 가 활성

.. image:: https://user-images.githubusercontent.com/30430227/142744922-468ed196-96a8-48b2-961c-3eda38eed52d.png
.. image:: https://user-images.githubusercontent.com/30430227/142745078-e533e998-b67a-4243-88d8-0af97a343e58.png

2. Curve Guide 타입 

.. image:: https://user-images.githubusercontent.com/30430227/142744974-1c4e5c20-87f1-4645-8485-972a3da95ea6.png

``Particle Life Time 동안 커프 끝에 도달한다 - 즉 lift time이 속도``

3. Collection Instance

.. image:: https://user-images.githubusercontent.com/30430227/142745302-4674fe24-dea4-4ecd-b423-b7f59685b19c.png

.. image:: https://user-images.githubusercontent.com/30430227/142745283-8d665168-4542-4b82-9ba9-611d2e564479.png
.. image:: https://user-images.githubusercontent.com/30430227/142745305-f560f21e-c266-4a9d-8d54-51c56c0f6242.png



젤리
--------

.. image:: https://user-images.githubusercontent.com/30430227/126725922-846a202c-c5f0-4154-b6c3-dcc4e6ba610e.png  
.. image:: https://user-images.githubusercontent.com/30430227/126725079-8f96a5db-3574-46f6-930b-2c4855fd4c99.png

`` softbody > goal 체크해제, Bending: 2, pull/push: 0.75``

.. image:: https://user-images.githubusercontent.com/30430227/126725055-a99273ea-eb23-4084-aa3f-4c68eb0e3886.png

``Transmission: 1, 유리같은재질``

.. image:: https://user-images.githubusercontent.com/30430227/126725199-3e8cb556-82cb-40bf-8569-2aeb245def9c.png

`` vertex parent, 자식선택 > 부모선택 > EditMode``


베게 
------

1. 박스  

.. image:: https://user-images.githubusercontent.com/30430227/133077761-3b357d8a-f3c5-4587-90ce-e6e35b5f5d77.png
.. image:: https://user-images.githubusercontent.com/30430227/133077721-b658f21c-4751-4226-a979-8ace8bce9646.png  
.. image:: https://user-images.githubusercontent.com/30430227/133078239-d4e167e6-1ca4-4f1e-ab71-3914fdcd461f.png  


2.  큐션  

``바닥 Softbody $ Cloth Friction: 50, 공으로 눌러 모양 만듬``  

.. image:: https://user-images.githubusercontent.com/30430227/133079189-290fd4a4-abb8-4cbc-b28c-fc512f10cb43.png  


3. pin  

``Gravity: 0, Pressure: 10``  

.. image:: https://user-images.githubusercontent.com/30430227/133079496-c2c46db7-4ae0-4b28-bf42-aab2386585d4.png
.. image:: https://user-images.githubusercontent.com/30430227/133080230-49eda33e-7f43-439b-a9ed-8bb6d5603dc2.png  



연기
-----

.. code-block::

 Flow::
 Initial Temperature: 스모크 속도
 Surface Emission: 표면 방출량(적을 수록 보기좋다?
 Texture Offset: animate 


1. Follow Path  

.. image:: https://user-images.githubusercontent.com/30430227/133711346-c69937a6-e4d7-4ed3-8af3-ff90ddb25fc6.png
.. image:: https://user-images.githubusercontent.com/30430227/133711372-332d7ce6-c18e-4b3f-ac15-c92a71778dd2.png  

2. Quick Effect  

.. image:: https://user-images.githubusercontent.com/30430227/133711539-e218d9f4-d1f2-4a36-9d05-0781f929b7c7.png
.. image:: https://user-images.githubusercontent.com/30430227/133711585-abca29a3-dd90-4290-be2a-d090b341803c.png  

``Domain Dissolve``  

.. image:: https://user-images.githubusercontent.com/30430227/133713067-31208996-3eb5-4d0b-ba76-23a0dc5902b9.png
.. image:: https://user-images.githubusercontent.com/30430227/133713082-1ea4dc2e-14c7-4a7c-ac1b-5b82015cdda2.png  

``Bake 버튼?``  

.. image:: https://user-images.githubusercontent.com/30430227/133725459-cefdd5b2-88ad-4763-9ec6-ca1854090b5c.png  

``Domain Material``  

.. image:: https://user-images.githubusercontent.com/30430227/133731538-92ffd8ba-0acb-4f5b-9c74-b5eb8597f278.png
.. image:: https://user-images.githubusercontent.com/30430227/133731516-d462c374-3f86-4913-89d6-aa0539d1d5e6.png  

``Render::Bloom, Volumetrics``  

.. image:: https://user-images.githubusercontent.com/30430227/133731905-c30e06cd-dc2d-400f-8832-998e2b33ed1f.png
.. image:: https://user-images.githubusercontent.com/30430227/133731854-b9c6cdca-f206-4e0a-b70e-dbd2c20505a3.png

 
 
 Puffy Cloth 
---------------

1. Cylinder > Top 평면 복사 후 Separate > Inset , 마지막은 Merge Vertex  

.. image:: https://user-images.githubusercontent.com/30430227/137719174-4bd665ff-fca9-4d6d-b060-7422986d63dd.png  


``Vertex Groups``  

.. image:: https://user-images.githubusercontent.com/30430227/137719356-190ab987-485c-4eef-b1b7-702c215a6d34.png


2. Displace - 위로 살짝 올려줌``  

.. image:: https://user-images.githubusercontent.com/30430227/137719675-2d26b5ad-6398-47a0-ab50-dec760e0505c.png  


3. Cloth  

``Cloth > Pressure: 3 Gravity: 0, Shrinking Factor: -0.2``  

.. image:: https://user-images.githubusercontent.com/30430227/137719759-b031d6a9-fce8-4ee9-969b-dcf144a3349d.png  
.. image:: https://user-images.githubusercontent.com/30430227/137720405-c7b44e74-5631-400d-a40a-8b07d224df71.png  

``Subdivide - 순서 Cloth 위로 올린다``  

.. image:: https://user-images.githubusercontent.com/30430227/137720620-4799fe05-acc1-46f6-bfd7-d6d12ae6e686.png  

.. image:: https://user-images.githubusercontent.com/30430227/137722395-0ba7c021-e3b9-4cbb-b5f5-da8e714518e4.png
.. image:: https://user-images.githubusercontent.com/30430227/137722326-a149de69-b550-4bcc-9be2-d0db8fbeccf5.png  


``Subdivide를 추가하면 Detail 추가됨``  


Cell Fracture
------------------

1. 기본

``실행``

.. image:: https://user-images.githubusercontent.com/30430227/141606394-8d38f041-68e9-4954-bd85-cd42a1c67794.png

``own vertex - 자신의 점 8개를 기준으로 분리``

.. image:: https://user-images.githubusercontent.com/30430227/141606460-de8d2916-3fea-498a-bbfb-aef03a73da35.png
.. image:: https://user-images.githubusercontent.com/30430227/141606454-75abc78c-5c24-4604-9c74-b8e149775d82.png

``Child vertex - 자식인 구의 점을 기준으로 갈라짐``

.. image:: https://user-images.githubusercontent.com/30430227/141606538-b3fead4e-0fff-4f44-93cc-99cc7cd21787.png
.. image:: https://user-images.githubusercontent.com/30430227/141606556-b68e8b29-6fe0-4318-b9a3-7c569eaee4dd.png

``Own Particles - 파티클 기준, Source Limit 이하로만 분리// Child Paricles - 자식의 파티클을 기준으로 갈라짐``

.. image:: https://user-images.githubusercontent.com/30430227/141606639-bd648dcc-458d-4756-9b73-5618dab32229.png

.. image:: https://user-images.githubusercontent.com/30430227/141606648-42db120f-6b73-4f28-85ce-cc325c6c1bcf.png
.. image:: https://user-images.githubusercontent.com/30430227/141606658-16ae7365-944b-42f9-8638-6d779e3a6623.png

.. image:: https://user-images.githubusercontent.com/30430227/141606671-bdbd107e-17cf-4623-9d15-700fe93b56a9.png

``Annotation Pencil - Surface``

.. image:: https://user-images.githubusercontent.com/30430227/141606719-e078cc8d-0dfa-43b5-94ca-d2a679541b96.png

.. image:: https://user-images.githubusercontent.com/30430227/141606797-6a279ac1-2c4c-4a75-b5ab-3397c356f1eb.png
.. image:: https://user-images.githubusercontent.com/30430227/141606805-79ea7be1-301f-4b2d-b780-f11a0151c9d5.png

``Multiple - 동시에 적용``

.. image:: https://user-images.githubusercontent.com/30430227/141606839-f5f48e14-3d09-4e72-b54f-dd0486ac5fcb.png

.. image:: https://user-images.githubusercontent.com/30430227/141606948-f9d8de13-4d21-4b7d-a9f6-0f426bda73ed.png
.. image:: https://user-images.githubusercontent.com/30430227/141606961-7ff57fb9-1258-4fd9-98f1-670f93141d38.png

``Noise:: Own, Noise 1 - X, Y, Z 값 영향``

.. image:: https://user-images.githubusercontent.com/30430227/141607006-9ef977c5-b5fe-4afb-87fa-2f5506b20d4c.png

``recursion -재귀적, 부분 분할//Source limit 0 : 갈라진데 또 갈라짐//Clamp Recursion: 분할 갯수``

.. image:: https://user-images.githubusercontent.com/30430227/141607220-5ec8334b-40b9-4c8d-aa03-7c88640008b3.png

.. image:: https://user-images.githubusercontent.com/30430227/141607200-8fec4199-5b17-4b7b-ba4e-142559ad67ac.png

``Material, Recenter, Collection``

.. image:: https://user-images.githubusercontent.com/30430227/141607483-7e9adcc2-11b5-49ab-a1fb-9bc8ba5eceb8.png

.. image:: https://user-images.githubusercontent.com/30430227/141607513-1273ea14-62b4-46f4-a333-4bc1c01c47a6.png
.. image:: https://user-images.githubusercontent.com/30430227/141607521-000c040b-0fba-4470-b7d9-be9e4b891068.png
.. image:: https://user-images.githubusercontent.com/30430227/141607527-0c4f6839-3578-44d4-b915-f030401ad2f5.png

``Rigidbody > Add Active``

.. image:: https://user-images.githubusercontent.com/30430227/141607685-bff558dd-92ed-4645-a698-4881ac0dc2f7.png

.. image:: https://user-images.githubusercontent.com/30430227/141607727-ef71a4d1-15f1-4904-9562-db20e5e488a0.png

**잠깐! 떨어지는 순간 박스와 조각 컬렉션을 바꿔치기 랜더링 시 Collection 은 랜더링 On/Off 키가 안먹힌다**

``Collection > R-mouse > Instance to Scene - 인스턴스 컬렉션은 키프레임이 된다``

.. image:: https://user-images.githubusercontent.com/30430227/141615506-eb1790df-d94b-4e70-ad5b-4ee64dff7274.png


밀어내기 - Rigid Body 수동 조작
------------------------------

``Animate 체크 > 포지션 키프레임``

.. image:: https://user-images.githubusercontent.com/30430227/141653781-2c3def84-8b8b-4f97-a762-8d0c8df2d0af.png
.. image:: https://user-images.githubusercontent.com/30430227/141653794-d6272887-f617-4a95-9b04-edd2513e54d3.png

.. image:: https://user-images.githubusercontent.com/30430227/141653803-22659d54-8796-4ed6-8dec-61bf6590ad38.png
.. image:: https://user-images.githubusercontent.com/30430227/141653815-6dd15737-fd11-426d-86cc-d92dfb052bd7.png

``부딪히기 전까진 고대로 있기``

.. image:: https://user-images.githubusercontent.com/30430227/141653827-a6bb2d2c-9bdd-44cd-b34c-a5c752e6a425.png



그대로 멈춰라
-------------

.. code-block::

 Apply Visual Transform - 시믈레이션 된 위치에 고정

 센터 구 Passive
 Force Field : -500
 Gravity: 0

.. image:: https://user-images.githubusercontent.com/30430227/141677995-8fecd0bb-5dd4-49aa-b7a7-061ee3fa926e.png

.. image:: https://user-images.githubusercontent.com/30430227/141677961-8cb1b26b-155b-4991-8a23-ca23b15593fc.png

``작은 구 추가``

.. image:: https://user-images.githubusercontent.com/30430227/141678036-de5999ae-2be3-454a-ac8b-55eb94074159.png

