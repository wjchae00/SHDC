# Transform

## GetEnableHandle
<procedure title="개체 이동/회전 핸들 모드 여부 반환" collapsible="true">
<note>GetEnableHandle() → {boolean}</note>

**Example**
```Javascript
//개체 이동/회전 핸들 모드 여부 반환
let enable = vizcore.Object3D.Transform.GetEnableHandle();
```
**Returns**

| Type    | Description         |
|---------|---------------------|
| boolean | Control 핸들 사용 여부 반환 |
</procedure>

## RestoreTransformAll
<procedure title="개체 이동/회전 초기화" collapsible="true">
<note>RestoreTransformAll()</note>

**Example**
```Javascript
//개체 이동/회전 초기화
vizcore.Object3D.Transform.RestoreTransformAll();
```
</procedure>

## RestoreTransformByBodyID
<procedure title="지정한 Body 개체 이동/회전 초기화" collapsible="true">
<note>RestoreTransformByBodyID(ids)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let nodeIds = [];                                   //Body ID Array
for (let i = 0; i < nodes.length; i++) {
    nodeIds.push(nodes[i].id);
}
//지정된 개체 하위 BodyID 목록 반환
let ids = vizcore.Object3D.GetBodyIdsByNodeID(nodeIds);
//지정한 Body 개체 이동/회전 초기화
vizcore.Object3D.Transform.RestoreTransformByBodyID(ids);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Body ID Array |
</procedure>

## RestoreTransformByNodeID
<procedure title="지정한 Node 개체 이동/회전 초기화" collapsible="true">
<note>RestoreTransformByNodeID(ids)</note>

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
//지정한 Node 개체 이동/회전 초기화
vizcore.Object3D.Transform.RestoreTransformByNodeID(ids);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Node ID Array |
</procedure>

## SetEnableHandle
<procedure title="개체 이동/회전 핸들 모드" collapsible="true">
<note>SetEnableHandle(enable)</note>

**Example**
```Javascript
//개체 이동/회전 핸들 모드
vizcore.Object3D.Transform.SetHandleMode(true);
```  
**Parameters**

| Name   | Type    | Description              |
|--------|---------|--------------------------|
| enable | Boolean | true : 활성화, false : 비활성화 |
</procedure>

## SetTransform
<procedure title="개체 이동/회전" collapsible="true">
<note>SetTransform(ids, move, rotate)</note>

**Example**
```Javascript
let nodeID = 2000;
let bodyID = 3000;      
let ids = [nodeID , bodyID];                            //Array<Number>
let move = new VIZCore.Vector3(1000, 2000, 0);          //이동값 : VIZCore.Vector3()
let rotate = new VIZCore.Vector3(0, 0, 90);             //회전값 : VIZCore.Vector3()
//개체 이동/회전
vizcore.Object3D.Transform.SetTransform(ids, move, rotate);
```
**Parameters**

| Name   | Type            | Description             |
|--------|-----------------|-------------------------|
| ids    | `Array<Number>` | Node ID Array           |
| move   | VIZCore.Vector3 | 이동값 : VIZCore.Vector3() |
| rotate | VIZCore.Vector3 | 회전값 : VIZCore.Vector3() |
</procedure>

## SetTransformByBodyID
<procedure title="Body ID 기준 개체 이동/회전" collapsible="true">
<note>SetTransformByBodyID(ids, transform)</note>

**Example**
```Javascript
let bodyId = [2000];                                      //Number
let transform = new VIZCore.Matrix4();
transform.translate(100, 0, 0);
//개체 이동/회전
vizcore.Object3D.Transform.SetTransformByBodyID(bodyId, transform);
```
**Parameters**

| Name      | Type            | Description       |
|-----------|-----------------|-------------------|
| ids       | Array           | Node Array        |
| transform | VIZCore.Matrix4 | VIZCore.Matrix4() |
</procedure>

## SetTransformByMatrix
<procedure title="Matrix 기준 개체 이동/회전" collapsible="true">
<note>SetTransformByMatrix(ids, transform)</note>

**Example**
```Javascript
let nodeID = 2000;
let bodyID = 3000;
let ids = [nodeID , bodyID];                              //Array<Number>
let transform = new VIZCore.Matrix4();
transform.translate(100, 0, 0);
//개체 이동/회전
vizcore.Object3D.Transform.SetTransformByMatrix(ids, transform);
```
**Parameters**

| Name      | Type            | Description   |
|-----------|-----------------|---------------|
| ids       | `Array<Number>` | Node ID Array |
| transform | VIZCore.Matrix4 | Matrix4       |
</procedure>

## SetTransformByNode
<procedure title="Node 기준 개체 이동/회전" collapsible="true">
<note>SetTransformByNode(nodes, transform)</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
let transform = new VIZCore.Matrix4();
transform.translate(100, 0, 0);
//개체 이동/회전
vizcore.Object3D.Transform.SetTransformByNode(nodes, transform);
```
**Parameters**

| Name      | Type            | Description       |
|-----------|-----------------|-------------------|
| nodes     | `Array<Object>` | Node Object Array |
| transform | VIZCore.Matrix4 | Matrix4           |
</procedure>

## TransformByBodyID
<procedure title="Body ID 기준 개체 이동/회전" collapsible="true">
<note>TransformByBodyID(bodyId, move, rotate)</note>

**Example**
```Javascript   
let bodyId = 2000;                                            //Node
let move = new VIZCore.Vector3(1000, 2000, 0);                //이동값 : VIZCore.Vector3()
let rotate = new VIZCore.Vector3(0, 0, 90);                   //회전값 : VIZCore.Vector3()
//개체 이동/회전
vizcore.Object3D.Transform.TransformByBodyID(bodyId, move, rotate);
```
**Parameters**

| Name   | Type            | Description             |
|--------|-----------------|-------------------------|
| bodyId | Number          | Node ID                 |
| move   | VIZCore.Vector3 | 이동값 : VIZCore.Vector3() |
| rotate | VIZCore.Vector3 | 회전값 : VIZCore.Vector3() |
</procedure>