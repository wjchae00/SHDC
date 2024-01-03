# GeometryUtility

## ShowOsnap
<procedure title="오스냅(Osnap) 기능 사용" collapsible="true">
<note>ShowOsnap(cbCallback, surface, vertex, line)</note>

**Example**
```Javascript
//Callback
let pickCallback = function(e) {
    console.log(e);
};
//오스냅(Osnap) 기능 사용
vizcore.GeometryUtility.ShowOsnap(pickCallback, true, false, false);
```
**Parameters**

| Name       | Type     | Description                   |
|------------|----------|-------------------------------|
| cbCallback | function | Callback                      |
| surface    | Boolean  | 면 선택 가능 여부 (좌표 및 normal 반환)   |
| vertex     | Boolean  | preselect 정점 가능 여부 (좌표 반환)    |
| line       | Boolean  | preselect 라인 가능 여부 (라인 좌표 반환) |
</procedure>

## ShowOsnapByOnlyModel
<procedure title="오스냅(Osnap) 기능 사용 (모델 개체만 선택 가능)" collapsible="true">
<note>ShowOsnapByOnlyModel(cbCallback, surface, vertex, line)</note>

**Example**
```Javascript
//Callback
let pickCallback = function(e) {
    console.log(e);
};
오스냅(Osnap) 기능 사용 (모델 개체만 선택 가능)
vizcore.GeometryUtility.ShowOsnapByOnlyModel(pickCallback, true, false, false);
```
**Parameters**

| Name       | Type     | Description                   |
|------------|----------|-------------------------------|
| cbCallback | function | Callback                      |
| surface    | Boolean  | 면 선택 가능 여부 (좌표 및 normal 반환)   |
| vertex     | Boolean  | preselect 정점 가능 여부 (좌표 반환)    |
| line       | Boolean  | preselect 라인 가능 여부 (라인 좌표 반환) |
</procedure>

## ShowOsnapByOnlyShapeDrawing
<procedure title="오스냅(Osnap) 기능 사용 (ShapeDrawing 개체만 선택 가능)" collapsible="true">
<note>ShowOsnapByOnlyShapeDrawing(cbCallback, surface, vertex, line)</note>

**Example**
```Javascript
//Callback
let pickCallback = function(e) {
    console.log(e);
};
//오스냅(Osnap) 기능 사용 (ShapeDrawing 개체만 선택 가능)
vizcore.GeometryUtility.ShowOsnapByOnlyShapeDrawing(pickCallback, true, false, false);
```
**Parameters**

| Name       | Type     | Description                   |
|------------|----------|-------------------------------|
| cbCallback | function | Callback                      |
| surface    | Boolean  | 면 선택 가능 여부 (좌표 및 normal 반환)   |
| vertex     | Boolean  | preselect 정점 가능 여부 (좌표 반환)    |
| line       | Boolean  | preselect 라인 가능 여부 (라인 좌표 반환) |
</procedure>