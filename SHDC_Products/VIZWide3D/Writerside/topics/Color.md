# Color 

## ClearAll
<procedure title="색상 전체 초기화" collapsible="true">
<note>ClearAll()</note>

**Example**
```Javascript
//색상 전체 초기화
vizcore.Object3D.Color.ClearAll();
```
</procedure>

## ClearAlpha
<procedure title="개체 투명도 초기화" collapsible="true">
<note>ClearAlpha(ids)</note>

**Example**

```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];    //Array<Number>
//개체 투명도 초기화
vizcore.Object3D.Color.ClearAlpha(ids);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Node ID Array |
</procedure>

## ClearByBodyID
<procedure title="지정된 Body IDs 색상 초기화" collapsible="true">
<note>ClearByBodyID(bodyIds)</note>

**Example**
```Javascript
let nodeIds = [1];      //Array
let bodyIDs = vizwide3d.Object3D.GetBodyIdsByNodeID(nodeIds);   //지정된 개체 하위 BodyID 목록 반환
//지정된 Body IDs 색상 초기화
vizcore.Object3D.Color.ClearByBodyID(bodyIDs);
```
**Parameters**

| Name    | Type  | Description    |
|---------|-------|----------------|
| bodyIds | Array | Body IDs Array |
</procedure>

## ClearColor
<procedure title="개체 색상 및 투명도 초기화" collapsible="true">
<note>ClearColor(ids)</note>

**Example**
```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];        //Array<Number>
//개체 색상 및 투명도 초기화
vizcore.Object3D.Color.ClearColor(ids);

//[To Do] 화면 다시그리기 호출
vizcore.Main.Renderer.MainFBClear();
vizcore.Main.Renderer.Render();
```
**Parameters**

| Name | Type             | Description   |
|------|------------------|---------------|
| ids  | `Array<Number>`	 | Node ID Array |
</procedure>

## ClearRGB
<procedure title="개체 색상 초기화" collapsible="true">
<note>ClearRGB(ids)</note>

**Example**
```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];        //Array<Number>
//개체 색상 초기화
vizcore.Object3D.Color.ClearRGB(ids);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Node ID Array |
</procedure>

## SetAlpha
<procedure title="개체 투명도 변경" collapsible="true">
<note>SetAlpha(ids, alpha)</note>

**Example**
```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];        //Array<Number>
let alpha = 100;        //alpha
//개체 투명도 변경
vizcore.Object3D.Color.SetAlpha(ids, alpha);
```
**Parameters**

| Name  | Type            | Description   |
|-------|-----------------|---------------|
| ids   | `Array<Number>` | Node ID Array |
| alpha | Number          | 0 ~ 255 투명도   |
</procedure>

## SetColor
<procedure title="개체 색상 및 투명도 변경" collapsible="true">
<note>SetColor(ids, color)</note>

**Example**
```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];        //Array<Number>
let color = new VIZCore.Color(255, 125, 0, 255);        //R, G, B, A
//개체 색상 및 투명도 변경
vizcore.Object3D.Color.SetColor(ids, color);
```
**Parameters**

| Name  | Type            | Description   |
|-------|-----------------|---------------|
| ids   | `Array<Number>` | Node ID Array |
| color | VIZCore.Color   | Color         |
</procedure>

## SetColorByBody
<procedure title="바디 색상 변경" collapsible="true">
<note>SetColorByBody(bodies, color)</note>

**Example**
```Javascript
let nodes = vizcore.Object3D.Find.GetNodeByName(      //노드 이름에 해당하는 노드 반환
    'PIPE101'   // Keyword
    , true      // Full Match
);

let color = new VIZCore.Color(255, 125, 0, 255);        //R, G, B, A
let bodies = vizcore.Object3D.GetBodiesByNode(nodes);     //지정된 노드의 하위 Body 목록 반환
//바디 색상 변경
vizcore.Object3D.Color.SetColorByBody(bodies, color);
```
**Parameters**

| Name   | Type          | Description |
|--------|---------------|-------------|
| bodies | Array         | Body Array  |
| color  | VIZCore.Color | Color       |
</procedure>

## SetColorByBodyID
<procedure title="바디 색상 변경" collapsible="true">
<note>SetColorByBodyID(bodyIds, color)</note>

**Example**
```Javascript
let nodeIds = [1];
let bodyIDs = vizcore.Object3D.GetBodyIdsByNodeID(nodeIds);       //Array
//바디 색상 변경
vizcore.Object3D.Color.SetColorByBodyID(bodyIDs, new VIZCore.Color(255, 125, 0, 255));
```
**Parameters**

| Name    | Type          | Description    |
|---------|---------------|----------------|
| bodyIds | Array         | Body IDs Array |
| color   | VIZCore.Color | Color          |
</procedure>

## SetColorByFile
<procedure title="색상 변경" collapsible="true">
<note>SetColorByFile(fileId, color)</note>

**Example**
```Javascript
let fileId = "FileKey";     //FileID
let color = new VIZCore.Color(255, 125, 0, 255);        //R, G, B, A
//색상 변경
vizcore.Object3D.Color.SetColorByFile(fileId, color);
```
**Parameters**

| Name   | Type          | Description |
|--------|---------------|-------------|
| fileId | Object        | File ID     |
| color  | VIZCore.Color | Color       |
</procedure>

## SetColorByNode
<procedure title="노드 색상 변경" collapsible="true">
<note>SetColorByNode(nodes, color)</note>

**Example**
```Javascript
let nodes = vizcore.Object3D.Find.GetNodeByName(      //노드 이름에 해당하는 노드 반환
    'PIPE101'   // Keyword
    , true      // Full Match
);
//노드 색상 변경
vizcore.Object3D.Color.SetColorByNode(nodes, new VIZCore.Color(255, 125, 0, 255));
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| nodes | Array         | Node Array  |
| color | VIZCore.Color | Color       |
</procedure>

## SetColorByNodeID
<procedure title="노드 ID 기준 색상 변경" collapsible="true">
<note>SetColorByNodeID(nodeIds, color)</note>

**Example**
```Javascript
let nodeIds = [];       //Node ID Array
nodeIds.push(100);
nodeIds.push(200);
nodeIds.push(300);
//노드 색상 변경
vizcore.Object3D.Color.SetColorByNodeID(nodeIds, new VIZCore.Color(255, 125, 0, 255));
```

**Parameters**

| Name    | Type          | Description   |
|---------|---------------|---------------|
| nodeIds | Array         | Node ID Array |
| color   | VIZCore.Color | Color         |
</procedure>

## SetColorByOrigin
<procedure title="색상 변경" collapsible="true">
<note>SetColorByOrigin(fileIds, originIds, color)</note>

**Example**
```Javascript
let nodes = vizcore.Object3D.Find.GetNodeByName(      //노드 이름에 해당하는 노드 반환
    'PIPE101'   // Keyword
    , true      // Full Match
);

let fileIds = [];       //File IDs Array
let originIds = [];     //Origin IDs Array

for (let i = 0; i < nodes.length; i++) {        //push FileIDs, OriginIDs
    fileIds.push(nodes[i].fileId);
    originIds.push(nodes[i].originId);
}

let color = new VIZCore.Color(255, 125, 0, 255);        //R, G, B, A
//색상 변경
vizcore.Object3D.Color.SetColorByOrigin(fileIds, originIds, color);
```
**Parameters**

| Name      | Type          | Description      |
|-----------|---------------|------------------|
| fileIds   | Array         | File IDs Array   |
| originIds | Array         | Origin IDs Array |
| color     | VIZCore.Color | Color            |
</procedure>

## SetRGB
<procedure title="개체 색상 변경" collapsible="true">
<note>SetRGB(ids, color)</note>



**Example**
```Javascript
let nodeID = 2000;      //nodeID
let bodyID = 3000;      //bodyID
let ids = [nodeID , bodyID];        //Array<Number>
let color = new VIZCore.Color(255, 125, 0, 255);    //R, G, B, A
//개체 색상 변경
vizcore.Object3D.Color.SetRGB(ids, color);
```
**Parameters**

| Name  | Type            | Description   |
|-------|-----------------|---------------|
| ids   | `Array<Number>` | Node ID Array |
| color | VIZCore.Color   | Color         |
</procedure>


