# Object3D

## DisableViewDistanceBox
<procedure title="설정 거리보다 먼 경우 박스 표시 해제" collapsible="true">
<note>DisableViewDistanceBox(fileKey)</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//설정 거리보다 먼 경우 박스 표시 해제
vizcore.Object3D.DisableViewDistanceBox("sample1");
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| fileKey | Object | 파일 ID       |
</procedure>

## FromFile
<procedure title="FileID에 해당하는 Node 정보 반환" collapsible="true">
<note>FromFile(fileId) → {Array}</note>

**Example**
```Javascript
//FileID에 해당하는 Node 정보 반환
let nodes = vizcore.Object3D.FromFile("FileKey");
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| fileId | Object | File ID     |

**Returns**

| Type  | Description     |
|-------|-----------------|
| Array | Node Data Array |
</procedure>

## FromFilter
<procedure title="Filter에 해당하는 Node 정보 반환" collapsible="true">
<note>

FromFilter(filter) → `{Array<Object>}`
</note>

**Example**
```Javascript
//Filter에 해당하는 Node 정보 반환
let item = vizcore.Object3D.FromFilter(VIZCore.Enum.OBJECT3D_FILTER.ALL);
```
**Parameters**

| Name   | Type                         | Description                     |
|--------|------------------------------|---------------------------------|
| filter | VIZCore.Enum.OBJECT3D_FILTER | `//* @returns {Array} nodes ID` |

**Returns**

| Type            | Description |
|-----------------|-------------|
| `Array<Object>` | nodes       |
</procedure>

## FromID
<procedure title="Node ID에 해당하는 정보 반환" collapsible="true">
<note>FromID(id) → {Array}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let nodeIds = [];                                       //Array<Number>
for (let i = 0; i < nodes.length; i++) {
    nodeIds.push(nodes[i].id);
}

//Node ID에 해당하는 정보 반환
let node = vizcore.Object3D.FromID(nodeIds);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | Number | Node ID     |

**Returns**

| Type  | Description     |
|-------|-----------------|
| Array | Node Data Array |
</procedure> 

## FromLevel
<procedure title="Level에 해당하는 Node 정보 반환" collapsible="true">
<note>FromLevel(level) → {Array}</note>

**Example**
```Javascript
//Level에 해당하는 Node 정보 반환
let nodes = vizcore.Object3D.FromLevel(2);
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| level | Number | Level       |

**Returns**

| Type  | Description     |
|-------|-----------------|
| Array | Node Data Array |

</procedure> 

## FromOrigin
<procedure title="FileID, OriginID에 해당하는 Node 정보 반환" collapsible="true">
<note>FromOrigin(fileId, originId) → {Array}</note>

**Example**
```Javascript
//FileID, OriginID에 해당하는 Node 정보 반환
let node = vizcore.Object3D.FromOrigin("FileKey", 1);
```
**Parameters**

| Name     | Type   | Description |
|----------|--------|-------------|
| fileId   | string | File ID     |
| originId | Number | Origin ID   |

**Returns**

| Type  | Description     |
|-------|-----------------|
| Array | Node Data Array |


</procedure>
 

## FromRoot
<procedure title="전체 최상위 노드 반환" collapsible="true">

<note>

FromRoot() → `{Array<Object>}`
</note>

**Example**
```Javascript
//전체 최상위 노드 반환
let root = vizcore.Object3D.FromRoot();
```
**Returns**

| Type            | Description |
|-----------------|-------------|
| `Array<Object>` | Node ID     |
</procedure>
    

## FromRootByKey
<procedure title="지정된 모델 Key의 최상위 노드 반환" collapsible="true">

<note>

FromRootByKey(key) → `{Array<Object>}`
</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//지정된 모델 Key의 최상위 노드 반환
let nodes = vizcore.Object3D.FromRootByKey("sample1");
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| key  | string | File ID     |

**Returns**

| Type            | Description |
|-----------------|-------------|
| `Array<Object>` | Node ID     |
</procedure>


## FromRootByUrl
<procedure title="지정된 URL의 최상위 노드 반환" collapsible="true">
<note>

FromRootByUrl(url) → `{Array<Object>}`
</note>


**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//지정된 URL의 최상위 노드 반환
let nodes = vizcore.Object3D.FromRootByUrl("./VIZCore/Model/Sample1_wh.vizw");
```
**Parameters**

| Name | Type   | Description       |
|------|--------|-------------------|
| url  | string | File Download URL |

**Returns**

| Type            | Description |
|-----------------|-------------|
| `Array<Object>` | Node ID     |

</procedure>

## GetBodiesByFile
<procedure title="지정된 파일 하위 Body 목록 반환" collapsible="true">
<note>

GetBodiesByFile(fileKey) → `{ArrayObject}`
</note>


**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//지정된 파일 하위 Body 목록 반환
let bodies = vizcore.Object3D.GetBodiesByFile("sample1");
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| fileKey | string | File ID     |

**Returns**

| Type            | Description       |
|-----------------|-------------------|
| `Array<Object>` | Body Object Array |

</procedure>



## GetBodiesByNode
<procedure title="지정된 노드의 하위 Body 목록 반환" collapsible="true">
<note>

GetBodiesByNode(nodes) → {`Array<Object>`}

</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let color = new VIZCore.Color(255, 125, 0, 255);                    //R, G, B, A
//지정된 노드의 하위 Body 목록 반환
let bodies = vizcore.Object3D.GetBodiesByNode(nodes);
vizcore.Object3D.Color.SetColorByBody(bodies, color);
```
**Parameters**

| Name  | Type            | Description       |
|-------|-----------------|-------------------|
| nodes | `Array<Object>` | Node Object Array |

**Returns**

| Type            | Description       |
|-----------------|-------------------|
| `Array<Object>` | Body Object Array |


</procedure>


## GetBodiesByNodeID
<procedure title="지정된 Node ID의 하위 Body 목록 반환" collapsible="true">

<note>

GetBodiesByNodeID(nodeIds) → {`Array<Object>`}
</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let nodeIds = [];                                       //Array<Number>
for (let i = 0; i < nodes.length; i++) {
    nodeIds.push(nodes[i].id);
}
//지정된 Node ID의 하위 Body 목록 반환
let bodies = vizcore.Object3D.GetBodiesByNodeID(nodeIds);
```
**Parameters**

| Name    | Type            | Description          |
|---------|-----------------|----------------------|
| nodeIds | `Array<Number>` | Node Object ID Array |

**Returns**

| Type            | Description       |
|-----------------|-------------------|
| `Array<Object>` | Body Object Array |

</procedure>

## GetBodyIdsByFile
<procedure title="지정된 파일 하위 BodyID 목록 반환" collapsible="true">
<note>

GetBodyIdsByFile(fileKey) → `{Array<Number>}`
</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//지정된 파일 하위 BodyID 목록 반환
let bodyIds = vizcore.Object3D.GetBodyIdsByFile("sample1");
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| fileKey | string | fileKey     |

**Returns**

| Type            | Description   |
|-----------------|---------------|
| `Array<Number>` | Body ID Array |

</procedure>

## GetBodyIdsByNode
<procedure title="지정된 노드 하위 BodyID 목록 반환" collapsible="true">
<note>

GetBodyIdsByNode(nodes) → `{Array<Number>}`
</note>


**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//지정된 노드 하위 BodyID 목록 반환
let bodyIds = vizcore.Object3D.GetBodyIdsByNode(nodes);
```
**Parameters**

| Name  | Type            | Description       |
|-------|-----------------|-------------------|
| nodes | `Array<Object>` | Node Object Array |

**Returns**

| Type            | Description   |
|-----------------|---------------|
| `Array<Number>` | Body ID Array |

</procedure> 

## GetBodyIdsByNodeID
<procedure title="지정된 Node ID 하위 BodyID 목록 반환" collapsible="true">
<note>

GetBodyIdsByNodeID(ids) → `{Array<Number>}`
</note>


**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let nodeIds = [];                                       //Array<Number>
for (let i = 0; i < nodes.length; i++) {
    nodeIds.push(nodes[i].id);
}
//지정된 Node ID 하위 BodyID 목록 반환
let bodyIds = vizcore.Object3D.GetBodyIdsByNodeID(nodeIds);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Node ID Array |

**Returns**

| Type            | Description   |
|-----------------|---------------|
| `Array<Number>` | Body ID Array |

</procedure>



## GetBodyIdsByNodeOriginID
<procedure title="지정된 NodeOriginID 하위 BodyID 목록 반환" collapsible="true">
<note>

GetBodyIdsByNodeOriginID(fileKey, ids) → `{Array<Number>}`
</note>

**Example**
```Javascript
//지정된 NodeOriginID 하위 BodyID 목록 반환
let bodyIds = vizcore.Object3D.GetBodyIdsByNodeOriginID("sample1", [1]);
```
**Parameters**

| Name    | Type             | Description |
|---------|------------------|-------------|
| fileKey | String           | fileKey     |
| ids     | `	Array<Number>` | originIds   |

**Returns**

| Type            | Description   |
|-----------------|---------------|
| `Array<Number>` | Body ID Array |

</procedure>

## GetBoundBox
<procedure title="모델 전체 BoundBox 반환" collapsible="true">
<note>
GetBoundBox() → {VIZCore.BBox}</note>

**Example**
```Javascript
//모델 전체 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBox();
```
**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | BoundBox    |

</procedure>




## GetBoundBoxByNode
<procedure title="지정된 노드의 BoundBox 반환" collapsible="true">
<note>GetBoundBoxByNode(nodes) → {VIZCore.BBox}</note>



**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//지정된 노드의 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBoxByNode(nodes);
```
**Parameters**

| Name  | Type            | Description       |
|-------|-----------------|-------------------|
| nodes | `Array<Object>` | Node Object Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | BoundBox    |

</procedure>

## GetBoundBoxByNodeID
<procedure title="지정된 Node ID의 BoundBox 반환" collapsible="true">
<note>GetBoundBoxByNodeID(nodeIds) → {VIZCore.BBox}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
        
let nodeIds = [];                                       //Array<Number>
for (let i = 0; i < nodes.length; i++) {
    nodeIds.push(nodes[i].id);
}
//지정된 Node ID의 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBoxByNodeID(nodeIds);
```
**Parameters**

| Name    | Type            | Description          |
|---------|-----------------|----------------------|
| nodeIds | `Array<Number>` | Node Object ID Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | BoundBox    |

</procedure>

## GetInnerObjects
<procedure title="BBox 영역 내 노드 반환" collapsible="true">
<note>GetInnerObjects(bbox, union) → {Array}</note>

**Example**
```Javascript
//모델 전체 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBox();
//BBox 영역 내 노드 반환
let nodes = vizcore.Object3D.GetInnerObjects(bbox, true);
```
**Parameters**

| Name  | Type         | Description |
|-------|--------------|-------------|
| bbox  | VIZCore.BBox | BoundBox    |
| union | 	Boolean     | 전체 포함 여부    |

**Returns**

| Type  | Description   |
|-------|---------------|
| Array | Node ID Array |

</procedure>

## GetNodeStructure
<procedure title="Node ID의 Structure 정보 반환" collapsible="true">
<note>GetNodeStructure(id, topDown) → {Array}</note>

**Example**
```Javascript
// Node ID의 Structure 정보 반환
console.log(vizcore.Object3D.GetNodeStructure(9,false));
```
**Parameters**

| Name    | Type    | Description                    |
|---------|---------|--------------------------------|
| id      | Number  | Node ID                        |
| topDown | Boolean | True(TopDown), False(BottomUp) |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | Node Array  |
</procedure>

## GetOriginBoundBox
<procedure title="모델 Origin BoundBox 반환" collapsible="true">
<note>GetOriginBoundBox(nodes) → {VIZCore.BBox}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//모델 Origin BoundBox 반환
let bbox = vizcore.Object3D.GetOriginBoundBox(nodes);
```
**Parameters**

| Name  | Type            | Description       |
|-------|-----------------|-------------------|
| nodes | `Array<Object>` | Node Object Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | BoundBox    |

</procedure>

## GetSelectedObject3D
<procedure title="선택된 모델 반환" collapsible="true">
<note>

GetSelectedObject3D() → {`Array<Number>`}
</note>

**Example**
```Javascript
//선택된 모델 반환
let item = vizcore.Object3D.GetSelectedObject3D();
```
**Returns**

| Type            | Description   |
|-----------------|---------------|
| `Array<Number>` | Body ID Array |

</procedure>

## HideUnselectedObject 
<procedure title="비선택 개체 숨기기" collapsible="true">
<note>HideUnselectedObject()</note>


**Example**
```Javascript
//비선택 개체 숨기기
vizcore.Object3D.HideUnselectedObject();
```
</procedure>

## InvertSelection 
<procedure title="선택 반전" collapsible="true">
<note>InvertSelection()</note>

**Example**
```Javascript
//선택 반전
vizcore.Object3D.InvertSelection();
```
</procedure>

## LockMeshCache
<procedure title="Mesh Cache 메모리 우선 사용" collapsible="true">
<note>LockMeshCache(fileKey)</note>


**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//Mesh Cache 메모리 우선 사용
vizcore.Object3D.LockMeshCache("sample1");
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| fileKey | Object | 파일 ID       |
</procedure>

## RefreshBBox
<procedure title="모델 전체 BoundBox 재계산" collapsible="true">
<note>RefreshBBox()</note>

**Example**
```Javascript
//모델 전체 BoundBox 재계산
vizcore.Object3D.RefreshBBox();
```
</procedure>

## SelectAll
<procedure title="전체 개체 선택 / 선택해제" collapsible="true">
<note>SelectAll(select)</note>

**Example**
```Javascript
vizcore.Object3D.SelectAll(true);  // 전체 개체 선택
vizcore.Object3D.SelectAll(false); // 전체 개체 선택해제
```
**Parameters**

| Name   | Type    | Description                 |
|--------|---------|-----------------------------|
| select | Boolean | True(전체 선택), False(전체 선택해제) |
</procedure>

## SelectByFile
<procedure title="지정 파일로 모델 선택/해제 설정" collapsible="true">
<note>SelectByFile(fileIds, selection, append)</note>

**Example**
```Javascript
//모델 선택/해제 설정
let fileId = "FileKey";                                         //FileID
vizcore.Object3D.SelectByFile(fileId, true, true);

let fileIds = ["FileKey1", "FileKey2"];                         //FileID Array
vizcore.Object3D.SelectByFile(fileIds, true, true);
```
**Parameters**

| Name      | Type    | Description                    |
|-----------|---------|--------------------------------|
| fileIds   | Object  | FileID or FileID Array         |
| selection | Boolean | true: 선택 / false: 선택해제         |
| append    | Boolean | true: 선택추가 / false: 해당 id 만 선택 |
</procedure>

## SelectByNode
<procedure title="지정 노드로 모델 선택/해제 설정" collapsible="true">
<note>SelectByNode(nodes, selection, append)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//모델 선택/해제 설정
vizcoreide3d.Object3D.SelectByNode(nodes, true, true);
```
**Parameters**

| Name      | Type    | Description                    |
|-----------|---------|--------------------------------|
| nodes     | Array   | Node Array                     |
| selection | Boolean | true: 선택 / false: 선택해제         |
| append    | Boolean | true: 선택추가 / false: 해당 id 만 선택 |
</procedure>

## SelectByNodeID
<procedure title="지정 노드 아이디로 모델 선택/해제 설정" collapsible="true">
<note>SelectByNodeID(ids, selection, append)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
let ids = [];                                       //Node ID Array
for (let i = 0; i < nodes.length; i++) {
ids.push(nodes[i].id);
}
//모델 선택/해제 설정
vizcore.Object3D.SelectByNodeID(ids, true, true);
```
Parameters:

| Name      | Type    | Description                    |
|-----------|---------|--------------------------------|
| ids       | Array   | Node ID Array                  |
| selection | Boolean | true: 선택 / false: 선택해제         |
| append    | Boolean | true: 선택추가 / false: 해당 id 만 선택 |
</procedure>

## SelectByOrigin
<procedure title="지정 OriginID로 모델 선택/해제 설정" collapsible="true">
<note>SelectByOrigin(fileIds, originIds, selection, append, event)</note>


**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
let fileIds = [];                                               //File ID Array
let originIds = [];                                             //Origin ID Array
for (let i = 0; i < nodes.length; i++) {
fileIds.push(nodes[i].fileId);
originIds.push(nodes[i].originId);
}
//모델 선택/해제 설정
vizcore.Object3D.SelectByOrigin(fileIds, originIds, true, true, true);
```
**Parameters**

| Name      | Type    | Description                           |
|-----------|---------|---------------------------------------|
| fileIds   | Array   | File ID Array                         |
| originIds | Array   | Origin ID Array                       |
| selection | Boolean | true: 선택 / false: 선택해제                |
| append    | Boolean | true: 선택추가 / false: 해당 id 만 선택        |
| event     | Boolean | true: 선택 이벤트 활성화 / false: 선택 이벤트 비활성화 |
</procedure>

## SetObjectDisableViewDistanceBBox
<procedure title="지정한 개체 설정 거리보다 먼 경우 박스 표시 설정 미적용(SetViewDistanceBox로 지정한 파일 ID만 적용)" collapsible="true">
<note>SetObjectDisableViewDistanceBBox(fileKey, originId, disable)</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);

function exampleButtonClick() {
    //설정 거리보다 먼 경우 박스로 표시
    vizcore.Object3D.SetViewDistanceBox("sample1", 100);  
    //SetViewDistanceBox으로 지정한 파일 ID만 적용
    vizcore.Object3D.SetObjectDisableViewDistanceBBox("sample1", 10, true);
}
```
**Parameters**

| Name     | Type    | Description                  |
|----------|---------|------------------------------|
| fileKey  | String  | 파일 ID                        |
| originId | Number  | Node ID                      |
| disable  | Boolean | true : 미적용으로 설정 , false : 적용 |
</procedure>

## SetObjectDisableViewDistanceBBoxByArray
<procedure title="지정한 개체 설정 거리보다 먼 경우 박스 표시 설정 미적용(SetViewDistanceBox로 지정한 파일 ID만 적용)" collapsible="true">
<note>SetObjectDisableViewDistanceBBoxByArray(fileKey, arrayObjectID, disable)</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);

function exampleButtonClick() {
        let arrayObjectID = [10, 20];
        //설정 거리보다 먼 경우 박스로 표시
        vizcore.Object3D.SetViewDistanceBox("sample1", 100);
        //지정한 개체 설정 거리보다 먼 경우 박스 표시 설정 미적용
        vizcore.Object3D.SetObjectDisableViewDistanceBBoxByArray("sample1", arrayObjectID, true);
}
```
**Parameters**

| Name          | Type    | Description                  |
|---------------|---------|------------------------------|
| fileKey       | String  | 파일 ID                        |
| arrayObjectID | Array   | Node ID Array                |
| disable       | Boolean | true : 미적용으로 설정 , false : 적용 |
</procedure>

## SetSelectionColor
<procedure title="선택 모델 하이라이트 색상 설정" collapsible="true">
<note>SetSelectionColor(color)</note>

**Example**
```Javascript
let color = new VIZCore.Color(255, 0, 0, 255);                  //R, G, B, A
//선택 모델 하이라이트 색상 설정
vizcore.Object3D.SetSelectionColor(color);
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| color | VIZCore.Color | 하이라이트 색상    |
</procedure>

## SetViewDistanceBox
<procedure title="설정 거리보다 먼 경우 박스 로 표시" collapsible="true">
<note>SetViewDistanceBox(fileKey, distance)</note>

**Example**
```Javascript
//VIZWide3D 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//설정 거리보다 먼 경우 박스 로 표시
vizcore.Object3D.SetViewDistanceBox('sample1', 0.5);
```
**Parameters**

| Name     | Type    | Description |
|----------|---------|-------------|
| fileKey  | 	Object | 파일 ID       |
| distance | Number  | 거리          |
</procedure>

## ShowAll
<procedure title="모델 전체 보이기/숨기기 설정" collapsible="true">
<note>ShowAll(visible)</note>

**Example**
```Javascript
//모델 전체 보이기/숨기기 설정
vizcore.Object3D.ShowAll(true);
```
**Parameters**

| Name    | Type     | Description           |
|---------|----------|-----------------------|
| visible | 	Boolean | true: 보이기, false: 숨기기 |
</procedure>

## ShowByFile
<procedure title="파일 기준 모델 보이기/숨기기 설정" collapsible="true">
<note>ShowByFile(fileIds, visible)</note>

**Example**
```Javascript
//모델 선택/해제 설정
let fileId = "FileKey";
vizcore.Object3D.SelectByFile(fileId, true);
//파일 기준 모델 보이기/숨기기 설정
let fileIds = ["FileKey1", "FileKey2"];
vizcore.Object3D.ShowByFile(fileIds, true);
```
**Parameters**

| Name    | Type    | Description            |
|---------|---------|------------------------|
| fileIds | 	Object | FileID or FileID Array |
| visible | Boolean | true: 보이기 / false: 숨기기 |
</procedure>

## ShowByNode
<procedure title="노드 기준 모델 보이기/숨기기 설정" collapsible="true">
<note>ShowByNode(nodes, visible)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//모델 보이기/숨기기 설정
vizcore.Object3D.ShowByNode(nodes, true);
```
**Parameters**

| Name    | Type    | Description            |
|---------|---------|------------------------|
| nodes   | 	Array  | Node Array             |
| visible | Boolean | true: 보이기 / false: 숨기기 |
</procedure>

## ShowByNodeID
<procedure title="Node ID 기준 모델 보이기/숨기기 설정" collapsible="true">
<note>ShowByNodeID(ids, visible)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let ids = [];                                       //Node ID Array 
for (let i = 0; i < nodes.length; i++) {
    ids.push(nodes[i].id);
}
//모델 보이기/숨기기 설정
vizcore.Object3D.ShowByNodeID(ids, false);
```
**Parameters**

| Name    | Type    | Description            |
|---------|---------|------------------------|
| ids     | 	Array  | Node ID Array          |
| visible | Boolean | true: 보이기 / false: 숨기기 |
</procedure>

## ShowByOrigin
<procedure title="Origin  ID 기준 모델 보이기/숨기기 설정" collapsible="true">
<note>ShowByOrigin(fileIds, originIds, visible)</note>


**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//전체 개체 선택 / 선택해제
vizcore.View.SelectAll(false);

let fileIds = [];                                       //File ID Array
let originIds = [];                                     //Origin  ID Array 
for (let i = 0; i < nodes.length; i++) {
    fileIds.push(nodes[i].fileId);
    originIds.push(nodes[i].originId);
}
//Origin  ID 기준 모델 보이기/숨기기 설정
vizcore.Object3D.ShowByOrigin(fileIds, originIds, true);
```
**Parameters**

| Name      | Type    | Description            |
|-----------|---------|------------------------|
| fileIds   | 	Array  | File ID Array          |
| originIds | 	Array  | Origin  ID Array       |
| visible   | Boolean | true: 보이기 / false: 숨기기 |
</procedure>

## ShowSelectedObject
<procedure title="선택 개체 보이기 / 숨기기" collapsible="true">
<note>ShowSelectedObject(visible)</note>

**Example**
```Javascript
//선택 개체 보이기 / 숨기기
vizcore.Object3D.ShowSelectedObject(true);
```
**Parameters**

| Name    | Type    | Description            |
|---------|---------|------------------------|
| visible | Boolean | true: 보이기 / false: 숨기기 |
</procedure>

## UnlockMeshCache
<procedure title="Mesh Cache 메모리 우선 사용해제" collapsible="true">
<note>UnlockMeshCache(fileKey)</note>

**Example**
```Javascript
//vizcore 용 VIZW 파일의 헤더 추가
let models = [];
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
vizcore.Model.AddHeader(models);
//Mesh Cache 메모리 우선 사용해제
vizcore.Object3D.UnlockMeshCache("sample1");
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| fileKey | Object | 파일 ID       |
</procedure>

## --- Event Listener ---

## OnBoxSelected
<procedure title="선택상자 선택 이벤트 등록" collapsible="true">
<note>OnBoxSelected(listener)</note>

**Example**
```Javascript
// Event : OnBoxSelectedEvent
let OnBoxSelected = function (event) {
    //event.data == Object ID List

     if(event.data.length <= 0) {
         // 선택된 모델이 없음
     }
     else
     {
         //해당 노드 포커스
         vizcore.View.Camera.FocusObject(event.data);
     }
}
// Add Event Handler : Object SelectBox Selected Event (선택상자 선택 이벤트)
vizcore.Object3D.OnBoxSelected(OnBoxSelected);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnObject3DSelected
<procedure title="개체 선택 이벤트 등록" collapsible="true">
<note>OnObject3DSelected(listener)</note>

**Example**
```Javascript
// Event : OnObject3DSelectedEvent
let OnObject3DSelected = function (event) {
    // 선택된 모델이 없음
    if (event.data.id == -1) {
        //alert('선택된 모델이 없거나, 기존 선택상태가 해제됨.');
    }
    // 선택된 모델이 있음
    else {
        // 지정된 ID의 노드 정보 조회
        let node = vizcore.Object3D.FromID(event.data.id);

        let nodeId = node.id;
        let nodeIndex = node.index;
        let nodeKind = node.kind;
        let nodeKindStr = node.kindStr;
        let nodeParentId = node.parentId;
        let nodeName = node.name;
        let nodeLevel = node.level;
        let selection = node.selection;
        let visible = node.visible;
        let nodeBoundBox = node.boundBox;
    }
}

// Add Event Handler : Object Selected Event (개체 선택 이벤트)
vizcore.Object3D.OnObject3DSelected(OnObject3DSelected);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>