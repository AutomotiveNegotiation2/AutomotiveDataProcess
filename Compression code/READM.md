# Compression Code





### **Compression Code Directory Layout** 

- Binary to PCD.py

- Voxelization, Reconstruction, ROI crop code ( .pcd ).py

- zlma, zlib, bz2 compression code(for .txt data).py



### **Compression Code Manual**



#### 1. Binary to PCD

- 파일 경로 지정

  - file_name : bin 확장자 Point cloud Data 경로 지정

- bin 확장자 파일의 visualization

- bin 확장자 파일을 .pcd 확장자 파일로 저장

  

#### 2. Voxelization, Reconstruction, ROI crop code ( .pcd )

- 파일 경로 지정

  - data_path : PCD파일의 경로 위치
  - data_name : PCD파일 이름

- Voxelization ( .pcd )

  - Point Cloud Data(.pcd)파일을 voxelization  ( **voxel_size** 변수를 조정 가능 )
  - visualization하여 voxelization의 결과 확인

  

- Surface Reconstruction ( .pcd )

  -  3가지 방식 : Alpha shapes, Ball pivoting, Poisson surface reconstruction 

    - Alpha shapes : **ll** 변수를 조정하여 Surface Reconstruction 확인 가능 

    - Ball pivoting : **radii** 변수를 조정하여  Surface Reconstruction 확인 가능 

    - Poisson surface reconstruction : **depth** 변수를 조정하여 Surface Reconstruction 확인 가능

    - 출처 : [http://www.open3d.org/docs/latest/tutorial/Advanced/surface_reconstruction.html]

    

- ROI crop

  - ROI crop 정보가 들어있는 .json 파일과 파일 경로 필요

  - cropped.json 파일을 통해서 Point Cloud Data 내 일부분을  crop 가능

  - 출처 : [http://www.open3d.org/docs/0.9.0/tutorial/Basic/pointcloud.html]

    

#### 3. zlma, zlib, bz2 compression code

- CAN data Compression ( .csv )

  - 파일 경로 지정
    - file_path : CAN 파일의 경로 위치
    - file_name : CAN 파일 이름

  - 데이터 압축 방식 선택 : bz2, zlib, lzma
    - OUTPUT
      - 압축 전, 후, 복원된 전체 데이터의 크기
      - 압축 전, 후, 복원된 ID 데이터 크기
      - 전체 데이터 압축 비율
      - ID 데이터 압축 비율

  

-  GPS data(주행) Compression, GPS data(정차) Compression ( .json )

  - 파일 경로 지정
    - file_name : GPS 파일 이름
  - 데이터 압축 방식 선택 : bz2, zlib, lzma
    - OUTPUT
      - 압축 전, 후, 복원된 전체 데이터의 크기
      - 전체 데이터 압축 비율

- BSM Compression ( .txt )

  - 파일 경로 지정
    - file_path : BSM 파일의 경로 위치
    - file_name : BSM 파일 이름
  - 데이터 압축 방식 선택 : bz2, zlib, lzma
    - OUTPUT
      - 압축 전, 후, 복원된 전체 데이터의 크기
      - 전체 데이터 압축 비율



