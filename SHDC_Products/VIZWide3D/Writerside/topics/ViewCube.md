# ViewCube

## IsVisible
<procedure title="ViewCube 보이기 / 숨기기 상태 반환" collapsible="true">
<note>IsVisible() → {boolean}</note>

**Example**
```Javascript
//ViewCube 보이기 / 숨기기 상태 반환
if(vizcore.View.ViewCube.IsVisible() === true)
//ViewCube 보이기 / 숨기기
vizcore.View.ViewCube.Show(false);
```
**Returns**

| Type    | Description |
|---------|-------------|
| boolean | 보이기/숨기기 상태  |

</procedure> 

## SetOffset
<procedure title="ViewCube 오프셋 설정" collapsible="true">
<note>SetOffset(offset)</note>

**Example**
```Javascript
//ViewCube 오프셋 설정
vizcore.View.ViewCube.SetOffset(20);
vizcore.View.ViewCube.SetOffset(50); // Default
```
**Parameters**

| Name   | Type                            | Description    |
|--------|---------------------------------|----------------|
| offset | VIZCore.Enum.VIEWCUBE_POSITIONS | 오프셋 (기본값 : 50) |
</procedure>

## SetPosition
<procedure title="ViewCube 위치 및 오프셋 설정" collapsible="true">
<note>SetPosition(position, offset)</note>

**Example**
```Javascript
//ViewCube 위치 및 오프셋 설정
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.LEFT_TOP);       // 좌상단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.RIGHT_TOP);      // 우상단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.LEFT_BOTTOM);    // 좌하단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.RIGHT_BOTTOM);   // 우하단

vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.LEFT_TOP, 50);       // 좌상단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.RIGHT_TOP, 50);      // 우상단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.LEFT_BOTTOM, 50);    // 좌하단
vizcore.View.ViewCube.SetPosition(VIZCore.Enum.VIEWCUBE_POSITIONS.RIGHT_BOTTOM, 50);   // 우하단
```
**Parameters**

| Name     | Type                            | Description    |
|----------|---------------------------------|----------------|
| position | VIZCore.Enum.VIEWCUBE_POSITIONS | 위치             |
| offset   | VIZCore.Enum.VIEWCUBE_POSITIONS | 오프셋 (기본값 : 50) |
</procedure>

## Show
<procedure title="ViewCube 보이기 / 숨기기" collapsible="true">
<note>Show(visible)</note>

**Example**
```Javascript
//ViewCube 보이기 / 숨기기
vizcore.View.ViewCube.Show(true);
```
**Parameters**

| Name    | Type     | Description |
|---------|----------|-------------|
| visible | 	boolean | 보이기/숨기기     |
</procedure>