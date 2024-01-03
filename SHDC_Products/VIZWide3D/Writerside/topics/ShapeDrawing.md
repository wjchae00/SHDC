# ShapeDrawing

## AddBox
<procedure title="Box 생성" collapsible="true">
<note>AddBox(v1, v2, color) → {Number}</note>

**Example**
```Javascript
function exampleAddBox() {
    let v1 = new VIZCore.Vector3();                                     //min 좌표
    let v2 = new VIZCore.Vector3(10.0, 0.0, 0.0);                       //max 좌표
    let color = new VIZCore.Color(255, 255, 0, 255);                    //R, G, B, A
    //Box 생성
    let itemID = vizcore.ShapeDrawing.AddBox(v1, v2, color);
}
```
**Parameters**

| Name  | Type            | Description |
|-------|-----------------|-------------|
| v1    | VIZCore.Vector3 | min 좌표      |
| v2    | VIZCore.Vector3 | max 좌표      |
| color | VIZCore.Color   | Color       |

**Returns**

| Type   | Description |
|--------|-------------|
| Number | ID          |

</procedure>

## AddBoxByBox
<procedure title="Box 생성" collapsible="true">
<note>AddBoxByBox(bbox, color) → {Number}</note>

**Example**
```Javascript
function exampleAddBoxByBox() {
    //Box 생성
    let bbox = new VIZCore.BBox();
    let color = new VIZCore.Color(255, 255, 0, 255);
    let itemID = vizcore.ShapeDrawing.AddBoxByBox(bbox, color);
}
```
**Parameters**

| Name  | Type          | Description |
|-------|---------------|-------------|
| bbox  | 	VIZCore.BBox | boundbox    |
| color | VIZCore.Color | Color       |

**Returns**

| Type   | Description |
|--------|-------------|
| Number | ID          |

</procedure>

## AddCylinder
<procedure title="Cylinder 생성" collapsible="true">
<note>AddCylinder(v1, v2, radius, color) → {Number}</note>

**Example**
```Javascript
function exampleAddCylinder() {
    let v1 = new VIZCore.Vector3();                                          //좌표1
    let v2 = new VIZCore.Vector3(10.0, 0.0, 0.0);                            //좌표2
    let fRadius = 5.0;                                                       //Cylinder Radius
    let color = new VIZCore.Color(255, 255, 0, 255);                         //R, G, B, A
    //Cylinder 생성
    let itemID = vizcore.ShapeDrawing.AddCylinder(v1, v2, fRadius, color);
}
```
**Parameters**

| Name   | Type            | Description     |
|--------|-----------------|-----------------|
| v1     | VIZCore.Vector3 | 좌표1             |
| v2     | VIZCore.Vector3 | 좌표2             |
| radius | Number          | Cylinder Radius |
| color  | VIZCore.Color   | Color           |

**Returns**

| Type   | Description |
|--------|-------------|
| Number | ID          |
</procedure>

## AddPanel
<procedure title="평판 생성" collapsible="true">
<note>AddPanel(center, normal, width, length, color) → {Number}</note>

**Example**
```Javascript
function exampleAddPanel() {
    let center = new VIZCore.Vector3(0.0, 10.0, 0.0);                                     //중심 위치
    let normal = new VIZCore.Vector3(10.0, 0.0, 0.0);                       //방향
    let width = 5;
    let length = 1;
    let color = new VIZCore.Color(255, 255, 0, 255);                    //R, G, B, A
    //Panel 생성
    let itemID = vizcore.ShapeDrawing.AddPanel(center, normal, width, length, color);
}
```
**Parameters**

| Name   | Type            | Description |
|--------|-----------------|-------------|
| center | VIZCore.Vector3 | 중심 위치       |
| normal | VIZCore.Vector3 | 방향          |
| width  | float           | 너비          |
| length | float           | 길이          |
| color  | VIZCore.Color   | Color       |

**Returns**

| Type   | Description |
|--------|-------------|
| Number | ID          |

</procedure>

## Clear
<procedure title="개체 전체 삭제" collapsible="true">
<note>Clear()</note>

**Example**
```Javascript
//개체 전체 삭제
vizcore.ShapeDrawing.Clear();
```
</procedure>

## Delete
<procedure title="개체 삭제" collapsible="true">
<note>Delete(itemID)</note>

**Example**
```Javascript
//Box 생성
let bbox = new VIZCore.BBox();
let color = new VIZCore.Color(255, 255, 0, 255);
let itemID = vizcore.ShapeDrawing.AddBoxByBox(bbox, color);
//개체 삭제
vizcore.ShapeDrawing.Delete(itemID);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| itemID | Number | 개체 ID       |
</procedure>

## EnableUseSelection
<procedure title="개체 선택 가능 설정" collapsible="true">
<note>EnableUseSelection(itemID, enable)</note>

**Example**
```Javascript
//Box 생성
let bbox = new VIZCore.BBox();
let color = new VIZCore.Color(255, 255, 0, 255);
let itemID = vizcore.ShapeDrawing.AddBoxByBox(bbox, color);
//개체 선택 가능 설정
vizcore.ShapeDrawing.EnableUseSelection([itemID], false);
```
**Parameters**

| Name   | Type    | Description                        |
|--------|---------|------------------------------------|
| itemID | Array   | 개체 ID                              |
| enable | Boolean | 선택 가능여부 (true = 선택가능, false = 불가능) |
</procedure>

## Select
<procedure title="개체 선택" collapsible="true">
<note>Select(itemID, selection)</note>

**Example**
```Javascript
//Box 생성
let bbox = new VIZCore.BBox();
let color = new VIZCore.Color(255, 255, 0, 255);
let itemID = vizcore.ShapeDrawing.AddBoxByBox(bbox, color);
//개체 선택
vizcore.ShapeDrawing.Select([itemID], true);
```
**Parameters**

| Name      | Type    | Description |
|-----------|---------|-------------|
| itemID    | Array   | 개체 ID       |
| selection | Boolean | 선택          |
</procedure>

## Show
<procedure title="개체 보이기/숨기기" collapsible="true">
<note>Show(itemID, visible)</note>

**Example**
```Javascript
//Box 생성
let bbox = new VIZCore.BBox();
let color = new VIZCore.Color(255, 255, 0, 255);
let itemID = vizcore.ShapeDrawing.AddBoxByBox(bbox, color);
//개체 보이기/숨기기
vizcore.ShapeDrawing.Show([itemID], false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| itemID  | Array   | 개체 ID       |
| visible | Boolean | 보이기/숨기기     |
</procedure>