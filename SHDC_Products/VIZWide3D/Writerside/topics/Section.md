# Section

## Clear
<procedure title="단면 전체 삭제" collapsible="true">
<note>Clear()</note>

**Example**
```Javascript
//단면 전체 삭제
vizcore.Section.Clear();
```
</procedure>

## Create
<procedure title="단면 생성" collapsible="true">
<note>Create(clippingType) → {Object}</note>

**Example**
```Javascript
//X축 단면 생성
vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.X);
//Y축 단면 생성
vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.Y);
//Z축 단면 생성
vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.Z);
//BOX 단면 생성
vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.BOX);
//SELECTBOX 단면 생성
vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.SELECTBOX);
```
**Parameters**

| Name         | Type                        | Description                 |
|--------------|-----------------------------|-----------------------------|
| clippingType | VIZCore.Enum.CLIPPING_MODES | VIZCore.Enum.CLIPPING_MODES |

**Returns**

| Type   | Description     |
|--------|-----------------|
| Object | Data.ClipItem() |

</procedure> 

## GetBoxSize
<procedure title="단면 상자 크기 반환" collapsible="true">
<note>GetBoxSize(id) → {VIZCore.BBox}</note>

**Example**
```Javascript
//BOX 단면 생성
let item = vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.BOX);
//단면 상자 크기 반환
let bbox = vizcore.Section.GetBoxSize(item.id);
```
**Parameters**

| Name | Type   | Description        |
|------|--------|--------------------|
| id   | Object | Data.ClipItem().id |

**Returns**

| Type         | Description   |
|--------------|---------------|
| VIZCore.BBox | bbox boundBox |

</procedure>

## GetClipping
<procedure title="활성화된 단면 ID 반환" collapsible="true">
<note>GetClipping() → {clippingId}</note>


**Example**
```Javascript
//활성화된 단면 ID 반환
let clipped = vizcore.Section.GetClipping();
```
**Returns**

| Type       | Description |
|------------|-------------|
| clippingId | 단면 ID       |

</procedure>

## GetShow
<procedure title="단면 보이기/숨기기 반환" collapsible="true">
<note>GetShow(id) → {boolean}</note>

**Example**
```Javascript
//BOX 단면 생성
let item = vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.BOX);
//단면 보이기/숨기기 반환
let show = vizcore.Section.GetShow(item.id);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | String | clipping ID |

**Returns**

| Type    | Description             |
|---------|-------------------------|
| boolean | true : 보이기, false : 숨기기 |
</procedure>

## Inverse
<procedure title="단면 방향 전환" collapsible="true">
<note>Inverse()</note>

**Example**
```Javascript
//단면 방향 전환
vizcore.Section.Inverse();
```
</procedure>

## IsClipping
<procedure title="단면 클리핑 상태 반환" collapsible="true">
<note>IsClipping() → {Boolean}</note>

**Example**
```Javascript
//단면 클리핑 상태 반환
let clipped = vizcore.Section.IsClipping();
```
**Returns**

| Type    | Description |
|---------|-------------|
| Boolean | 단면 클리핑 여부   |

</procedure> 

## SetBoxSize
<procedure title="단면 상자 크기 변경" collapsible="true">
<note>SetBoxSize(id, bbox)</note>

**Example**
```Javascript
//BOX 단면 생성
let item = vizcore.Section.Create(VIZCore.Enum.CLIPPING_MODES.BOX);
//bbox 설정
let bbox = new VIZCore.BBox();
bbox.min.set(-10, -10, -10);
bbox.max.set(10, 10, 10);
bbox.update();
단면 상자 크기 변경
vizcore.Section.SetBoxSize(item.id, bbox);
```
**Parameters**

| Name | Type         | Description        |
|------|--------------|--------------------|
| id   | Object       | Data.ClipItem().id |
| bbox | VIZCore.BBox | 변경할 boundBox       |
</procedure>

## SetShow
<procedure title="단면 보이기/숨기기 설정" collapsible="true">
<note>SetShow(id, show)</note>



**Example**
```Javascript
//단면 보이기/숨기기 설정
vizcore.Section.SetShow(10, true);
```
**Parameters**

| Name | Type    | Description             |
|------|---------|-------------------------|
| id   | String  | clipping ID             |
| show | boolean | true : 보이기, false : 숨기기 | 
</procedure>

## Show
<procedure title="활성화된 단면 보이기/숨기기 설정" collapsible="true">
<note>Show(show)</note>



**Example**
```Javascript
//활성화된 단면 보이기/숨기기 설정
vizcore.Section.Show(true);
```
**Parameters**

| Name | Type    | Description             |
|------|---------|-------------------------|
| show | boolean | true : 보이기, false : 숨기기 | 
</procedure>