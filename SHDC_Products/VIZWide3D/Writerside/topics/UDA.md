# UDA

## AddByNodeID
<procedure title="지정된 개체의 기존 속성을 유지한채 속성을 추가" collapsible="true">
<note>AddByNodeID(nodeId, key, value)</note>

**Example**
```Javascript
let nodeId = 5;                                         //nodeId
let key = "NAME";                                       //key
let value = "/NO1_FLEX_G3";                             //value
//지정된 개체의 기존 속성을 유지한채 속성을 추가
vizcore.Object3D.UDA.AddByNodeID(nodeId, key, value);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| nodeId | Number | 노드 아이디      |
| key    | String | 속성 Key      |
| value  | String | 속성 value    |
</procedure>

## ClearDataToUDADialog
<procedure title="Clear Data(Refresh) To UDA Dialog" collapsible="true">
<note>ClearDataToUDADialog()</note>

**Example**
```Javascript
//Clear Data(Refresh) To UDA Dialog
vizcore.Object3D.UDA.ClearDataToUDADialog();
```
</procedure>

## DeleteByNodeID
<procedure title="지정된 개체의 해당 속성을 삭제" collapsible="true">
<note>DeleteByNodeID(nodeId)</note>

**Example**
```Javascript
let nodeId = 5;
//지정된 개체의 해당 속성을 삭제
vizcore.Object3D.UDA.DeleteByNodeID(nodeId);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| nodeId | Number | 노드 아이디      |
</procedure>

## DeleteKeyByNodeID
<procedure title="지정된 개체의 해당 속성을 삭제" collapsible="true">
<note>DeleteKeyByNodeID(nodeId, key)</note>

**Example**

```Javascript  
// [To Do] vizcore.Configuration.Property.UseArrayBuffer = false 일 때만 가능
vizcore.Configuration.Property.UseArrayBuffer = false;

let nodeId = 5;                                            //nodeId 
let key = "TYPE";                                          //key
//지정된 개체의 해당 속성을 삭제
vizcore.Object3D.UDA.DeleteKeyByNodeID(nodeId, key);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| nodeId | Number | 노드 아이디      |
| key    | String | 속성 Key      |
</procedure>

## FromNodeID
<procedure title="Node ID에 해당하는 속성 정보 반환" collapsible="true">
<note>FromNodeID(nodeId) → {Array}</note>

**Example**
```Javascript
let nodeId = 5;
//Node ID에 해당하는 속성 정보 반환
let fromNodeId = vizcore.Object3D.UDA.FromNodeID(nodeId);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| nodeId | Number | 노드 아이디      |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | 사용자 정의 속성   |
</procedure>

## FromOrigin
<procedure title="FileID, OriginID에 해당하는 속성 정보 반환" collapsible="true">
<note>FromOrigin(fileId, originId) → {Array}</note>

**Example**
```Javascript
//FileID, OriginID에 해당하는 속성 정보 반환
let node = vizcore.Object3D.UDA.FromOrigin("FileKey", 1);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| fileId | Object | File ID     |
| origin | Number | Origin ID   |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | 사용자 정의 속성   |
</procedure>

## GetBodyIDs
<procedure title="속성(KEY, VALUE)에 해당하는 BODY ID 배열" collapsible="true">
<note>GetBodyIDs(key, value) → {Array}</note>

**Example**
```Javascript
//속성(KEY, VALUE)에 해당하는 BODY ID 배열
let uda_bodyIDs = vizcore.Object3D.UDA.GetBodyIDs("NAME", "/NO1_FLEX_G3");

if (uda_bodyIDs !== undefined) {
    for (let i = 0; i < uda_bodyIDs.length; i++) {
    console.log("NAME : /NO1_FLEX_G3 - BODYID: " + uda_bodyIDs[i]);
    }
}
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| key   | String | 속성 Key      |
| value | String | 속성 Value    |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | BODY ID     |
</procedure>

## GetCustomDataItem
<procedure title="사용자 추가 속성 오브젝트 반환" collapsible="true">
<note>GetCustomDataItem(key, value) → {Object}</note>

**Example**
```Javascript
for (let index = 0; index < 3; index++) {
    //사용자 추가 속성 오브젝트 반환
    let item = vizcore.Object3D.UDA.GetCustomDataItem("key" + index, "value" + index);
    console.log(item);
}
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| key   | String | 속성 Key      |
| value | String | 속성 Value    |

**Returns**

| Type   | Description          |
|--------|----------------------|
| Object | {key:' ', value:' '} |

</procedure>

## GetKeys
<procedure title="속성 키 목록 반환" collapsible="true">
<note>GetKeys() → {Array}</note>

**Example**
```Javascript
let keys = [];
//속성 키 목록 반환
keys = vizcore.Object3D.UDA.GetKeys();
```
**Returns**

| Type  | Description |
|-------|-------------|
| Array | 키 목록 배열     |

</procedure>

## GetNodeIDs
<procedure title="속성(KEY, VALUE)에 해당하는 NODE ID 배열" collapsible="true">
<note>GetNodeIDs(key, value) → {Array}</note>

**Example**
```Javascript
//속성(KEY, VALUE)에 해당하는 NODE ID 배열
let uda_nodeIds = vizcore.Object3D.UDA.GetNodeIDs("NAME", "/NO1_FLEX_G3");

if (uda_nodeIds !== undefined) {
    for (let i = 0; i < uda_nodeIds.length; i++) {
    console.log("NAME : /NO1_FLEX_G3 - NODEID: " + uda_nodeIds[i]);
    }
}
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| key   | String | 속성 Key      |
| value | String | 속성 Value    |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | NODE IDs    |
</procedure>

## GetNodeIDsByValue
<procedure title="속성(VALUE)에 해당하는 NODE ID 배열" collapsible="true">
<note>GetNodeIDsByValue(value) → {Array}</note>

**Example**
```Javascript
//속성(VALUE)에 해당하는 NODE ID 배열
let uda_nodeIds = vizcore.Object3D.UDA.GetNodeIDsByValue("/NO1_FLEX_G3", true);

    if (uda_nodeIds !== undefined) {
    for (let i = 0; i < uda_nodeIds.length; i++) {
    console.log("NAME : /NO1_FLEX_G3 - NODEID: " + uda_nodeIds[i]);
    }
}
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| value | String | 속성 Value    |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | NODE IDs    |
</procedure>

## GetPropertyInfo
<procedure title="전체 속성별 노드 정보 반환" collapsible="true">
<note>GetPropertyInfo() → {Object}</note>

**Example**
```Javascript
//전체 속성별 노드 정보 반환
let mapInfo = vizcore.Object3D.UDA.GetPropertyInfo();
console.log(mapInfo);
```
**Returns**

| Type   | Description                                                                                |
|--------|--------------------------------------------------------------------------------------------|
| Object | {keyMap : Key 기준 노드 정렬 맵, valueMap : value 기준 노드 정렬 맵, keyValueMap : key+value 기준 노드 정렬 맵} |

</procedure>

## GetValueByKeyFromNodeId
<procedure title="아이디에 해당하는 노드에서 특정 키의 값 반환" collapsible="true">
<note>GetValueByKeyFromNodeId(id, key) → {String}</note>

**Example**
```Javascript
let nodeId = 5;                                         //nodeId
let key = "TYPE";                                       //key
//아이디에 해당하는 노드에서 특정 키의 값 반환
let value = vizcore.Object3D.UDA.GetValueByKeyFromNodeId(nodeId, key);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | Number | 노드 아이디      |
| key  | String | 속성 Key      |

**Returns**

| Type   | Description |
|--------|-------------|
| String | 값(Value)    |
</procedure>

## GetValues
<procedure title="속성 키에 해당하는 값 목록 반환" collapsible="true">
<note>GetValues(key) → {Array}</note>

**Example**
```Javascript
let values = [];
//속성 키에 해당하는 값 목록 반환
values = vizcore.Object3D.UDA.GetValues("TYPE");
```
**Parameters**

| Name | Type         | Description |
|------|--------------|-------------|
| key  | String       | 속성 Key      |

**Returns**

| Type  | Description    |
|-------|----------------|
| Array | 값(Value) 목록 배열 |
</procedure>

## Select
<procedure title="속성(KEY, VALUE)에 해당하는 개체 선택" collapsible="true">
<note>Select(key, value) → {Array}</note>

**Example**
```Javascript
//속성(KEY, VALUE)에 해당하는 개체 선택
let uda_NodeID = vizcore.Object3D.UDA.Select("NAME", "/NO1_FLEX_G3");
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| key   | String | 속성 Key      |
| value | String | 속성 Value    |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | NODE IDs    |
</procedure> 

## SetCustomDataByNodeID
<procedure title="휘발성 사용자 정의 속성 설정 속성 최상단에 추가 Object 선택 이벤트와 연동하여 사용 권장" collapsible="true">
<note>SetCustomDataByNodeID(id, items)</note>

**Example**
```Javascript
let id = 3;                                                         //id
let items = [];                                                     //Array
for (let index = 0; index < 3; index++) {
    //사용자 추가 속성 오브젝트 반환
    let item = vizcore.Object3D.UDA.GetCustomDataItem("key" + index, "value" + index);
    items.push(item);
}
//사용자 정의 속성 설정 속성
vizcore.Object3D.UDA.SetCustomDataByNodeID(id, items);
```
**Parameters**

| Name  | Type   | Description      |
|-------|--------|------------------|
| id    | Number | Node ID          |
| items | Array  | 사용자 추가 속성 아이템 목록 |
</procedure>

## ShowDataToUDADialog
<procedure title="Show Data(Refresh) To UDA Dialog" collapsible="true">
<note>ShowDataToUDADialog(nodeId)</note>



**Example**
```Javascript
let nodeId = 5;
//Show Data To UDA Dialog
vizcore.Object3D.UDA.ShowDataToUDADialog(nodeId);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| nodeId | Number | 노드 아이디      |
</procedure>

## ShowUDADialog
<procedure title="UDA (User-Defined Attributes) Dialog 보이기 숨기기" collapsible="true">
<note>ShowUDADialog(visible)</note>

**Example**
```Javascript
//UDA (User-Defined Attributes) Dialog 보이기 숨기기
vizcore.Object3D.UDA.ShowUDADialog(true);
```
**Parameters**

| Name    | Type    | Description             |
|---------|---------|-------------------------|
| visible | boolean | true : 보이기, false : 숨기기 |
</procedure>