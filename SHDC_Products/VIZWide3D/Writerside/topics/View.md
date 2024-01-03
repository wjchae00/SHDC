# View

## BackupCamera
<procedure title="카메라 백업" collapsible="true">
<note>BackupCamera() → {Data.UUIDv4}</note>

**Example**
```Javascript
//카메라 백업
let camera = vizcore.View.BackupCamera();
```
**Returns**

| Type        | Description |
|-------------|-------------|
| Data.UUIDv4 | 백업 아이디      |
</procedure>
 
## BoxZoomByArea
<procedure title="영역을 확대" collapsible="true">
<note>BoxZoomByArea(x1, y1, x2, y2)</note>

**Example**
```Javascript
//영역을 확대
vizcore.View.BoxZoomByArea(100, 100, 600, 600);
```
**Parameters**

| Name | Type   | Description          |
|------|--------|----------------------|
| x1   | Number | 위치                   |
| y1   | Number | 위치                   |
| x2   | Number | 위치                   |
| y2   | Number | 위치                   |
</procedure>

## CameraZoomIn
<procedure title="설정된 Pivot 기준 Camera Zoom In" collapsible="true">
<note>CameraZoomIn(ratio)</note>

**Example**
```Javascript
//설정된 Pivot 기준 Camera Zoom In
vizcore.View.CameraZoomIn();
vizcore.View.CameraZoomIn(0.5);
vizcore.View.CameraZoomIn(1.0);
vizcore.View.CameraZoomIn(2.0);
```
**Parameters**

| Name  | Type   | Description   |
|-------|--------|---------------|
| ratio | Number | Zoom (기본 1.0) |
</procedure>

## CameraZoomOut
<procedure title="설정된 Pivot 기준 Camera Zoom Out" collapsible="true">
<note>CameraZoomOut(ratio)</note>

**Example**
```Javascript
//설정된 Pivot 기준 Camera Zoom Out
vizcore.View.CameraZoomOut();
vizcore.View.CameraZoomOut(0.5);
vizcore.View.CameraZoomOut(1.0);
vizcore.View.CameraZoomOut(2.0);
```
**Parameters**

| Name  | Type   | Description   |
|-------|--------|---------------|
| ratio | Number | Zoom (기본 1.0) |
</procedure>

## ClearGLWindow
<procedure title="GL Windows View 초기화" collapsible="true">
<note>ClearGLWindow()</note>

**Example**
```Javascript
// GL Windows View 초기화
vizcore.View.ClearGLWindow();
```
</procedure>

## DeleteCameraBackupData
<procedure title="카메라 복원 데이터 제거" collapsible="true">
<note>DeleteCameraBackupData(id)</note>

**Example**
```Javascript
//카메라 백업
let camera = vizcore.View.BackupCamera();
//카메라 복원 데이터 제거
vizcore.View.DeleteCameraBackupData(camera);
```

**Parameters**

| Name | Type         | Description |
|------|--------------|-------------|
| id   | 	Data.UUIDv4 | 백업 아이디      |
</procedure>

## EnableAnimation
<procedure title="카메라 애니메이션 설정" collapsible="true">
<note>EnableAnimation(enable)</note>

**Example**
```Javascript
//카메라 애니메이션 설정
vizcore.View.EnableAnimation(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableEnvironment
<procedure title="환경 조명 설정 - 활성화 / 비활성화" collapsible="true">
<note>EnableEnvironment(enable)</note>

**Example**
```Javascript
//환경 조명 설정 - 활성화 / 비활성화
vizcore.View.EnableEnvironment(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableFog
<procedure title="환경 Fog 활성화" collapsible="true">
<note>EnableFog(enable)</note>

**Example**
```Javascript
//환경 Fog 활성화
vizcore.View.EnableFog(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableGraySacle
<procedure title="GraySacle 모드 활성화 / 비활성화" collapsible="true">
<note>EnableGraySacle(enable)</note>

**Example**
```Javascript
//GraySacle 모드 활성화 / 비활성화
vizcore.View.EnableGraySacle(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableHiddenLine
<procedure title="HiddenLine 모드 활성화 / 비활성화" collapsible="true">
<note>EnableHiddenLine(enable)</note>

**Example**
```Javascript
//HiddenLine 모드 활성화 / 비활성화
vizcore.View.EnableHiddenLine(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableShadow
<procedure title="그림자 효과 활성화 / 비활성화 (WebGL 2.0 지원)" collapsible="true">
<note>EnableShadow(enable)</note>

**Example**
```Javascript
//그림자 효과 활성화 / 비활성화 (WebGL 2.0 지원)
vizcore.View.EnableShadow(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableSilhouetteEdge
<procedure title="윤곽효과 모드 활성화 / 비활성화" collapsible="true">
<note>EnableSilhouetteEdge(enable)</note>

**Example**
```Javascript
//윤곽효과 모드 활성화 / 비활성화
vizcore.View.EnableSilhouetteEdge(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableSilhouetteEdgeToSelectedObject
<procedure title="선택모델 윤곽효과 활성화 / 비활성화" collapsible="true">
<note>EnableSilhouetteEdgeToSelectedObject(enable)</note>

**Example**
```Javascript
//선택모델 윤곽효과 활성화 / 비활성화
vizcore.View.EnableSilhouetteEdgeToSelectedObject(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableSSAO
<procedure title="SSAO효과 모드 활성화 / 비활성화" collapsible="true">
<note>EnableSSAO(enable)</note>

**Example**
```Javascript
//SSAO효과 모드 활성화 / 비활성화
vizcore.View.EnableSSAO(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## EnableWireframe
<procedure title="Wireframe 모드 활성화 / 비활성화" collapsible="true">
<note>EnableWireframe(enable)</note>

**Example**
```Javascript
//Wireframe 모드 활성화 / 비활성화
vizcore.View.EnableWireframe(true);
```
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## FitAll
<procedure title="현재 모델을 화면에 맞춤" collapsible="true">
<note>FitAll()</note>

**Example**
```Javascript
//현재 모델을 화면에 맞춤
vizcore.View.FitAll();
```
</procedure>

## FocusByBoundBox
<procedure title="바운드 박스로 포커스" collapsible="true">
<note>FocusByBoundBox(boundBox, margin)</note>

**Example**
```Javascript
//모델 전체 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBox();
//바운드 박스로 포커스
vizcore.View.FocusByBoundBox(bbox,50);
```
**Parameters**

| Name     | Type      | Description         |
|----------|-----------|---------------------|
| boundBox | Data.BBox | Bound Box           |
| margin   | Number    | screen margin ratio |
</procedure>

## FocusObjectByNodeID
<procedure title="해당 Node IDs 의 노드 포커스" collapsible="true">
<note>FocusObjectByNodeID(nodeIds, offset, margin)</note>

**Example**
```Javascript
// 선택 개체 ID
let selNode = vizcore.Object3D.GetSelectedObject3D();
// 포커스
vizcore.View.FocusObjectByNodeID(selNode);
```
**Parameters**

| Name    | Type   | Description         |
|---------|--------|---------------------|
| nodeIds | Array  | Node IDs            |
| offset  | Number | Offset              |
| margin  | Number | screen margin ratio |
</procedure>

## FocusPivot
<procedure title="피벗 위치로 화면 중심이동" collapsible="true">
<note>FocusPivot(world)</note>

**Example**
```Javascript
// 피벗 위치로 화면 중심이동
let world = new VIZCore.Vector3(0,0,0);
vizcore.View.FocusPivot(world);
```
**Parameters**

| Name  | Type            | Description                               |
|-------|-----------------|-------------------------------------------|
| world | VIZCore.Vector3 | Pivot 위치 갱신 (undefined === 현재 pivot으로 이동) |
</procedure>

## GetBackupCameraData
<procedure title="카메라 복원 데이터 반환" collapsible="true">
<note>GetBackupCameraData(id) → {BackupCameraData}</note>

**Example**
```Javascript
//카메라 백업
let camera = vizcore.View.BackupCamera();
//카메라 복원 목록 반환
vizcore.View.GetBackupCameraList(camera);
```

**Parameters**

| Name | Type        | Description |
|------|-------------|-------------|
| id   | Data.UUIDv4 | 백업 아이디      |

**Returns**

| Type             | Description |
|------------------|-------------|
| BackupCameraData | 백업된 데이터 반환  |

</procedure>

## GetBackupCameraList
<procedure title="카메라 복원 목록 반환" collapsible="true">
<note>GetBackupCameraList() → {Array}</note>

**Example**
```Javascript
//카메라 복원 목록 반환
vizcore.View.GetBackupCameraList();      
```
**Returns**

| Type  | Description                   |
|-------|-------------------------------|
| Array | 백업된 데이터 반환 : BackupCameraData |
</procedure>

## GetCameraData
<procedure title="현재 카메라 정보 반환" collapsible="true">
<note>GetCameraData() → {Object}</note>

**Example**
```Javascript
//현재 카메라 정보 반환
vizcore.View.GetCameraData();      
```
**Returns**

| Type   | Description |
|--------|-------------|
| Object | CameraData  |
</procedure>
 
## GetCurrentImage
<procedure title="현재 화면의 이미지 데이터 반환" collapsible="true">
<note>GetCurrentImage(bIncludeReview) → {String}</note>

**Example**
```Javascript
let img = new Image();
let bIncludeReview = true; // 리뷰 정보 이미지에 포함
img.src = vizcore.View.GetCurrentImage(bIncludeReview);   // 현재 화면의 이미지 데이터 반환
img.style.objectfit = "contain";                            //object-fit: contain
var w = window.open('', '');                                //new window
w.document.title = "Snapshot";                              //window title
w.document.body.appendChild(img);                           //img
```
**Parameters**

| Name           | Type    | Description                      |
|----------------|---------|----------------------------------|
| bIncludeReview | boolean | 리뷰 정보 포함 여부(측정, 노트, 그리기, 그리드 정보) |

**Returns**

| Type   | Description      |
|--------|------------------|
| String | 이미지 데이터 (base64) |

</procedure>

## GetDirectionalLight
<procedure title="Directional Light 정보 반환" collapsible="true">
<note>GetDirectionalLight() → {view.Data.LightItem}</note>

**Example**
```Javascript
//Directional Light 정보 반환
let lightInfo = vizcore.View.GetDirectionalLight();
lightInfo.Color.set(255, 0, 0, 255); //빛 색상 변경
lightInfo.Power = 2;     //빛 세기 설정
```
**Returns**

| Type                | Description |
|---------------------|-------------|
| view.Data.LightItem | 빛 정보 반환     |
</procedure>
 
## GetLightDirection
<procedure title="빛 방향 반환" collapsible="true">
<note>GetLightDirection() → {VIZCore.Vector3}</note>

**Example**
```Javascript
//빛 방향 반환
vizcore.View.GetLightDirection();
```
**Returns**

| Type            | Description |
|-----------------|-------------|
| VIZCore.Vector3 | 빛 방향        |
</procedure>
 
## GetLockCameraUpAngle
<procedure title="Z축 고정 시 모델의 바닥면으로 회전되는 것을 방지 설정반환" collapsible="true">
<note>GetLockCameraUpAngle() → {Boolean}</note>

**Example**
```Javascript
//Z축 고정 시 모델의 바닥면으로 회전되는 것을 방지 설정반환
vizcore.View.GetLockCameraUpAngle();
```
**Returns**

| Type    | Description                          |
|---------|--------------------------------------|
| Boolean | True(바닥면으로 카메라 회전 차단), False(360 회전) |

</procedure>
 
## GetPivotLock
<procedure title="회전 중심(Pivot) 위치설정 잠금여부 반환" collapsible="true">
<note>GetPivotLock() → {Boolean}</note>

**Example**
```Javascript
//회전 중심(Pivot) 위치설정 잠금여부 반환
vizcore.View.GetPivotLock();
```

**Returns**

| Type    | Description |
|---------|-------------|
| Boolean | True, False |
</procedure>

## GetScreen1PixelLength
<procedure title="화면 기준 1Pixel당 거리 반환" collapsible="true">
<note>GetScreen1PixelLength(pos) → {Number}</note>

**Example**
```Javascript
//화면 기준 1Pixel당 거리 반환
let pos = new VIZCore.Vector3(0,0,0);
vizcore.View.GetScreen1PixelLength(pos);
```
**Parameters**

| Name | Type            | Description |
|------|-----------------|-------------|
| pos  | VIZCore.Vector3 | 기준 좌표       |

**Returns**

| Type   | Description |
|--------|-------------|
| Number | 1Pixel당 거리  |
</procedure>

## GetViewUnderControlMode
<procedure title="View Control 중 형상 가시화 모드 설정 반환" collapsible="true">
<note>GetViewUnderControlMode() → {VIZCore.Enum.ViewUnderControlVisibleMode}</note>

**Example**
```Javascript
//View Control 중 형상 가시화 모드 설정 반환
let item = vizcore.View.GetViewUnderControlMode();
```
**Returns**

| Type                                     | Description |
|------------------------------------------|-------------|
| VIZCore.Enum.ViewUnderControlVisibleMode | 설정 반환       |

</procedure>

## IsAnimation
<procedure title="카메라 애니메이션 설정 반환" collapsible="true">
<note>IsAnimation() → {Boolean}</note>

**Example**
```Javascript
//카메라 애니메이션 설정 반환
vizcore.View.IsAnimation();
```
**Returns**

| Type    | Description              |
|---------|--------------------------|
| Boolean | true : 활성화, false : 비활성화 |
</procedure>
 
## IsEdgeVisible
<procedure title="모델 모서리 표시 상태 반환" collapsible="true">
<note>IsEdgeVisible() → {boolean}</note>

**Example**
```Javascript
//모델 모서리 표시 상태 반환
if(vizcore.View.IsEdgeVisible() === true)
//모델 모서리 표시
vizcore.View.ShowEdge(false);
```
**Returns**

| Type    | Description                   |
|---------|-------------------------------|
| boolean | 상태 : True(show) / False(hide) |

</procedure>
 
## IsEnableViewLightRotate
<procedure title="카메라 방향에 따른 빛 방향 업데이트 반환" collapsible="true">
<note>IsEnableViewLightRotate() → {Boolean}</note>

**Example**
```Javascript
//카메라 방향에 따른 빛 방향 업데이트 반환
vizcore.View.IsEnableViewLightRotate();
```
**Returns**

| Type    | Description                   |
|---------|-------------------------------|
| Boolean | true : 빛 방향 갱신, false : 방향 고정 |
</procedure>

## LockCamera
<procedure title="카메라 제어" collapsible="true">
<note>LockCamera(enable)</note>

**Example**
```Javascript
//카메라 제어
vizcore.View.LockCamera(true);
```
**Parameters**

| Name   | Type    | Description               |
|--------|---------|---------------------------|
| enable | Boolean | True(Lock), False(Unlock) |
</procedure>

## LockPivot
<procedure title="회전 중심(Pivot) 위치설정 잠금" collapsible="true">
<note>LockPivot()</note>

**Example**
```Javascript
//회전 중심(Pivot) 위치설정 잠금
vizcore.View.LockPivot();
```
</procedure>

## LockZAxis
<procedure title="Z축을 기준으로 회전" collapsible="true">
<note>LockZAxis(enable)</note>

**Example**
```Javascript
//Z축을 기준으로 회전
vizcore.View.LockZAxis(true);
```
**Parameters**

| Name   | Type    | Description                      |
|--------|---------|----------------------------------|
| enable | Boolean | True(Z축을 기준으로 회전), False(360 회전) |
</procedure>

## MoveCamera
<procedure title="카메라 이동" collapsible="true">
<note>MoveCamera(camera)</note>

**Example**
```Javascript
//카메라 이동
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.ISO_PLUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.ISO_MINUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.X_PLUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.X_MINUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.Y_PLUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.Y_MINUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.Z_PLUS);
vizcore.View.MoveCamera(VIZCore.Enum.CameraDirection.Z_MINUS);
```
**Parameters**

| Name   | Type                         | Description |
|--------|------------------------------|-------------|
| camera | VIZCore.Enum.CameraDirection | 카메라 방향      |
</procedure>

## Refresh
<procedure title="현재 화면을 갱신" collapsible="true">
<note>Refresh()</note>

**Example**
```Javascript
//현재 화면을 갱신
vizcore.View.Refresh();
```
</procedure>

## ResetGLWindow
<procedure title="초기 GL Windows View 설정" collapsible="true">
<note>ResetGLWindow()</note>

**Example**
```Javascript
//초기 GL Windows View 설정
vizcore.View.ResetGLWindow();
```
</procedure>

## ResetView
<procedure title="초기 화면으로 초기화" collapsible="true">
<note>ResetView()</note>

**Example**
```Javascript
//초기 화면으로 초기화
vizcore.View.ResetView();
```
</procedure>

## Resize
<procedure title="Window 의 크기를 변경된 조건에 맞게 조정" collapsible="true">
<note>Resize()</note>

**Example**
```Javascript
//Window 의 크기를 변경된 조건에 맞게 조정
vizcore.View.Resize();
```
</procedure>
 
## RollbackCamera
<procedure title="카메라 복원" collapsible="true">
<note>RollbackCamera(id)</note>

**Example**
```Javascript
//카메라 백업
let camera = vizcore.View.BackupCamera();
//카메라 복원 목록 반환
vizcore.View.RollbackCamera(camera);
```

**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | string | 백업 아이디      |
</procedure>

## RotateCamera
<procedure title="Camera 회전" collapsible="true">
<note>RotateCamera(x, y, z, angleFormat)</note>

**Example**
```Javascript
let rotateAngleX = 45.0;                                            //x
//Camera 회전
vizcore.View.RotateCamera(rotateAngleX, 0, 0);
vizcore.View.RotateCamera(rotateAngleX, 0, 0, VIZCore.Enum.AngleFormat.DEGREE);
```
**Parameters**

| Name        | Type                     | Description                               |
|-------------|--------------------------|-------------------------------------------|
| x           | Number                   | 회전 X                                      |
| y           | Number                   | 회전 Y                                      |
| z           | Number                   | 회전 Z                                      |
| angleFormat | VIZCore.Enum.AngleFormat | DEFAULT : VIZCore.Enum.AngleFormat.DEGREE |
</procedure>

## RotateCameraByMatrix
<procedure title="Camera 회전" collapsible="true">
<note>RotateCameraByMatrix(matrix)</note>

**Example**
```Javascript
let matrix = new VIZCore.Matrix4();
matrix.translate(10,20,20) 
//Camera 회전
vizcore.View.RotateCameraByMatrix(matrix);
```
**Parameters**

| Name   | Type            | Description |
|--------|-----------------|-------------|
| matrix | VIZCore.Matrix4 | 회전 Matrix   |
</procedure>

## RotateCameraByVector
<procedure title="Camera 회전" collapsible="true">
<note>RotateCameraByVector(vector, angleFormat)</note>

**Example**
```Javascript
let vector = new VIZCore.Vector3(45,90,0)
//Camera 회전
vizcore.View.RotateCameraByVector(vector, VIZCore.Enum.AngleFormat.DEGREE);
```
**Parameters**

| Name        | Type                     | Description                               |
|-------------|--------------------------|-------------------------------------------|
| vector      | VIZCore.Vector3          | 회전 angle x, y, z                          |
| angleFormat | VIZCore.Enum.AngleFormat | DEFAULT : VIZCore.Enum.AngleFormat.DEGREE |
</procedure>

## ScreenToWorld
<procedure title="2D 좌표(화면 좌표)계를 3D World 좌표계로 반환" collapsible="true">
<note>ScreenToWorld(x, y, z)</note>

**Example**
```Javascript
//2D 좌표(화면 좌표)계를 3D World 좌표계로 반환
vizcore.View.ScreenToWorld(0, 0, 0);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| x    | Number | X 좌표        |
| y    | Number | Y 좌표        |
| z    | Number | Z 좌표        |
</procedure>

## ScreenToWorldByVector3
<procedure title="2D 좌표(화면 좌표)계를 3D World 좌표계로 반환" collapsible="true">
<note>ScreenToWorldByVector3(screen)</note>

**Example**
```Javascript
//2D 좌표(화면 좌표)계를 3D World 좌표계로 반환
let screen = new VIZCore.Vector3(0,0,0);
vizcore.View.ScreenToWorldByVector3(screen);
```
**Parameters**

| Name   | Type             | Description |
|--------|------------------|-------------|
| screen | 	VIZCore.Vector3 | Screen 좌표   |
</procedure>

## SetAmbientColor
<procedure title="Ambient 설정" collapsible="true">
<note>SetAmbientColor(color)</note>

**Example**
```Javascript
//Ambient 설정
vizcore.View.SetAmbientColor(
new VIZCore.Color(180, 90, 255, 255)        //(R, G, B, A)
);
```
**Parameters**

| Name  | Type            | Description |
|-------|-----------------|-------------|
| color | 		VIZCore.Color | Ambient 색상  |
</procedure>

## SetBackgroundColor
<procedure title="배경 색상 설정" collapsible="true">
<note>SetBackgroundColor(color1, color2)</note>

**Example**
```Javascript
//배경 색상 설정
vizcore.View.SetBackgroundColor(
new VIZCore.Color(255, 255, 255, 255)
, new VIZCore.Color(180, 180, 180, 255)
);
```
**Parameters**

| Name   | Type            | Description |
|--------|-----------------|-------------|
| color1 | 		VIZCore.Color | Color #1    |
| color2 | 		VIZCore.Color | Color #2    |
</procedure>

## SetBackgroundMode
<procedure title="배경 색상 표현 설정" collapsible="true">
<note>SetBackgroundMode(mode)</note>

**Example**
```Javascript
//배경 색상 표현 설정
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_ONE);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_HOR);
vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_HOR_REVERSE);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_VER);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_VER_REVERSE);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CHOR);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CHOR_REVERSE);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CVER);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CVER_REVERSE);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CENTER);
//vizcore.View.SetBackgroundMode(VIZCore.Enum.BackgroundModes.COLOR_TWO_CORNER);
////배경 색상 설정
vizcore.View.SetBackgroundColor(
new VIZCore.Color(255, 255, 255, 255)
, new VIZCore.Color(180, 180, 180, 255)
);
//3D 화면 모델 Render
vizcore.Render();
```
**Parameters**

| Name | Type                         | Description |
|------|------------------------------|-------------|
| mode | VIZCore.Enum.BackgroundModes | 배경 색상표현 설정  |
</procedure>

## SetCameraBaseDirection
<procedure title="초기 모델 조회 시, 초기 카메라 방향 설정" collapsible="true">
<note>SetCameraBaseDirection(direction)</note>

**Example**
```Javascript
//초기 모델 조회 시, 초기 카메라 방향 설정
vizcore.View.SetCameraBaseDirection(VIZCore.Enum.VIEW_MODES.PlusZ);
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw");
```
**Parameters**

| Name      | Type                    | Description |
|-----------|-------------------------|-------------|
| direction | VIZCore.Enum.VIEW_MODES | 카메라 방향      |
</procedure>

## SetCameraBaseDirectionMatrix
<procedure title="초기 모델 조회 시, 초기 카메라 방향 설정" collapsible="true">
<note>SetCameraBaseDirectionMatrix(matrix)</note>

**Example**
```Javascript
//초기 모델 조회 시, 초기 카메라 방향 설정
let baseMatrix = new VIZCore.Matrix4();
vizcore.View.SetCameraBaseDirectionMatrix(baseMatrix);
```
**Parameters**

| Name   | Type            | Description     |
|--------|-----------------|-----------------|
| matrix | VIZCore.Matrix4 | 초기 방향 matrix 설정 |
</procedure>

## SetCameraBaseMatrix
<procedure title="초기 모델 조회 시, 초기 카메라 설정" collapsible="true">
<note>SetCameraBaseMatrix(matrix)</note>

**Example**
```Javascript
//초기 모델 조회 시, 초기 카메라 설정
let baseMatrix = new VIZCore.Matrix4();
vizcore.View.SetCameraBaseMatrix(baseMatrix);
```
**Parameters**

| Name   | Type            | Description  |
|--------|-----------------|--------------|
| matrix | VIZCore.Matrix4 | 초기 matrix 설정 |
</procedure>

## SetCameraData
<procedure title="현재 카메라 정보 설정" collapsible="true">
<note>SetCameraData(cameraData)</note>

**Example**
```Javascript
//현재 카메라 정보 반환
let camera = vizcore.View.GetCameraData();
//현재 카메라 정보 설정
vizcore.View.SetCameraData(camera);
```
**Parameters**

| Name | Type        | Description |
|------|-------------|-------------|
| id   | Data.UUIDv4 | 백업 아이디      |
</procedure>

## SetCameraDataByMatrix
<procedure title="피벗 위치로 화면 중심이동" collapsible="true">
<note>SetCameraDataByMatrix(matrix, zoom)</note>

**Example**
```Javascript
// VIZCore3D.NET
// float[] matrix = camera.Matrix;  * // VIZCore3D.NET.Data.CameraData camera = vizcore3d.View.GetCameraData();
// float zoom = camera.Zoom

let matrix = [0.281377,0.488073,-0.826203,0,-0.959597,0.143115,-0.242262,0,0,0.860989,0.508623,0,-2949.6,-29019.27,19458.8,1];
let zoom = 1.161692;

vizcore.View.SetCameraDataByMatrix(matrix, zoom);
```
**Parameters**

| Name   | Type            | Description      |
|--------|-----------------|------------------|
| matrix | `Array<Number>` | 카메라 매트릭스(Matrix) |
| zoom   | Number          | 카메라 Zoom         |
</procedure>

## SetEdgeColor
<procedure title="모서리 강조 색상 설정" collapsible="true">
<note>SetEdgeColor(color)</note>

**Example**
```Javascript
//모델 모서리 표시
vizcore.View.ShowEdge(true);
//모서리 강조 색상 설정
vizcore.View.SetEdgeColor(new VIZCore.Color(255, 0, 0, 255));
```
**Parameters**

| Name  | Type          | Description          |
|-------|---------------|----------------------|
| color | VIZCore.Color | Edge Highlight Color |
</procedure>

## SetEnableViewLightRotate
<procedure title="카메라 방향에 따른 빛 방향 업데이트" collapsible="true">
<note>SetEnableViewLightRotate(enable)</note>

**Example**
```Javascript
//카메라 방향에 따른 빛 방향 업데이트
vizcore.View.SetEnableViewLightRotate(true);
```
**Parameters**

| Name   | Type    | Description                   |
|--------|---------|-------------------------------|
| enable | Boolean | true : 빛 방향 갱신, false : 방향 고정 |
</procedure>

## SetLightColor
<procedure title="빛 색상 설정" collapsible="true">
<note>SetLightColor(color)</note>

**Example**
```Javascript
//빛 색상 설정
vizcore.View.SetLightColor(new VIZCore.Color(123,21,34,255));
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| color | VIZCore.Color | 빛 색상        |
</procedure>

## SetLightDirection
<procedure title="빛 방향 설정" collapsible="true">
<note>SetLightDirection(direction)</note>

**Example**
```Javascript
//빛 방향 설정
vizcore.View.SetLightDirection(new VIZCore.Vector3(123,21,34));
```
**Parameters**

| Name      | Type            | Description |
|-----------|-----------------|-------------|
| direction | VIZCore.Vector3 | 빛 방향        |
</procedure>

## SetLightTime
<procedure title="지정된 시간의 빛 방향 설정" collapsible="true">
<note>SetLightTime(time)</note>

**Example**
```Javascript
//지정된 시간의 빛 방향 설정
vizcore.View.SetLightTime(10);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| time | Number | 시간 (6 ~ 18) |
</procedure>

## SetLockCameraUpAngle
<procedure title="Z축 고정 시 모델의 바닥면으로 회전되는 것을 방지" collapsible="true">
<note>SetLockCameraUpAngle(enable)</note>

**Example**
```Javascript
//Z축 고정 시 모델의 바닥면으로 회전되는 것을 방지
vizcore.View.SetLockCameraUpAngle(true);
vizcore.View.SetLockCameraUpAngle(false);
```
**Parameters**

| Name   | Type    | Description                          |
|--------|---------|--------------------------------------|
| enable | Boolean | True(바닥면으로 카메라 회전 차단), False(360 회전) |
</procedure>

## SetLockCameraUpAngleMinMax
<procedure title="Z축 고정된 카메라를 회전할수 있는 각도 설정" collapsible="true">
<note>SetLockCameraUpAngleMinMax(min, max)</note>

**Example**
```Javascript
//Z축 고정된 카메라를 회전할수 있는 각도 설정
vizcore.View.SetLockCameraUpAngleMinMax(0,0);
```
**Parameters**

| Name | Type   | Description     |
|------|--------|-----------------|
| min  | Number | 최소 각 (-90 ~ 90) |
| max  | Number | 최대 각 (-90 ~ 90) |
</procedure>

## SetModelObjectCustomEdgeColor
<procedure title="지정한 개체의 모델 모서리 추가 표시 색상 설정" collapsible="true">
<note>SetModelObjectCustomEdgeColor(color)</note>

**Example**
```Javascript
let ids = [9, 13];                                //Array<Number>
//지정한 개체의 모델 모서리 설정
vizcore.Object3D.CustomEdge.SetEdge(ids, true);
//지정한 개체의 모델 모서리 추가 표시
vizcore.View.ShowModelObjectCustomEdge(true);
let color = new VIZCore.Color(255,255,255,255);                 //R, G, B, A
//지정한 개체의 모델 모서리 추가 표시 색상 설정
vizcore.View.SetModelObjectCustomEdgeColor(color);
```
**Parameters**

| Name  | Type          | Description  |
|-------|---------------|--------------|
| color | VIZCore.Color | 모서리 추가 표시 색상 |
</procedure>

## SetPivot
<procedure title="피봇(회전 중심) 설정" collapsible="true">
<note>SetPivot(point)</note>

**Example**
```Javascript
let point = new VIZCore.Vector3(0, 0, 0);
//피봇(회전 중심) 설정
vizcore.View.SetPivot(point);
```
**Parameters**

| Name  | Type            | Description |
|-------|-----------------|-------------|
| point | VIZCore.Vector3 | 위치          |
</procedure>

## SetPivotPosition
<procedure title="회전 중심(Pivot) 위치 설정" collapsible="true">
<note>SetPivotPosition(position)</note>

**Example**
```Javascript
function example1() {
    //Pivot 위치 설정
    vizcore.View.SetPivotPosition(new VIZCore.Vector3(100, 0, 0));
}

function example2() {
    //위치 설정 잠금해제
    vizcore.View.UnlockPivot();
    //Pivot 위치 설정
    vizcore.View.SetPivotPosition(new VIZCore.Vector3(100, 0, 0));
    //위치 설정 잠금
    vizcore.View.LockPivot();
}
```
**Parameters**

| Name     | Type            | Description |
|----------|-----------------|-------------|
| position | VIZCore.Vector3 | Pivot 위치    |
</procedure>

## SetPivotVisible
<procedure title="회전 중심(Pivot) 가시화 여부" collapsible="true">
<note>SetPivotVisible(visible)</note>

**Example**
```Javascript
vizcore.View.SetPivotVisible(true);  // Show
vizcore.View.SetPivotVisible(false); // Hide
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | boolean | 가시화 여부      |
</procedure>

## SetProjection
<procedure title="Projection (원근, 평행) 모드 설정" collapsible="true">
<note>SetProjection(projection)</note>

**Example**
```Javascript
vizcore.View.SetProjection(VIZCore.Enum.PROJECTION_MODES.Orthographic); // 평행
vizcore.View.SetProjection(VIZCore.Enum.PROJECTION_MODES.Perspective);  // 원근
```
**Parameters**

| Name       | Type                          | Description |
|------------|-------------------------------|-------------|
| projection | VIZCore.Enum.PROJECTION_MODES | 원근/평행 모드    |
</procedure>

## SetRenderMode
<procedure title="Render Mode 설정" collapsible="true">
<note>SetRenderMode(mode)</note>

**Example**
```Javascript
//Render Mode 설정
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.Smooth);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.Xray);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.Plastic);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.HiddenLine);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.HiddenLineDashed);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.WireFrame);
vizcore.View.SetRenderMode(VIZCore.Enum.RENDER_MODES.GrayScale);
```
**Parameters**

| Name | Type                      | Description    |
|------|---------------------------|----------------|
| mode | VIZCore.Enum.RENDER_MODES | Render Mode 설정 |
</procedure>

## SetSelectionColor
<procedure title="선택 객체 색상 설정" collapsible="true">
<note>SetSelectionColor(color)</note>

**Example**
```Javascript
//선택 객체 색상 설정
vizcore.View.SetSelectionColor(new VIZCore.Color(255,255,0,255));
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| color | VIZCore.Color | 선택 객체 색상    |
</procedure>

## SetSelectionLevel
<procedure title="선택 가능 개체 타입이 LEVEL일 경우, 선택되어야 하는 LEVEL 설정" collapsible="true">
<note>SetSelectionLevel(level)</note>

**Example**
```Javascript
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw");
//선택 가능 개체 타입 설정
vizcore.View.SetSelectionUnit(VIZCore.Enum.SELECT_UNIT.Level);
vizcore.View.SetSelectionLevel(5); // 선택된 개체의 상위 5 Level 개체를 선택상태로 변경
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| level | Number | 개체 레벨       |
</procedure>

## SetSelectionLineColor
<procedure title="선택 객체 선 색상 설정" collapsible="true">
<note>SetSelectionLineColor(color)</note>

**Example**
```Javascript
//선택 객체 선 색상 설정
vizcore.View.SetSelectionLineColor(new VIZCore.Color(255,255,0,255));
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| color | VIZCore.Color | 선택 객체 선 색상  |
</procedure>

## SetSelectionObject3DType
<procedure title="선택 가능 개체 유형 설정" collapsible="true">
<note>SetSelectionObject3DType(selectionObject3DTypes)</note>

**Example**
```Javascript
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw");
//선택 가능 개체 유형 설정
vizcore.View.SetSelectionObject3DType(VIZCore.Enum.SelectionObject3DTypes.ALL);                // 전체 개체 선택
vizcore.View.SetSelectionObject3DType(VIZCore.Enum.SelectionObject3DTypes.OPAQUE_OBJECT3D);    // 불투명한 개체만 선택
vizcore.View.SetSelectionObject3DType(VIZCore.Enum.SelectionObject3DTypes.NONE);    // 선택 안함
vizcore.View.SetSelectionObject3DType(VIZCore.Enum.SelectionObject3DTypes.CUSTOMCOLOR_OBJECT3D);    // 색상 변경된 개체만 선택
//3D 화면 모델 Render
vizcore.Render();
```
**Parameters**

| Name                   | Type                                | Description |
|------------------------|-------------------------------------|-------------|
| selectionObject3DTypes | VIZCore.Enum.SelectionObject3DTypes | 개체 유형       |
</procedure>

## SetSelectionUnit
<procedure title="선택 가능 개체 타입 설정" collapsible="true">
<note>SetSelectionUnit(unit)</note>

**Example**
```Javascript
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw");
//선택 가능 개체 타입 설정
vizcore.View.SetSelectionUnit(VIZCore.Enum.SELECT_UNIT.Assembly);
vizcore.View.SetSelectionUnit(VIZCore.Enum.SELECT_UNIT.Part);
vizcore.View.SetSelectionUnit(VIZCore.Enum.SELECT_UNIT.Level);
```
**Parameters**

| Name | Type                     | Description |
|------|--------------------------|-------------|
| unit | VIZCore.Enum.SELECT_UNIT | 개체 유형       |
</procedure>

## SetShadowRatio
<procedure title="그림자 효과 비율 설정 (0 ~ 1)" collapsible="true">
<note>SetShadowRatio(ratio)</note>

**Example**
```Javascript
//그림자 효과 활성화 / 비활성화
vizcore.View.EnableShadow(true);
//그림자 효과 비율 설정 (0 ~ 1)
vizcore.View.SetShadowRatio(0.3);
```
**Parameters**

| Name  | Type   | Description                     |
|-------|--------|---------------------------------|
| ratio | Number | 0 : 그림자 표시하지 않음, 1 : 그림자 어둡게 적용 |
</procedure>

## SetViewUnderControlMode
<procedure title="View Control 중 형상 가시화 모드 설정" collapsible="true">
<note>SetViewUnderControlMode(mode)</note>

**Example**
```Javascript
//View Control 중 형상 가시화 모드 설정
vizcore.View.SetViewUnderControlMode(VIZCore.Enum.ViewUnderControlVisibleMode.SHADED);
vizcore.View.SetViewUnderControlMode(VIZCore.Enum.ViewUnderControlVisibleMode.BOUNDBOX);
```
**Parameters**

| Name | Type                                     | Description  |
|------|------------------------------------------|--------------|
| mode | VIZCore.Enum.ViewUnderControlVisibleMode | 형상 가시화 모드 설정 |
</procedure>

## SetZAxis2Up
<procedure title="Axis Z Up" collapsible="true">
<note>SetZAxis2Up()</note>

**Example**
```Javascript
vizcore.View.SetZAxis2Up();
```
</procedure>

## ShowEdge
<procedure title="모델 모서리 표시" collapsible="true">
<note>ShowEdge(visible)</note>

**Example**
```Javascript
vizcore.View.ShowEdge(true);  // Show
vizcore.View.ShowEdge(false); // Hide
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | boolean | 모델 모서리 표시   |
</procedure>

## ShowModelObjectCustomEdge
<procedure title="지정한 개체의 모델 모서리 추가 표시" collapsible="true">
<note>ShowModelObjectCustomEdge(visible)</note>

**Example**
```Javascript
vizcore.View.ShowModelObjectCustomEdge(true);  // Show
vizcore.View.ShowModelObjectCustomEdge(false); // Hide

function funExample() {
    let ids = [10 , 20];
    //지정한 개체의 모델 모서리 설정
    vizcore.Object3D.CustomEdge.SetEdge(ids, true);
    //지정한 개체의 모델 모서리 추가 표시
    vizcore.View.ShowModelObjectCustomEdge(true); 
}
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | boolean | 모델 모서리 표시   |
</procedure>

## TranslateCameraByMatrix
<procedure title="Camera 이동" collapsible="true">
<note>TranslateCameraByMatrix(matrix)</note>

**Example**
```Javascript
let matrix = new VIZCore.Matrix4();
matrix.translate(10,20,20)
//Camera 이동
vizwide3d.View.TranslateCameraByMatrix(matrix);
```

**Parameters**

| Name   | Type            | Description |
|--------|-----------------|-------------|
| matrix | VIZCore.Matrix4 | 이동 Matrix   |
</procedure>

## TranslateCameraByVector
<procedure title="Camera 이동" collapsible="true">
<note>TranslateCameraByVector(vector)</note>

**Example**
```Javascript
//Camera 이동
vizcore.View.TranslateCameraByVector(new VIZCore.Vector3(0,0,0));
```
**Parameters**

| Name   | Type            | Description |
|--------|-----------------|-------------|
| vector | VIZCore.Vector3 | 이동          |
</procedure>

## UnlockPivot
<procedure title="회전 중심(Pivot) 위치설정 잠금해제" collapsible="true">
<note>UnlockPivot()</note>

**Example**
```Javascript
//회전 중심(Pivot) 위치설정 잠금해제
vizcore.View.UnlockPivot();
```
</procedure>

## UpdateGLWindow
<procedure title="Update GL Window - matrix MV, matrix MVP Update" collapsible="true">
<note>UpdateGLWindow(matrix)</note>

**Example**
```Javascript
let matrix = new VIZCore.Matrix4();
//Update GL Window - matrix MV, matrix MVP Update
vizcore.View.UpdateGLWindow(matrix);
```
**Parameters**

| Name   | Type            | Description                        |
|--------|-----------------|------------------------------------|
| matrix | VIZCore.Matrix4 | Model Matrix == undefined 인 경우 초기값 |
</procedure>

## ViewBackBottomSide
<procedure title="Camera 설정 (+y -z)" collapsible="true">
<note>ViewBackBottomSide()</note>

**Example**
```Javascript
//Camera 설정 (+y -z)
vizcore.View.ViewBackBottomSide();
```
</procedure>

## ViewBackSection
<procedure title="Camera 설정 (+y)" collapsible="true">
<note>ViewBackSection()</note>

**Example**
```Javascript
//Camera 설정 (+y)
vizcore.View.ViewBackSection();
```
</procedure>

## ViewBackTopSide
<procedure title="Camera 설정 (+y +z)" collapsible="true">
<note>ViewBackTopSide()</note>

**Example**
```Javascript
//Camera 설정 (+y +z)
vizcore.View.ViewBackTopSide();
```
</procedure>

## ViewBottomPlan
<procedure title="Camera 설정 (-z)" collapsible="true">
<note>ViewBottomPlan()</note>

**Example**
```Javascript
//Camera 설정 (-z)
vizcore.View.ViewBottomPlan();
```
</procedure>

## ViewFrontBottomSide
<procedure title="Camera 설정 (-y -z)" collapsible="true"> 
<note>ViewFrontBottomSide()</note>

**Example**
```Javascript
//Camera 설정 (-y -z)
vizcore.View.ViewFrontBottomSide();
```
</procedure>

## ViewFrontSection
<procedure title="Camera 설정 (-y)" collapsible="true">
<note>ViewFrontSection()</note>

**Example**
```Javascript
//Camera 설정 (-y)
vizcore.View.ViewFrontSection();
```
</procedure>

## ViewFrontTopSide
<procedure title="Camera 설정 (-y +z)" collapsible="true">
<note>ViewFrontTopSide()</note>

**Example**
```Javascript
//Camera 설정 (-y +z)
vizcore.View.ViewFrontTopSide();
```
</procedure>

## ViewISOLeftBackBottom
<procedure title="Camera 설정 (-x +y -z)" collapsible="true">
<note>ViewISOLeftBackBottom()</note>

**Example**
```Javascript
//Camera 설정 (-x +y -z)
vizcore.View.ViewISOLeftBackBottom();
```
</procedure>

## ViewISOLeftBackTop
<procedure title="Camera 설정 (-x +y +z)" collapsible="true">
<note>ViewISOLeftBackTop()</note>

**Example**
```Javascript
//Camera 설정 (-x +y +z)
vizcore.View.ViewISOLeftBackTop();
```
</procedure>

## ViewISOLeftFrontBottom
<procedure title="Camera 설정 (-x -y -z)" collapsible="true">
<note>ViewISOLeftFrontBottom()</note>

**Example**
```Javascript
//Camera 설정 (-x -y -z)
vizcore.View.ViewISOLeftFrontBottom();
```
</procedure>

## ViewISOLeftFrontTop
<procedure title="Camera 설정 (-x -y +z)" collapsible="true">
<note>ViewISOLeftFrontTop()</note>

**Example**
```Javascript
//Camera 설정 (-x -y +z)
vizcore.View.ViewISOLeftFrontTop();
```
</procedure>

## ViewISOMinus
<procedure title="Camera 설정 (ISO-)" collapsible="true">
<note>ViewISOMinus()</note>

**Example**
```Javascript
//Camera 설정 (ISO-)
vizcore.View.ViewISOMinus();
```
</procedure>

## ViewISOPlus
<procedure title="Camera 설정 (ISO+)" collapsible="true">
<note>ViewISOPlus()</note>

**Example**
```Javascript
//Camera 설정 (ISO+)
vizcore.View.ViewISOPlus();
```
</procedure>

## ViewISORightBackBottom
<procedure title="Camera 설정 (+x +y -z)" collapsible="true">
<note>ViewISORightBackBottom()</note>

**Example**
```Javascript
//Camera 설정 (+x +y -z)
vizcore.View.ViewISORightBackBottom();
```
</procedure>

## ViewISORightBackTop
<procedure title="Camera 설정 (+x +y +z)" collapsible="true">
<note>ViewISORightBackTop()</note>

**Example**
```Javascript
//Camera 설정 (+x +y +z)
vizcore.View.ViewISORightBackTop();
```
</procedure>

## ViewISORightFrontBottom
<procedure title="Camera 설정 (+x -y -z)" collapsible="true">
<note>ViewISORightFrontBottom()</note>

**Example**
```Javascript
//Camera 설정 (+x -y -z)
vizcore.View.ViewISORightFrontBottom();
```
</procedure>

## ViewISORightFrontTop
<procedure title="Camera 설정 (+x -y +z)" collapsible="true">
<note>ViewISORightFrontTop()</note>

**Example**
```Javascript
//Camera 설정 (+x -y +z)
vizcore.View.ViewISORightFrontTop();
```
</procedure>

## ViewLeftBackSide
<procedure title="Camera 설정 (-x +y)" collapsible="true">
<note>ViewLeftBackSide()</note>

**Example**
```Javascript
Camera 설정 (-x +y)
vizcore.View.ViewLeftBackSide();
```
</procedure>

## ViewLeftBottomSide
<procedure title="Camera 설정 (-x -z)" collapsible="true">
<note>ViewLeftBottomSide()</note>

**Example**
```Javascript
//Camera 설정 (-x -z)
vizcore.View.ViewLeftBottomSide();
```
</procedure>

## ViewLeftElevation
<procedure title="Camera 설정 (-x)" collapsible="true">
<note>ViewLeftElevation()</note>

**Example**
```Javascript
//Camera 설정 (-x)
vizcore.View.ViewLeftElevation();
```
</procedure>

## ViewLeftFrontSide
<procedure title="Camera 설정 (-x -y)" collapsible="true">
<note>ViewLeftFrontSide()</note>

**Example**
```Javascript
//Camera 설정 (-x -y)
vizcore.View.ViewLeftFrontSide();
```
</procedure>

## ViewLeftTopSide
<procedure title="Camera 설정 (-x +z)" collapsible="true">
<note>ViewLeftTopSide()</note>

**Example**
```Javascript
//Camera 설정 (-x +z)
vizcore.View.ViewLeftTopSide();
```
</procedure>

## ViewRightBackSide
<procedure title="Camera 설정 (+x +y))" collapsible="true">
<note>ViewRightBackSide()</note>

**Example**
```Javascript
//Camera 설정 (+x +y)
vizcore.View.ViewRightBackSide();
```
</procedure>

## ViewRightBottomSide
<procedure title="Camera 설정 (+x -z)" collapsible="true">
<note>ViewRightBottomSide()</note>

**Example**
```Javascript
//Camera 설정 (+x -z)
vizcore.View.ViewRightBottomSide();
```
</procedure>

## ViewRightElevation
<procedure title="Camera 설정 (+x)" collapsible="true">
<note>ViewRightElevation()</note>

**Example**
```Javascript
//Camera 설정 (+x)
vizcore.View.ViewRightElevation();
```
</procedure>

## ViewRightFrontSide
<procedure title="Camera 설정 (+x -y)" collapsible="true">
<note>ViewRightFrontSide()</note>

**Example**
```Javascript
//Camera 설정 (+x -y)
vizcore.View.ViewRightFrontSide();
```
</procedure>

## ViewRightTopSide
<procedure title="Camera 설정 (+x +z)" collapsible="true">
<note>ViewRightTopSide()</note>

**Example**
```Javascript
//Camera 설정 (+x +z)
vizcore.View.ViewRightTopSide();
```
</procedure>

## ViewTopPlan
<procedure title="Camera 설정 (+z)" collapsible="true">
<note>ViewTopPlan()</note>

**Example**
```Javascript
//Camera 설정 (+z)
vizcore.View.ViewTopPlan();
```
</procedure>

## WorldToScreen
<procedure title="3D World 좌표계를 2D 좌표(화면 좌표) 반환" collapsible="true">
<note>WorldToScreen(x, y, z)</note>

**Example**
```Javascript
//3D World 좌표계를 2D 좌표(화면 좌표) 반환
vizcore.View.WorldToScreen(2, 2, 2);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| x    | Number | x 좌표        |
| y    | Number | y 좌표        |
| z    | Number | z 좌표        |
</procedure>

## WorldToScreenByVector3
<procedure title="3D World 좌표계를 2D 좌표(화면 좌표) 반환" collapsible="true">
<note>WorldToScreenByVector3(world)</note>

**Example**
```Javascript
//3D World 좌표계를 2D 좌표(화면 좌표) 반환
vizcore.View.WorldToScreenByVector3(new VIZCore.Vector3(0.0, 0.0, 0.0);
```
**Parameters**

| Name  | Type             | Description |
|-------|------------------|-------------|
| world | 	VIZCore.Vector3 | World  좌표   |
</procedure>

## ZoomSelectedObject
<procedure title="선택 모델 박스 줌" collapsible="true">
<note>ZoomSelectedObject(offset, margin)</note>

**Example**
```Javascript
//선택 모델 박스 줌
vizcore.View.ZoomSelectedObject(0, 0.1);
```
**Parameters**

| Name   | Type   | Description         |
|--------|--------|---------------------|
| offset | Number | bbox offset         |
| margin | Number | screen margin ratio |
</procedure>

## --- Event Listener ---

## OnCameraStateChangedEvent
<procedure title="카메라 변경 이벤트 등록" collapsible="true">
<note>OnCameraStateChangedEvent(listener)</note>

**Example**
```Javascript
// [To Do] vizcore.Configuration.Event.EnableCameraChanged = true 일 때만 가능
vizcore.Configuration.Event.EnableCameraChanged = true;

// Event : OnCameraStateChangedEvent
let onCameraChangedEvent = function (event) {
    console.log(event)
}

// Add Event Handler : Camera Changed Event (카메라 변경 이벤트)
vizcore.View.OnCameraStateChangedEvent(onCameraChangedEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnEmptyMeshBlockEvent
<procedure title="Empty MeshBlock 이벤트 등록" collapsible="true">
<note>OnEmptyMeshBlockEvent(listener)</note>

**Example**
```Javascript
// Event : OnEmptyMeshBlockEvent
let onEmptyMeshBlockEvent = function (event) {
    console.log(event)
}

// Add Event Handler : Empty MeshBlock Event (빈 메시 블록 파일 이벤트)
vizcore.View.OnEmptyMeshBlockEvent(onEmptyMeshBlockEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnSelectedEvent
<procedure title="개체 선택 이벤트 등록" collapsible="true">
<note>OnSelectedEvent(listener)</note>

**Example**
```Javascript
// Event : OnSelectedEvent
let callback = function (param) {
    // 선택 개체 타입
    console.log("선택 개체 타입 :: ", param.data.type);
    // 선택 이벤트 원형 : Mouse, Touch
    console.log("선택 이벤트 :: ",param.data.event);
    // 선택 개체 정보
    console.log("선택 개체 정보 :: ",param.data.info);
}

// Add Event Handler : 관리 객체 선택 이벤트
vizcore.View.OnSelectedEvent(callback);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultContextMenuEvent
<procedure title="View Default ContextMenu Event" collapsible="true">
<note>OnViewDefaultContextMenuEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultContextMenuEvent
let OnViewDefaultContextMenu = function (event) {
    console.log(event);
}

// Add Event Handler : ContextMenu
vizcore.View.OnViewDefaultContextMenuEvent(OnViewDefaultContextMenu);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultKeyUpEvent
<procedure title="View Default KeyUp Event" collapsible="true">
<note>OnViewDefaultKeyUpEvent(listener)</note>

**Example**
```Javascript
// Event : onViewDefaultKeyUpEvent
let onViewDefaultKeyUpEvent = function (event) {
    console.log(event);
}

// Add Event Handler : KeyUp (키업 이벤트)
vizcore.View.OnViewDefaultKeyUpEvent(onViewDefaultKeyUpEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultMouseDoubleClickEvent
<procedure title="View Default Mouse DoubleClick Event" collapsible="true">
<note>OnViewDefaultMouseDoubleClickEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultMouseDoubleClickEvent
let OnViewDefaultMouseDoubleClick = function (event) {
    console.log(event);
}

// Add Event Handler : Mouse DoubleClick (마우스 더블클릭 이벤트)
vizcore.View.OnViewDefaultMouseDoubleClickEvent(OnViewDefaultMouseDoubleClick);

```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultMouseDownEvent
<procedure title="View Default Mouse Down Event" collapsible="true">
<note>OnViewDefaultMouseDownEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultMouseDownEvent
let OnViewDefaultMouseDown = function (event) {
    console.log(event);
}

// Add Event Handler : Mouse Down (마우스 다운 이벤트)
vizcore.View.OnViewDefaultMouseDownEvent(OnViewDefaultMouseDown);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultMouseMoveEvent
<procedure title="View Default Mouse Move Event" collapsible="true">
<note>OnViewDefaultMouseMoveEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultMouseMoveEvent
let OnViewDefaultMouseMove = function (event) {
    console.log(event);
}

// Add Event Handler : Mouse Up (마우스 이동 이벤트)
vizcore.View.OnViewDefaultMouseMoveEvent(OnViewDefaultMouseMove);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultMouseUpEvent
<procedure title="View Default Mouse Up Event" collapsible="true">
<note>OnViewDefaultMouseUpEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultMouseUpEvent
let OnViewDefaultMouseUp = function (event) {
    console.log(event);
}

// Add Event Handler : Mouse Up (마우스 업 이벤트)
vizcore.View.OnViewDefaultMouseUpEvent(OnViewDefaultMouseUp);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDefaultMouseWheelEvent
<procedure title="View Default Mouse Wheel Event" collapsible="true">
<note>OnViewDefaultMouseWheelEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDefaultMouseWheelEvent
let OnViewDefaultMouseWheel = function (event) {
    console.log(event);
}

// Add Event Handler : Mouse Wheel (마우스 휠 이벤트)
vizcore.View.OnViewDefaultMouseWheelEvent(OnViewDefaultMouseWheel);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnViewDrawInfoEvent
<procedure title="View DrawInfo Event" collapsible="true">
<note>OnViewDrawInfoEvent(listener)</note>

**Example**
```Javascript
// Event : OnViewDrawInfoEvent
let OnViewDrawInfo = function (event) {
    console.log(event);
}

// Add Event Handler : DrawInfo (그리기 상태에 대한 정보 반환)
vizcore.View.OnViewDrawInfoEvent(OnViewDrawInfo);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>