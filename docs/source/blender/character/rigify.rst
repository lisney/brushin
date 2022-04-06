Rigify
========


기존방식
------------

1. Bone

`In Front Axies: 1, 무릎 joint는 좀 더 앞쪽으로`

.. image:: https://user-images.githubusercontent.com/30430227/138624555-099165bf-4aa5-4625-84e0-3cbab4d0611e.png

.. image:: https://user-images.githubusercontent.com/30430227/138624653-80413044-676b-4f08-9bfe-ef996674ba08.png
.. image:: https://user-images.githubusercontent.com/30430227/138624713-e02ec165-d4bb-4af7-bfe1-124f8abdbb2a.png

`F2 - rename`

.. image:: https://user-images.githubusercontent.com/30430227/138624885-15b929d9-dc82-4804-9e55-4f278b9ef3bd.png
.. image:: https://user-images.githubusercontent.com/30430227/138627379-d9c1afbe-7acb-4b0c-8d60-5f45af52702d.png


.. image:: https://user-images.githubusercontent.com/30430227/138624993-43912069-19a9-4334-9edb-5da1f6bf0dee.png

`Move`

.. image:: https://user-images.githubusercontent.com/30430227/138625099-d2cb9ce9-1c9c-4ab8-a994-90e8ba0a8454.png

`Add Bone  'spine'A`

.. image:: https://user-images.githubusercontent.com/30430227/138625312-f5e6aab5-5c76-4dd4-9e38-46922a70c144.png
.. image:: https://user-images.githubusercontent.com/30430227/138625401-cf98505a-8ab5-4437-913b-38e64f1ad8f4.png

`neck, head`

.. image:: https://user-images.githubusercontent.com/30430227/138625522-a9e6b61c-2b2f-447f-b083-ec7b06d2115d.png

`Add Bone 'upper_arm.L, lower_arm.L'`

.. image:: https://user-images.githubusercontent.com/30430227/138625736-0acf4935-d964-4340-a197-96260aeb3123.png
.. image:: https://user-images.githubusercontent.com/30430227/138625753-58a56037-0b99-4204-b144-0daac59d0166.png

`hand.L`

.. image:: https://user-images.githubusercontent.com/30430227/138625964-18fccf1e-b442-432d-a968-2453c7f2fe20.png

`collar.L`

.. image:: https://user-images.githubusercontent.com/30430227/138626396-e3784e52-a1ad-4138-8f08-fb62bdf9de9d.png
.. image:: https://user-images.githubusercontent.com/30430227/138626432-85f2ad17-2df0-44fc-98d5-65ce02e29823.png

.. image:: https://user-images.githubusercontent.com/30430227/138626488-a6058617-bc51-4f25-9458-a81788afb7dc.png

`Extrude Bone 'pelvis.L'`

.. image:: https://user-images.githubusercontent.com/30430227/138626825-8a9423fc-70c8-444e-9a34-f6c378f3e7c4.png

`Parent`

.. image:: https://user-images.githubusercontent.com/30430227/138626865-a987fb8d-6cca-4c89-a947-0fbb8196323d.png

.. image:: https://user-images.githubusercontent.com/30430227/138626960-03b7aca8-d22f-480b-91ce-ac39ee545493.png

.. image:: https://user-images.githubusercontent.com/30430227/138627000-2298d9c7-0b3e-442f-b787-241000279b70.png

.. image:: https://user-images.githubusercontent.com/30430227/138627058-f11bf7bc-bc10-48cc-bf38-ebd8da2ef0d8.png

`Add Bone root'`

.. image:: https://user-images.githubusercontent.com/30430227/138627631-42cb3f8a-6541-47cb-8a2d-b19fcd1d9671.png

`Copy rootBone & Scale & Move 'pelvis_control'`

.. image:: https://user-images.githubusercontent.com/30430227/138627776-67ba6b48-aac6-484f-bcfc-3c5954783db3.png

`Parent`

.. image:: https://user-images.githubusercontent.com/30430227/138627881-edd48738-e7f2-4eb1-8d48-d4432504681b.png

.. image:: https://user-images.githubusercontent.com/30430227/138627929-9041ff99-35ca-405a-baff-465856ae9235.png


2. 컨트롤

`extrude & Clear Parent 'IK.L'`

.. image:: https://user-images.githubusercontent.com/30430227/138628230-b97fa6fa-cf21-4299-ae60-ea49d39a07e6.png

`IK Constraint`

.. image:: https://user-images.githubusercontent.com/30430227/138641713-f0f9354d-1f92-4b56-92de-5cf641a2ab4a.png

`Chain Length: 2, Lock IK`

.. image:: https://user-images.githubusercontent.com/30430227/138642125-e9b8dc75-3938-4674-a2d4-af3652ec29ac.png

`Extrud >Clear Parent > Move 'pole.L'`

.. image:: https://user-images.githubusercontent.com/30430227/138642267-9acb220b-d13f-40e7-8961-f5dbdec1d41b.png
.. image:: https://user-images.githubusercontent.com/30430227/138642284-c70409da-aec3-420a-b45d-720e14ac9530.png

.. image:: https://user-images.githubusercontent.com/30430227/138642453-49075c35-e5a0-408e-a914-2edd148f17a3.png

`pole > Parent`

.. image:: https://user-images.githubusercontent.com/30430227/138642647-5949df89-f531-4da7-a2b7-5fe0b34d05c8.png

`IK bone > Parent`

.. image:: https://user-images.githubusercontent.com/30430227/138644828-e21768ef-3fc1-424f-9ccd-b1b1e385b9bd.png

`foot > Clear Parent > CopyLocation`

.. image:: https://user-images.githubusercontent.com/30430227/138642973-d8342d72-6027-4b73-bcde-64d771ab3f0e.png

.. image:: https://user-images.githubusercontent.com/30430227/138643093-96a62461-b3a9-4e6b-86f4-6835ed6f57ce.png

`Head/Tail: 1`

.. image:: https://user-images.githubusercontent.com/30430227/138643237-0cccd22b-02c8-4ab6-b3fc-95a84e267e93.png

.. image:: https://user-images.githubusercontent.com/30430227/138643252-4676b9a4-5088-4ad3-8649-78b5a3294376.png
.. image:: https://user-images.githubusercontent.com/30430227/138643268-08b29f1a-3b3b-4e74-89c9-de1b67e6ca9b.png

`Symmetrize`

.. image:: https://user-images.githubusercontent.com/30430227/138644419-0b10900e-5737-4772-9f52-2bc0e23fdef2.png

3. Controls > Deform

.. image:: https://user-images.githubusercontent.com/30430227/138645156-f730ba6f-53a9-4b40-b1fb-61bc25f7768b.png

`Alt 클릭, 선택한 모두에 적용`

.. image:: https://user-images.githubusercontent.com/30430227/138645223-28c3647d-882a-405a-a65c-addeab6f8add.png


4. Weight

.. image:: https://user-images.githubusercontent.com/30430227/138645547-a9c55f50-2501-47a9-8b2e-984ed3d4353c.png


5. Custom Shape

.. image:: https://user-images.githubusercontent.com/30430227/138645848-fd15fb8f-74cc-414c-81cb-ab2796302800.png

.. image:: https://user-images.githubusercontent.com/30430227/138645882-0d78fc05-f6c0-4e61-b7aa-a3a9d762e22a.png
.. image:: https://user-images.githubusercontent.com/30430227/138645929-5fc82bca-0f9c-42f0-9603-f19b2ff323e8.png

.. image:: https://user-images.githubusercontent.com/30430227/138645963-e64f5f8a-968d-421a-83b5-76b83fe31fec.png
.. image:: https://user-images.githubusercontent.com/30430227/138645997-e38193e4-9d7a-42bf-99e3-918aae7a9341.png

.. image:: https://user-images.githubusercontent.com/30430227/138646022-b2361a30-22ac-46cc-bc78-db89cc7b60be.png
.. image:: https://user-images.githubusercontent.com/30430227/138646057-6b3e7e57-f1c8-466b-bcef-d1034a6f2d07.png

.. image:: https://user-images.githubusercontent.com/30430227/138646097-52e8417e-14c9-4455-96d2-78cc61c954d1.png

.. image:: https://user-images.githubusercontent.com/30430227/138646155-85155370-267f-4472-abb2-08f10b333755.png


Human
-------

1. Basic Human(Meta Rig

.. image:: https://user-images.githubusercontent.com/30430227/138650536-a6a1a7b7-ebc7-4a32-aa56-0d458cd21ad3.png

`Scale`

.. image:: https://user-images.githubusercontent.com/30430227/138670830-7852676c-a845-45b0-abd1-10f4704a64e8.png

`Edit Mode > Mirror`

.. image:: https://user-images.githubusercontent.com/30430227/138670969-f89ee69e-a094-4bc2-8666-514792035163.png

.. image:: https://user-images.githubusercontent.com/30430227/138671216-96060b27-1dfc-4115-b45a-b7a33ae080e4.png

.. image:: https://user-images.githubusercontent.com/30430227/138671431-d6d2cfcd-1919-453a-84ad-e7b15c99efd9.png

`Select > 'L' > Move `

.. image:: https://user-images.githubusercontent.com/30430227/138671577-9d49b795-01fc-4475-a8f8-d63c881bc0d4.png
.. image:: https://user-images.githubusercontent.com/30430227/138671617-a48bfcc3-2352-4403-928a-367623d56984.png

.. image:: https://user-images.githubusercontent.com/30430227/138671677-f73f6c7e-3bd6-45bc-ae48-1613c509bd4e.png

`heel`

.. image:: https://user-images.githubusercontent.com/30430227/138672173-97631e5a-fa8d-49bd-99ed-24c7752d0919.png
.. image:: https://user-images.githubusercontent.com/30430227/138672241-5fe6f737-0316-4afe-a9b0-66c130b2c96b.png

.. image:: https://user-images.githubusercontent.com/30430227/138672325-736e9ab8-40b3-4e47-a3ed-1a0177eed058.png


2. Generate Rig

`Apply > All Transform`

.. image:: https://user-images.githubusercontent.com/30430227/138674756-24a71edc-6ec5-46db-9a55-b3ee47837cd1.png

`Generate Rig`

.. image:: https://user-images.githubusercontent.com/30430227/138674845-ead85ef1-92b5-457c-82a2-44cb635d71c1.png

.. image:: https://user-images.githubusercontent.com/30430227/138674913-5c517692-a77a-4a2f-a40c-6c04bc5748aa.png

`Hide metarig`

.. image:: https://user-images.githubusercontent.com/30430227/138675146-a0316b65-dc04-4614-b772-7c2c414488cf.png

.. image:: https://user-images.githubusercontent.com/30430227/138675170-fc1879c8-d67f-4e95-b895-4130c14d4f56.png


3. Auto Weight

.. image:: https://user-images.githubusercontent.com/30430227/138675306-8ad89518-f2ba-4628-b335-e1b7bbe23344.png

`Pose Mode > Move`

.. image:: https://user-images.githubusercontent.com/30430227/138675412-697b91ea-eadd-4071-8f60-5d5cc43f9176.png

`IK/FK`

.. image:: https://user-images.githubusercontent.com/30430227/138675701-436e266f-8f39-4bf7-a12d-d0bb8ded0a4c.png

.. image:: https://user-images.githubusercontent.com/30430227/138675737-3140d941-21df-4ed4-9f54-0a6b41783bcb.png
.. image:: https://user-images.githubusercontent.com/30430227/138675782-b92ddd7e-af5b-48df-95cf-ba003ddead81.png

`heel IK`

.. image:: https://user-images.githubusercontent.com/30430227/138676456-49df32ec-3fb7-4959-85c3-924cbeaba478.png
.. image:: https://user-images.githubusercontent.com/30430227/138676354-febe5ec3-c62c-460c-8cfe-0f3921d6bc8f.png


Dog
-----

1. Model Check

`Foot Z-0`

.. image:: https://user-images.githubusercontent.com/30430227/138677656-21bb2c96-6ac0-4fd1-98fa-22a526165c2a.png

`Center, 꼬리 - 말렸으면 펴줄 것`

.. image:: https://user-images.githubusercontent.com/30430227/138677711-5ef4c62e-adf8-481c-8805-4dd12d999acc.png

`Scale`

.. image:: https://user-images.githubusercontent.com/30430227/138677798-4e084a07-fa97-48e8-a141-80e6f50c7278.png

2. Bone

.. image:: https://user-images.githubusercontent.com/30430227/138677963-e15d82e3-aa77-416d-bc8c-97cde2ebddea.png

.. image:: https://user-images.githubusercontent.com/30430227/138678085-1de54cdb-47a3-4899-acf2-65a8f7365c80.png

`Scale > Apply All Transform > Edit(X-Axis Mirror`

.. image:: https://user-images.githubusercontent.com/30430227/138678176-f8fffb7e-a560-425e-b6bd-29934447f7db.png

`Select Parent/Child  '[, ']`

.. image:: https://user-images.githubusercontent.com/30430227/161682747-4097b487-3e99-4ad6-a805-58e849276a50.png

.. image:: https://user-images.githubusercontent.com/30430227/138687391-05534943-b81e-4fb9-952a-a2b488ae874f.png
.. image:: https://user-images.githubusercontent.com/30430227/138687554-c2ea2426-eaab-40aa-a6f0-c7a9f1b1bf18.png


3. Generate Rig

`Advanced Options, overwrite: 기존 리그를 덮어 쓴다`

.. image:: https://user-images.githubusercontent.com/30430227/138688040-8a455f6c-2242-46de-86d0-8187938efc98.png

`Generate Rig`

.. image:: https://user-images.githubusercontent.com/30430227/138688230-4237eda8-17ca-4e83-9a9e-50ea9b82dec2.png

`Auto Weight`

.. image:: https://user-images.githubusercontent.com/30430227/138688312-07ad1c17-6d75-48e2-a74b-6c694779b33f.png

`Modifier 위치`

.. image:: https://user-images.githubusercontent.com/30430227/138688462-943af043-2a52-4ce0-ac10-566efdb79860.png

`Fix`

.. image:: https://user-images.githubusercontent.com/30430227/138688573-761fbec8-31d7-4cec-82bb-7642ee95c61e.png

.. image:: https://user-images.githubusercontent.com/30430227/138688795-f9a4ef19-8580-4b7b-bb8a-aadd92119e5c.png
.. image:: https://user-images.githubusercontent.com/30430227/138688845-52e64a2f-1da7-4416-b599-4dd19a09a7aa.png

`overwrite`

.. image:: https://user-images.githubusercontent.com/30430227/138688929-8e5259e0-80d7-489a-a168-ba9d7fb4d4e4.png

.. image:: https://user-images.githubusercontent.com/30430227/138690127-a468bc36-916d-415e-bd63-ca32351303df.png
.. image:: https://user-images.githubusercontent.com/30430227/138690221-5d22186b-6d5b-4303-be01-b222d33748ee.png

.. image:: https://user-images.githubusercontent.com/30430227/138690522-46f2de88-df0e-49b3-925b-24a347159d97.png


horse 
------

1. Bone

.. image:: https://user-images.githubusercontent.com/30430227/138847668-860d0d19-619b-4d9f-a366-3e98b601aa8c.png

.. image:: https://user-images.githubusercontent.com/30430227/138847791-566be3f4-7b91-422c-9ec1-3f0c49a52f43.png

`X-Axis Mirror`

.. image:: https://user-images.githubusercontent.com/30430227/138850086-17979814-57c1-4d43-a266-8a56bad958fb.png

`Delete Hair Bone`

.. image:: https://user-images.githubusercontent.com/30430227/138850268-2549b184-7f8d-43d5-8d9f-836e253f444f.png
.. image:: https://user-images.githubusercontent.com/30430227/138850300-9800f7ce-2fe9-4b39-a899-30a2d096696b.png

`Bug Fix - 귀에 Parent 되어 있는 것을 머리로`

.. image:: https://user-images.githubusercontent.com/30430227/138850536-8c0c0979-d764-42b6-b94d-2b1f61c926ac.png

`Mouse > Parent`

.. image:: https://user-images.githubusercontent.com/30430227/138850927-75f0e9f8-1271-47bf-802a-dd928782dd10.png

.. image:: https://user-images.githubusercontent.com/30430227/138851338-7103930e-3c01-49f8-a0d7-866aa6508b9c.png
.. image:: https://user-images.githubusercontent.com/30430227/138851475-4c416971-cc1f-4dda-9ef8-ef26c6009ed0.png

.. image:: https://user-images.githubusercontent.com/30430227/138851648-35c6db4b-18f0-47f1-a8fb-006521f5d223.png

`Duplicate Bones`

.. image:: https://user-images.githubusercontent.com/30430227/138851922-6a79c39b-323a-4d74-9e59-f048d5437fc3.png
.. image:: https://user-images.githubusercontent.com/30430227/138851967-4d89c833-0ea2-4366-ab2d-6b7d3bab366b.png

`Tail > Move > Edit >Batch Rename Ctrl - F2' > Symmetrize`

.. image:: https://user-images.githubusercontent.com/30430227/138852851-49dc7be1-d4a3-4b3a-9b90-49ac77209270.png

.. image:: https://user-images.githubusercontent.com/30430227/138853117-9c453a0e-7955-4941-858e-cb0e9b58957a.png


2. Generate Rig

.. image:: https://user-images.githubusercontent.com/30430227/138853400-2232465a-51fd-4d1a-8e56-30ab1af4e580.png

`Auto Weight - 앞 발 이상?`

.. image:: https://user-images.githubusercontent.com/30430227/138853645-68921809-2583-4f3c-b69f-d6b35efee8e7.png


고양이 인간
------------

1. Bone 

.. image:: https://user-images.githubusercontent.com/30430227/138863352-eb15f73d-713f-4463-a81d-5c048c09146d.png
.. image:: https://user-images.githubusercontent.com/30430227/138863401-2f4563d6-7550-49af-8754-23028c108a94.png

`ear & tail 'Hide' > Delete All`

.. image:: https://user-images.githubusercontent.com/30430227/138863666-b73d7521-f64e-4b62-8c50-e7cd04b2af9a.png

.. image:: https://user-images.githubusercontent.com/30430227/138863754-958c3855-5081-41e5-acc4-c656d3e79e29.png
.. image:: https://user-images.githubusercontent.com/30430227/138863802-ff2cc168-00e9-4b94-aa00-868b8372a965.png

`In Edit Mode > Move Layer 1`

.. image:: https://user-images.githubusercontent.com/30430227/138864043-86bb949b-416a-4910-9c42-5cd5a7576602.png

`Combine Bones Ctrl - j > Layer 'Shift - Click'`

.. image:: https://user-images.githubusercontent.com/30430227/138864431-ffc1038e-ec34-4ae1-a61f-f31c30a26953.png

.. image:: https://user-images.githubusercontent.com/30430227/138864295-fc1b5ec6-83b1-403f-a3b5-20826c2e56dc.png
.. image:: https://user-images.githubusercontent.com/30430227/138864469-66435247-4405-467e-b300-5431ae5f8b14.png

`Bone Edit`

.. image:: https://user-images.githubusercontent.com/30430227/138864782-20e12df7-5234-4f1b-8cdc-ef1d64825883.png
.. image:: https://user-images.githubusercontent.com/30430227/138865166-c012c962-cea9-4e96-bffb-6b8ee1e50fd4.png

`Tail Move > Edit, 꼬리 뼈에 뿥일 때 '/' 로컬 뷰`

.. image:: https://user-images.githubusercontent.com/30430227/138865506-0f9954ba-cb49-437e-9c56-00cfe4befddf.png

.. image:: https://user-images.githubusercontent.com/30430227/138865580-724d258c-fc45-4346-8cf9-cbaf1023c621.png

.. image:: https://user-images.githubusercontent.com/30430227/138865971-35d5e5a1-9b5e-4b40-8131-e04b6f11f2df.png

`귀`

.. image:: https://user-images.githubusercontent.com/30430227/138866067-a7bf2778-3e5a-4736-a68f-445d1f0c3152.png
.. image:: https://user-images.githubusercontent.com/30430227/138866161-11763f10-3dcb-4b1e-a261-6009a093236a.png

.. image:: https://user-images.githubusercontent.com/30430227/138866293-5149d18c-3bed-48e8-b481-2d3e93d20d95.png


2. Generate Rig

`꼬리는 가능, 귀는 컨트롤이 안 생긴다`

.. image:: https://user-images.githubusercontent.com/30430227/138866832-faad50b9-23a2-4111-9762-633f602ae095.png


3. 귀 뼈를 지우고 Breast 뼈를 복사하여 귀에 붙인다 > Parent to Head

.. image:: https://user-images.githubusercontent.com/30430227/138867168-93235868-38d7-43bb-a385-cc110a54a062.png

`귀 컨트롤이 생김`

.. image:: https://user-images.githubusercontent.com/30430227/138867384-d157972f-884f-4a00-a12a-4e12810a0b06.png


Rigify Bone
-----------

`본 생성 > Edit Mode`

.. image:: https://user-images.githubusercontent.com/30430227/138868561-3869e116-4501-4ba5-97d8-39d5aeccaf80.png

`기존 본 삭제 > Basic.copy_chain`

.. image:: https://user-images.githubusercontent.com/30430227/138868670-0d293f75-f5a7-4e5f-b85b-6b01d0f5c08f.png

`Generate Rig`

.. image:: https://user-images.githubusercontent.com/30430227/138868878-eff9621b-3d8a-4f2c-8f58-129627045a0a.png

`Edit Mode > Add Bone > Subdivide`

.. image:: https://user-images.githubusercontent.com/30430227/138869184-9193d457-c6f7-4995-b8ad-d60e6bd9ebda.png

`Pose Mode > Rigify Type`

.. image:: https://user-images.githubusercontent.com/30430227/138869635-239dceee-f0aa-49ac-a00e-df315fd3cedb.png

.. image:: https://user-images.githubusercontent.com/30430227/138869722-7d3fdf16-0d1e-41bf-a777-5fc9fcbe09a0.png

`Generate Rig`

.. image:: https://user-images.githubusercontent.com/30430227/138869830-a80d601b-8fed-4f78-915e-8dbd2e7366b0.png


Custom Rig 1
-------------

1. Bone

.. image:: https://user-images.githubusercontent.com/30430227/138995359-5cd3802c-c5ca-4759-bb21-d2aad3bb1c18.png

`Edit Mode > Delete > Add Leg > Edit`

.. image:: https://user-images.githubusercontent.com/30430227/138995533-2da3090d-39a7-4c38-bb8d-4f1c10731d32.png

.. image:: https://user-images.githubusercontent.com/30430227/138995562-69329c66-086b-44be-a179-ef3d9a8644f7.png
.. image:: https://user-images.githubusercontent.com/30430227/138995803-00cb2481-0deb-40cb-a56f-b1f4dfc912a6.png

`Add Bone 'spine'`

.. image:: https://user-images.githubusercontent.com/30430227/138999232-0cfcf54c-c95b-4cd3-aa12-0dd5f31005d8.png
.. image:: https://user-images.githubusercontent.com/30430227/138999309-4e6e8a20-c754-470c-b32a-5f9888536017.png

`Pose Mode > Rig Type: Basic_spine`

.. image:: https://user-images.githubusercontent.com/30430227/138999459-3ed23a2f-49a4-497a-b784-fda63f10054b.png

.. image:: https://user-images.githubusercontent.com/30430227/138999481-00329065-52a2-4774-8bad-61057fbd4920.png

`Add Arm 'limbs.arm'`

.. image:: https://user-images.githubusercontent.com/30430227/138999859-126cffdf-58f8-4e7e-8c10-74acab37842f.png

`Add Bone > 'collar.L' > basic_super_copy > Parent > Parent to spine`

.. image:: https://user-images.githubusercontent.com/30430227/138999894-c8fda52e-07e7-46c1-a53f-fc1699aa1b80.png

.. image:: https://user-images.githubusercontent.com/30430227/139000092-2551277e-7f0a-47bf-ab88-737b67b0130b.png

.. image:: https://user-images.githubusercontent.com/30430227/139000726-1eaaa749-7bae-4aee-925b-c09ab55d1849.png

`Extrude > 'pelvis.L' > basic_super_copy(No Control >Parent > Parent to spine`

.. image:: https://user-images.githubusercontent.com/30430227/139000312-03eff134-3cfb-4f59-9a65-d9421a8d983e.png

.. image:: https://user-images.githubusercontent.com/30430227/139000771-72d31573-8ffc-421d-a277-9044180e5d0c.png

`spine_super_head > Parent - 목 본의 위치는 spine의 위치와 같아야 한다`

.. image:: https://user-images.githubusercontent.com/30430227/139000449-cc716432-f5ca-43b9-99b1-e71c1d8147c6.png

.. image:: https://user-images.githubusercontent.com/30430227/139000519-22ecd94d-0fc5-49f1-81ac-7b41fa0cce2d.png

.. image:: https://user-images.githubusercontent.com/30430227/139000852-c33723e8-604f-4ebd-8090-0eb663e7f46d.png

`Pose Mode > Connect chain 체크`

.. image:: https://user-images.githubusercontent.com/30430227/139000968-84bd2545-46fa-4948-9304-0334b46cd14e.png

`Symmetrize`

.. image:: https://user-images.githubusercontent.com/30430227/139001045-ca63a37f-4592-41ff-aa0f-214bb1f4fda0.png

`spine_basic_tail`

.. image:: https://user-images.githubusercontent.com/30430227/139001366-3b1c6496-d3da-4ab8-aa20-e565e7b76b3d.png

`rotate > Edit > Extrude > Parent to spine`

.. image:: https://user-images.githubusercontent.com/30430227/139001720-37334607-de65-45c8-acea-cb1ab3fe5153.png

.. image:: https://user-images.githubusercontent.com/30430227/139001785-f20e3c53-fc13-4134-9f51-0b5faf8620ec.png
.. image:: https://user-images.githubusercontent.com/30430227/139001799-1c604217-838e-440b-a386-86dc7dd3f370.png

`Add Bone > 'ear.L','ear1.L' > Parent to Head > Pose Mode 'limbs.simple_tentacle'`

.. image:: https://user-images.githubusercontent.com/30430227/139002039-27239c16-ab7a-4be6-a0bd-41816e912b86.png
.. image:: https://user-images.githubusercontent.com/30430227/139002070-e43f93a1-cfa3-4507-a3e8-cbfadbe200e8.png

.. image:: https://user-images.githubusercontent.com/30430227/139002161-89ba5925-a91d-4d8f-9fc0-ce9325f3264c.png


2. Generate Rig

.. image:: https://user-images.githubusercontent.com/30430227/139002438-9f4996d8-e445-4e0d-838b-a853468ea57d.png


Custom Rig 2
---------------

1. Bone

`Single Bone > Edit Mode > Delete > 'limbs.leg'`

.. image:: https://user-images.githubusercontent.com/30430227/139008086-826bc315-5523-44aa-8946-6946250dc1b5.png

`Move > Edit`

.. image:: https://user-images.githubusercontent.com/30430227/139008232-42335c76-805c-4abc-8dc9-153d75ccd276.png
.. image:: https://user-images.githubusercontent.com/30430227/139008267-7766b6aa-4d45-47fb-a000-7e6a969ccae2.png

`spines.basic_spine`

.. image:: https://user-images.githubusercontent.com/30430227/139008393-d5e85329-83a2-45fd-820b-82c5c4d226d3.png

.. image:: https://user-images.githubusercontent.com/30430227/139008513-00357de8-df92-4316-9cc0-e689d7824b8d.png
.. image:: https://user-images.githubusercontent.com/30430227/139008552-e581351c-b428-4883-b319-b8d7b8c19797.png

`limbs.arm`

.. image:: https://user-images.githubusercontent.com/30430227/139008898-83ec101c-f2e0-43f3-8bf5-a0b6361ddf1f.png

.. image:: https://user-images.githubusercontent.com/30430227/139008919-5eb698e4-081c-49cb-8fcd-0b5d38ff83fd.png

`limbs.simple_tentacle > Delete > 'finger', 'finger1 > Edit`

.. image:: https://user-images.githubusercontent.com/30430227/139008983-025aa61f-ac74-4347-b230-e00031b2d862.png

.. image:: https://user-images.githubusercontent.com/30430227/139009027-d8490421-be0b-4e7c-a68e-d141a07833dc.png
.. image:: https://user-images.githubusercontent.com/30430227/139009292-18053cd4-8ad3-4a08-b113-63727c4926e4.png

`Duplicate`

.. image:: https://user-images.githubusercontent.com/30430227/139009348-d0cd46c4-51ca-4c97-b017-c45f4fd86918.png

`Simmetrize`

.. image:: https://user-images.githubusercontent.com/30430227/139010044-73e6dcde-6e74-4dad-aed6-d286f4a9b9a0.png

`spines.super_head > Dissolve Bone`

.. image:: https://user-images.githubusercontent.com/30430227/139010218-53f55d1e-389a-4eda-bf39-159b1c0af08f.png

.. image:: https://user-images.githubusercontent.com/30430227/139010260-dd360a0a-005e-4de7-b4db-1522e73ab522.png

.. image:: https://user-images.githubusercontent.com/30430227/139010452-ab785eae-5acc-4db5-882f-173e9170db76.png
.. image:: https://user-images.githubusercontent.com/30430227/139010473-5322aa82-6a90-441c-8edd-c0b5091297a9.png

.. image:: https://user-images.githubusercontent.com/30430227/139010668-b6eb5afb-9f18-4329-8145-65790257ca50.png

`Pose Mode > Connect Chain`

.. image:: https://user-images.githubusercontent.com/30430227/139010690-6dad30ac-7114-4d8b-b69b-c313ef1b6947.png

.. image:: https://user-images.githubusercontent.com/30430227/139010719-5767e11c-186a-45ef-892b-13516205b256.png

`Edit Mode > Add Bone > 'tentacle.L' > Extrude`

.. image:: https://user-images.githubusercontent.com/30430227/139010881-8310ec27-6f60-4dfc-834f-131a2e089b56.png
.. image:: https://user-images.githubusercontent.com/30430227/139010940-ef23c5e1-64f6-4273-928b-49c05466c90d.png

`Pose Mode > limbs.simple_tentacle`

.. image:: https://user-images.githubusercontent.com/30430227/139011072-69c278f0-8e93-4709-9383-dfe6e1f9db2a.png

`Simmetrize > Extrude`

.. image:: https://user-images.githubusercontent.com/30430227/139011324-3aabe692-4268-4e7e-830b-bb3d60c1a568.png
.. image:: https://user-images.githubusercontent.com/30430227/139011364-4015bd9d-da98-41be-9b40-e254362afd95.png

`Add Bone > 'eye' > Rig Type: Deform Uncheck > 눈 알의 중심으로 이동 Select to Cursor(Not offset`

.. image:: https://user-images.githubusercontent.com/30430227/139012295-3d7f8a1b-1eba-4edf-b384-c09ab4d5b3b1.png

.. image:: https://user-images.githubusercontent.com/30430227/139011628-d3c01956-6cf8-4bed-bde2-ac6bf9f318f1.png

.. image:: https://user-images.githubusercontent.com/30430227/139011862-e9b5575c-d98b-4a0e-b239-74b276245116.png

.. image:: https://user-images.githubusercontent.com/30430227/139012141-fd87c610-59b3-4061-acbe-7e11f0a3bb10.png

`Extrude > 'pelvis.L' > Rig Type: Control Uncheck > Simmetrize`

.. image:: https://user-images.githubusercontent.com/30430227/139012538-302d906e-e3bb-4dd1-ae23-42066412586c.png
.. image:: https://user-images.githubusercontent.com/30430227/139012563-16caaa7a-98f0-4b96-ac37-ed05c488c087.png

.. image:: https://user-images.githubusercontent.com/30430227/139012754-dd86f5e0-b7c1-4e0a-8708-0b218a206e8f.png

`Copy pelivs > Batch Rename - 펠비스, 체스트, 스컬 본은 말단 본의 변형 영역을 제한한다`

.. image:: https://user-images.githubusercontent.com/30430227/139013190-fc1791a1-dfde-478d-a79d-c57a1b528daa.png

.. image:: https://user-images.githubusercontent.com/30430227/139013312-b46c65a1-6ba7-4b47-bf04-452ce184e6d7.png

`Copy chest > Batch Rename`

.. image:: https://user-images.githubusercontent.com/30430227/139013527-97245fa3-baeb-448f-ac91-9d174ebcf7f4.png

.. image:: https://user-images.githubusercontent.com/30430227/139013561-84ff2f47-222a-48fa-9b12-d4d9b23269dd.png

`Parent`

.. image:: https://user-images.githubusercontent.com/30430227/139013819-1bc2d354-b719-414d-9c25-f9cf501fdf73.png

.. image:: https://user-images.githubusercontent.com/30430227/139013776-bf64e22e-dd3d-4a79-9c75-c092f1062d1c.png

.. image:: https://user-images.githubusercontent.com/30430227/139013875-abb08649-fcd5-4c9b-b8d0-12f2e3da1db5.png

.. image:: https://user-images.githubusercontent.com/30430227/139013978-b813ccf7-53ef-4dad-9caa-90111c27bdfe.png

.. image:: https://user-images.githubusercontent.com/30430227/139014061-3813faaf-6089-49c4-87c9-90e98e76b979.png

.. image:: https://user-images.githubusercontent.com/30430227/139014129-8e6fb335-276f-4cb2-acce-edc3a64b1ecf.png

.. image:: https://user-images.githubusercontent.com/30430227/139014299-28a2bf6d-4702-4974-850d-2e4dd3fdc464.png


2. Generate Rig

.. image:: https://user-images.githubusercontent.com/30430227/139014552-864e024d-23de-41e9-a2b2-0e511113d67d.png

`눈 Weight > 눈 메쉬 와 릭 쉐이프 선택 후 Pose Mode `

.. image:: https://user-images.githubusercontent.com/30430227/139015251-7a8ceecd-74b4-4199-9366-9d776646e1c7.png

.. image:: https://user-images.githubusercontent.com/30430227/139016368-fa04b9ad-12fb-4fd7-8f6b-d1d7a299379d.png



팔 다리 IK/FK 
-------------

IK는 Pin(고정 애니메이션에 사용

`Pole Target`

.. image:: https://user-images.githubusercontent.com/30430227/139038572-f75c9c5b-6b64-4483-9eb9-120565f398a0.png

`Toggle Pole - 클래식 폴 타깃`

.. image:: https://user-images.githubusercontent.com/30430227/139038711-b763b2c4-78a6-4121-a68d-01fadbe8f4dd.png

.. image:: https://user-images.githubusercontent.com/30430227/139040802-d83208a8-92bc-4d1e-ab27-43501cffcb71.png

`IK 스트레치 - 이동`

.. image:: https://user-images.githubusercontent.com/30430227/139038890-78552b11-f0e7-4cf8-8fd6-4bf5d527fc82.png

`FK 스트레치 - 스케일`

.. image:: https://user-images.githubusercontent.com/30430227/139041151-2bb3dc49-98c0-44d5-a746-0ac5b49ada39.png

`FK Limb 도 고정 가능(좌 Off 우 On`

.. image:: https://user-images.githubusercontent.com/30430227/139041659-20bb7452-4cf7-4b6b-bd8d-446a80295f42.png

.. image:: https://user-images.githubusercontent.com/30430227/139041564-1bfd6034-d32f-4aca-b98f-faefa730672b.png
.. image:: https://user-images.githubusercontent.com/30430227/139041713-f07e6ca7-db16-4e65-82e6-4e1aafca9f41.png

`IK to FK(FK 모드 - IK 컨트롤 FK 위치로`

.. image:: https://user-images.githubusercontent.com/30430227/139042487-9ee81f72-6e4f-427c-a437-84c82a314ab0.png

.. image:: https://user-images.githubusercontent.com/30430227/139042436-e13d5158-7c48-4e00-9fbe-acba7b78799d.png
.. image:: https://user-images.githubusercontent.com/30430227/139042519-11422d39-b6f4-4d4d-894b-c0585e4d4acd.png

`팔에 없는 컨트롤`

.. image:: https://user-images.githubusercontent.com/30430227/139043193-0aff57b1-4564-4e5b-96b0-444e28a0f257.png
.. image:: https://user-images.githubusercontent.com/30430227/139043274-00436c81-b92f-4766-9db3-1f1aff0aa81f.png


기타 
------

`torso 는 척추 전체, hips/chest 는 상반 하반 컨트롤`

.. image:: https://user-images.githubusercontent.com/30430227/139045135-795624a4-6b29-4e75-8366-99b24fdacc7a.png

`꼬리가 한 방향으로만 회전하는 이유`

.. image:: https://user-images.githubusercontent.com/30430227/139045388-aabfd963-edc5-4f2d-80bf-5d15f16530c8.png

.. image:: https://user-images.githubusercontent.com/30430227/139045693-18cdb7b4-ab51-4a0c-bab6-63e85a365185.png
.. image:: https://user-images.githubusercontent.com/30430227/139045807-2092513d-6631-421b-a576-5eaaff156aa9.png

`Tweak 컨트롤 - 카툰 애니메이션, 근육 효과`


참조이미지(Empty-Image
--------------------------------

`Tweak Layer Off`

.. image:: https://user-images.githubusercontent.com/30430227/139056779-fd683aeb-325f-4d45-958b-24be2a214f88.png

`팔 FK`

.. image:: https://user-images.githubusercontent.com/30430227/139056975-0250fcfb-fe0e-4dd8-b91d-df1a4018960d.png
.. image:: https://user-images.githubusercontent.com/30430227/139057016-7f86882b-932b-4164-add9-85ca50385a1a.png

`다리 - 지탱하는 다리 - IK, 발 차는 다리 - FK`

.. image:: https://user-images.githubusercontent.com/30430227/139057177-ab60c6aa-61da-4fdc-95cf-27b861a35bfb.png
.. image:: https://user-images.githubusercontent.com/30430227/139057215-9327b679-1032-4479-b251-34e85a49211c.png

.. image:: https://user-images.githubusercontent.com/30430227/139059656-359a7eb8-f7d2-4aac-abea-0d34e713e370.png


1. Torso
 
`Transform Ori 'Local'`

.. image:: https://user-images.githubusercontent.com/30430227/139057446-24ced9e4-a3d0-42ce-862e-8a4279e6ae6a.png

.. image:: https://user-images.githubusercontent.com/30430227/139057488-64562a72-c0e8-466b-86cc-3e05930a68ab.png
.. image:: https://user-images.githubusercontent.com/30430227/139057523-39bd5231-0000-4b67-9cb3-8aec669e12e1.png

.. image:: https://user-images.githubusercontent.com/30430227/139057548-2bacdc45-19f6-4090-b522-af136a5d5e29.png


2. 팔 

`첫 번째 방법 단축키 'R, R'`

`두 번째 방법 Auto IK `

.. image:: https://user-images.githubusercontent.com/30430227/139059850-4d271b56-6014-4646-b485-b6d8d584f7d9.png

.. image:: https://user-images.githubusercontent.com/30430227/139060130-13484f79-e033-4c0a-b8b5-84b010d8923b.png


3. 포즈 

.. image:: https://user-images.githubusercontent.com/30430227/139167175-2036afe0-7b01-4c7b-be47-327c154a08ae.png

.. image:: https://user-images.githubusercontent.com/30430227/139167497-25640ed5-5c6f-4f4a-89cc-15c5c5ca34e2.png



Weight Paint
--------------

`Vertex Groups filter`

.. image:: https://user-images.githubusercontent.com/30430227/139240618-e948f53f-ed04-4695-9770-2c8a100ed8df.png

`선택 Vertex의 정보, Deform은 뼈, Normallize 전체 웨이트의 합이 1로`

.. image:: https://user-images.githubusercontent.com/30430227/139241173-56efea8f-c3c0-439c-bbce-4b59b64e7714.png

`Auto Normalize: weight 값을 1로 유지 하기 위해- 페인트 시 기존 그룹의 weight를 자동으로 지워준다- 위의 Normallize 참고`

.. image:: https://user-images.githubusercontent.com/30430227/139243722-8c9769f9-31b3-4593-b4eb-910f2c7a977e.png

.. image:: https://user-images.githubusercontent.com/30430227/139244225-704c22d7-16f7-4500-b950-b5a8b01698bb.png
.. image:: https://user-images.githubusercontent.com/30430227/139244339-e816eb13-2eab-45a2-bdda-67b7098a48fb.png

.. image:: https://user-images.githubusercontent.com/30430227/139244413-a4356888-4f10-4e08-a745-0d8bb55f09a3.png

`반대 편 뼈 미러 페인트 - 좌 그저 미러 페인트/ 우 반대 뼈로 미러페인트 `

.. image:: https://user-images.githubusercontent.com/30430227/139245172-40dd0d55-abce-4dd0-8303-3cb68ef277e7.png
.. image:: https://user-images.githubusercontent.com/30430227/139245214-1f47ebfc-9a9f-46bd-9dbb-272efbfdf2de.png

`오버레이 모드 Shift - Alt - Z`

.. image:: https://user-images.githubusercontent.com/30430227/139247370-22ad976b-ef55-4173-a4b3-662f5eac167b.png
.. image:: https://user-images.githubusercontent.com/30430227/139247393-2321435d-0d3c-4fc0-970f-58d18c71ad65.png

.. image:: https://user-images.githubusercontent.com/30430227/139247443-164af663-ed45-4efe-919b-936974741edd.png

`Restrict 체크 - 해당 본 vertex 그룹에 속한 vertex 에만 영향을 준다`

.. image:: https://user-images.githubusercontent.com/30430227/139248804-71e31a36-c686-4ab9-94bd-b98513c3f533.png


**기초 페인팅**

1. 팔 페인트

.. image:: https://user-images.githubusercontent.com/30430227/139245830-ebda2f5c-c4f2-49ab-894c-3f21c7ba44a6.png

`앞 부분은 약하게 weight 를 증가시킨다`

.. image:: https://user-images.githubusercontent.com/30430227/139245901-d995c6b8-3559-45d6-a340-a7a07f8f9f1c.png
.. image:: https://user-images.githubusercontent.com/30430227/139246029-8e820506-0bc6-4d3a-9d5b-517529047f4b.png

`뒷 부분은 팔 weight가 지나치므로 Spine 쪽을 증가시킨다`

.. image:: https://user-images.githubusercontent.com/30430227/139246284-74650db8-78f8-4f35-92ce-00ecb5298a6e.png
.. image:: https://user-images.githubusercontent.com/30430227/139246323-1695ac90-e703-496b-9536-abd4f8b492df.png

`머리 - 턱 부분을 증가시킨다`

.. image:: https://user-images.githubusercontent.com/30430227/139246547-66d3dd6d-5869-4b3b-8346-b9ded2094428.png
.. image:: https://user-images.githubusercontent.com/30430227/139246593-641e4c08-24b2-422a-b956-48ebd60c7a4d.png

`collar`

.. image:: https://user-images.githubusercontent.com/30430227/139246791-10581bdb-48da-4915-a6fd-2a8fd66878e8.png
.. image:: https://user-images.githubusercontent.com/30430227/139246814-38b66c4d-00d0-4c0b-9819-2b3d4ee805af.png

`어깨 위 파인 부분 - Blur`

.. image:: https://user-images.githubusercontent.com/30430227/139247191-d85bf26d-6854-4dbf-9706-d507a03e1a75.png
.. image:: https://user-images.githubusercontent.com/30430227/139247245-a698ef96-d4eb-4b97-95ea-d6047a859883.png


2. 다리

`IK 컨트롤 이동`

.. image:: https://user-images.githubusercontent.com/30430227/139247691-75c562a8-1bc9-4d79-9a2a-1b7f34909a58.png
.. image:: https://user-images.githubusercontent.com/30430227/139247755-cc24653e-14d3-4e07-83c8-e7138ce1c7b8.png

`Pelvis > Add`

.. image:: https://user-images.githubusercontent.com/30430227/139247890-1ff66c38-015b-46d2-b372-d654aef6be61.png
.. image:: https://user-images.githubusercontent.com/30430227/139248040-f30e503f-03e1-4416-8b5c-81a572525dad.png

`Spine`

.. image:: https://user-images.githubusercontent.com/30430227/139248193-1e00feb2-5504-46b6-ba8e-3f9cf6f4c897.png
.. image:: https://user-images.githubusercontent.com/30430227/139248165-6785c9c5-5d06-4aaa-98e7-bda24826caf2.png
.. image:: https://user-images.githubusercontent.com/30430227/139248234-1fcb99e0-8b4d-41a1-bb98-fa78340404dc.png


3. Unparent 방법

`Clear and keep Transform`

.. image:: https://user-images.githubusercontent.com/30430227/139249313-792a37d6-7ab5-4630-9322-2dc6f43b68b1.png

`Delete All Groups`

.. image:: https://user-images.githubusercontent.com/30430227/139249468-45681c49-47d1-4244-9bd8-a1b9bf45de35.png

`Delete Armature Modifier`

.. image:: https://user-images.githubusercontent.com/30430227/139249574-1e813ef1-ba67-4163-8d9f-779dd01b21b5.png


**Rigify Weight**

`Bone 보이게 Shift - 오른쪽 두 번째 라인 레이어 클릭`

.. image:: https://user-images.githubusercontent.com/30430227/139250242-c52805fe-d2b5-4cd5-9c5b-612ebfcf7629.png

`컨트롤로 포즈를 잡은 후 본을 선택하여 페인팅한다`

.. image:: https://user-images.githubusercontent.com/30430227/139250288-d9fa897d-03e7-43d1-bc80-8098ccf043a0.png


**Rig widh Cloth**

`옷에 With Empty Groups >몸 선택 후 옷 선택> Weight Paint`

.. image:: https://user-images.githubusercontent.com/30430227/159213866-497894a4-b7cc-4ef2-bb4d-ec0dc00c8032.png

.. image:: https://user-images.githubusercontent.com/30430227/159214129-0bef23fb-5d71-42d5-a657-649abd446843.png

