# GeometryProperty

## GetBoundBoxByBody
<procedure title="지정된 Body (Array) 의 BoundBox 반환" collapsible="true">
<note>GetBoundBoxByBody(bodies) → {VIZCore.BBox}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let color = new VIZCore.Color(255, 125, 0, 255);              //R, G, B, A

//지정된 노드의 하위 Body 목록 반환
let bodies = vizcore.Object3D.GetBodiesByNode(nodes);
//지정된 Body (Array) 의 BoundBox 반환
vizcore.Object3D.GeometryProperty.GetBoundBoxByBody(bodies);
```
**Parameters**

| Name   | Type            | Description       |
|--------|-----------------|-------------------|
| bodies | `Array<Object>` | Body Object Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | Bound Box   |
</procedure>

## GetBoundBoxByNode
<procedure title="지정된 Nodes 의 BoundBox 반환" collapsible="true">
<note>GetBoundBoxByNode(nodes) → {VIZCore.BBox}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//지정된 Nodes 의 BoundBox 반환
let boundBox = vizcore.Object3D.GeometryProperty.GetBoundBoxByNode(nodes);
```
**Parameters**

| Name  | Type            | Description       |
|-------|-----------------|-------------------|
| nodes | `Array<Object>` | Node Object Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | Bound Box   |
</procedure>

## GetBoundBoxByNodeID
<procedure title="지정된 Node ID (Array) 의 BoundBox 반환" collapsible="true">
<note>GetBoundBoxByNodeID(ids) → {VIZCore.BBox}</note>

**Example**
```Javascript
let ids = [];                   //Node ID Array
ids.push(100);
ids.push(200);
ids.push(300);
//지정된 Node ID (Array) 의 BoundBox 반환
vizcore.Object3D.GeometryProperty.GetBoundBoxByNodeID(ids);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Object>` | Node ID Array |

**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | Bound Box   |
</procedure>