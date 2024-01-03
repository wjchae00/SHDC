# CustomEdge

## ClearAll
<procedure title="모두 초기화" collapsible="true">
<note>ClearAll()</note>

**Example**
```Javascript
//모두 초기화
vizcore.Object3D.CustomEdge.ClearAll();
```
</procedure>

## SetEdge
<procedure title="지정한 개체의 모델 모서리 설정" collapsible="true">
<note>SetEdge(ids, edge)</note>

**Example**
```Javascript
let ids = [9, 13];                                //Array<Number>
//지정한 개체의 모델 모서리 설정
vizcore.Object3D.CustomEdge.SetEdge(ids, true);
//지정한 개체의 모델 모서리 표시
vizcore.View.ShowModelObjectCustomEdge(true);
let color = new VIZCore.Color(255,0,0,255);                 //R, G, B, A
//지정한 개체의 모델 모서리 추가 표시 색상 설정
vizcore.View.SetModelObjectCustomEdgeColor(color);
```
**Parameters**

| Name | Type            | Description   |
|------|-----------------|---------------|
| ids  | `Array<Number>` | Node ID Array |
| edge | Boolean         | 모서리 표시        |
</procedure>

## SetEdgeByOrigin
<procedure title="지정한 개체의 모델 모서리 설정" collapsible="true">
<note>SetEdgeByOrigin(fileKey, originIds, edge)</note>

**Example**
```Javascript
let fileKey = "sample";                                         //File ID
let originIds = [10];                                           //Origin IDs Array
//지정한 개체의 모델 모서리 설정
vizcore.Object3D.CustomEdge.SetEdgeByOrigin(fileKey, originIds, true);
//지정한 개체의 모델 모서리 표시
vizcore.View.ShowModelObjectCustomEdge(true);
```
**Parameters**

| Name      | Type            | Description      |
|-----------|-----------------|------------------|
| fileKey   | String          | File ID          |
| originIds | `Array<Number>` | Origin IDs Array |
| edge      | Boolean         | 모서리 표시           |
</procedure>