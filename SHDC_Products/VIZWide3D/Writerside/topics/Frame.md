# Frame

## AddGridLine
<procedure title="Frame 추가" collapsible="true">

<note>AddGridLine(axis, gridId, offset)</note>

**Example**
```Javascript
vizcore.Frame.AddGridLine(              
    VIZCore.Enum.Axis.X             // X축 추가
    ,0                              // Grid Id
    ,0                              // 오프셋
);
```
**Parameters**

| Name   | Type              | Description |
|--------|-------------------|-------------|
| axis   | VIZCore.Enum.Axis | 축           |
| gridId | Number            | Grid Id     |
| offset | Number            | 오프셋         |
</procedure>

## AddGridLineCustom
<procedure title="Custom GridLine 추가" collapsible="true">
<note>AddGridLineCustom(axis, gridId, offset, label)</note>

**Example**
```Javascript
vizcore.Frame.AddGridLineCustom(
    VIZCore.Enum.Axis.Y             // Y축 추가             
    ,-1                             // Grid Id
    ,-1820                          // 오프셋
    ,'lb'                           // Custom Label                        
);
```
**Parameters**

| Name   | Type              | Description  |
|--------|-------------------|--------------|
| axis   | VIZCore.Enum.Axis | 축            |
| gridId | Number            | Grid Id      |
| offset | Number            | 오프셋          |
| label  | String            | Custom Label |
</procedure>

## Clear
<procedure title="Frame 초기화" collapsible="true">
<note>Clear()</note>

**Example**
```Javascript
//Frame 초기화
vizcore.Frame.Clear();
```
</procedure>

## ElevationLine
<procedure title="Elevation Line 조회" collapsible="true">
<note>ElevationLine(visible)</note>

**Example**
```Javascript
//Elevation Line 조회
vizcore.Frame.ElevationLine(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |  
</procedure>

## GetGridItem
<procedure title="지정 축의 그리드 리스트 반환" collapsible="true">
<note>GetGridItem(nAxis) → {Object}</note>

**Example**
```Javascript
//지정 축의 그리드 리스트 반환
vizcore.Frame.GetGridItem(VIZCore.Enum.Axis.X);                   //X
vizcore.Frame.GetGridItem(VIZCore.Enum.Axis.Y);                   //Y
vizcore.Frame.GetGridItem(VIZCore.Enum.Axis.Z);                   //Z
```
**Parameters**

| Name  | Type              | Description |
|-------|-------------------|-------------|
| nAxis | VIZCore.Enum.Axis | 축           |

**Returns**

| Type   | Description |
|--------|-------------|
| Object | 그리드 리스트     |
</procedure>
 

## GetSnapItem
<procedure title="지정 위치에서 가장 가까운 그리드 정보 반환" collapsible="true">
<note>GetSnapItem(nAxis, point) → {Object}</note>

**Example**
```Javascript
//지정 위치에서 가장 가까운 그리드 정보 반환
vizcore.Frame.GetSnapItem(VIZCore.Enum.Axis.X,1);                   //X
vizcore.Frame.GetSnapItem(VIZCore.Enum.Axis.Y,0);                   //Y
vizcore.Frame.GetSnapItem(VIZCore.Enum.Axis.Z,-1);                  //Z
```
**Parameters**

| Name  | Type              | Description |
|-------|-------------------|-------------|
| nAxis | VIZCore.Enum.Axis | 축           |
| point | Number            | 좌표          |

**Returns**

| Type   | Description               |
|--------|---------------------------|
| Object | 그리드 반환 (찾기 실패시 undefined) |   
</procedure>

## OpenString
<procedure title="Frame(SHIP GRID) String 열기" collapsible="true">
<note>OpenString(str)</note>

**Example**
```Javascript
let str = "[{\"axis\":\"X\",\"axisId\":0,\"label\":\"FR\",\"items\":[{\"id\":0,\"offset\":8500},{\"id\":1,\"offset\":10000}]},{\"axis\":\"Y\",\"axisId\":1,\"label\":\"LP\",\"items\":[{\"id\":0,\"offset\":10000},{\"id\":0,\"offset\":20000}]},{\"axis\":\"Z\",\"axisId\":2,\"label\":\"LP\",\"items\":[{\"id\":0,\"offset\":2680},{\"id\":1,\"offset\":5000}]}]"

//Frame(SHIP GRID) String 열기
vizcore.Frame.OpenString(str);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| str  | String | String 열기   |
</procedure>

## OpenUri
<procedure title="Frame(SHIP GRID) URI 열기" collapsible="true">
<note>OpenUri(uri)</note>

**Example**
```Javascript
let uri = 'http://127.0.0.1/VIZCore/Model/ShipGrid/8222.json';

//Frame(SHIP GRID) URI 열기
vizcore.Frame.OpenUri(uri);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| uri  | String | URI 열기      |
</procedure>

## PlanLine
<procedure title="Plan Line 조회" collapsible="true">
<note>PlanLine(visible)</note>

**Example**
```Javascript
//Plan Line 조회
vizcore.Frame.PlanLine(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## SectionLine
<procedure title="Section Line 조회" collapsible="true">
<note>SectionLine(visible)</note>

**Example**
```Javascript
//Section Line 조회
vizcore.Frame.SectionLine(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ShowEvenNumber
<procedure title="짝수번째 표시" collapsible="true">
<note>ShowEvenNumber(visible)</note>

**Example**
```Javascript
//짝수번째 표시
vizcore.Frame.ShowEvenNumber(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ShowLevelGrid
<procedure title="레벨 그리드 활성화" collapsible="true">
<note>ShowLevelGrid(visible)</note>

**Example**
```Javascript
//레벨 그리드 활성화
vizcore.Frame.ShowLevelGrid(true);
```

**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ShowNumber
<procedure title="Show Number" collapsible="true">
<note>ShowNumber(visible)</note>

**Example**
```Javascript
//Show Number
vizcore.Frame.ShowNumber(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ShowNumberAllStep
<procedure title="화면 비율에 따라 Frame 번호 일부 조회" collapsible="true">
<note>ShowNumberAllStep(visible)</note>

**Example**
```Javascript
//자동 숨김(전체 Frame Number 보이기/숨기기), 기본값은 False
vizcore.Frame.ShowNumberAllStep(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ShowOddNumber
<procedure title="홀수번째 표시" collapsible="true">
<note>ShowOddNumber(visible)</note>

**Example**
```Javascript
//홀수번째 표시
vizcore.Frame.ShowOddNumber(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## XYPlane
<procedure title="XY Plane 조회" collapsible="true"> 
<note>XYPlane(visible)</note>

**Example**
```Javascript
//XY Plane 조회
vizcore.Frame.XYPlane(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## YZPlane
<procedure title="YZ Plane 조회" collapsible="true">
<note>YZPlane(visible)</note>

**Example**
```Javascript
//YZ Plane 조회
vizcore.Frame.YZPlane(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>

## ZXPlane
<procedure title="ZX Plane 조회" collapsible="true">
<note>ZXPlane(visible)</note>

**Example**
```Javascript
//ZX Plane 조회
vizcore.Frame.ZXPlane(false);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기 / 숨기기   |
</procedure>