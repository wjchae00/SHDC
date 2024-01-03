# Xray

## Enable
<procedure title="Xray 모드 활성화/비활성화" collapsible="true">
<note>Enable(enable)</note>

**Example**
```Javascript
//Xray 모드 활성화/비활성화
vizcore.View.Xray.Enable(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 활성화/비활성화    |
</procedure>

## Select
<procedure title="Xray 모드 지정 모델 선택 및 색상 표현" collapsible="true">
<note>Select(ids, selection)</note>

**Example**
```Javascript
let nodes = vizcore.Object3D.Find.GetNodeByName(
'배관_지하매설물.nwd'   // Keyword
, true      // Full Match
);

let bodies = vizcore.Object3D.GetBodiesByNode(nodes);

let ids = [];
for (let i = 0; i < bodies.length; i++) {
ids.push(bodies[i].bodyId);
}
vizcore.View.Xray.Select(ids, true);
```
**Parameters**

| Name      | Type    | Description      |
|-----------|---------|------------------|
| ids       | Array   | Body ID 목록       |
| selection | boolean | 선택 가능 여부 및 색상 표현 |
</procedure>