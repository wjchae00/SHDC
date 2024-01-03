# Player

## Player 생성

<procedure title="Player 생성">
<note>new Player(element, view, VIZCore)</note>

**Example**
```Javascript
//Player 생성
let view = document.getElementById("view");
let player = new vizcore.Player(view, vizcore, VIZCore);
```
**Parameters**

| Name    | Type   | Description      |
|---------|--------|------------------|
| view    | Object | HTML Element     |
| vizcore | Object | Core Instance    |
| VIZCore | Object | VIZCore Instance |
</procedure>

## Show
<procedure title="Animation Player 보이기/숨기기" collapsible="true">
<note>Show(visible)</note>

**Example**
```Javascript
//Animation Player 보이기/숨기기
let player = new vizcore.Player(view, vizcore, VIZCore);
player.Show(true);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 패널 보이기/숨기기  |
</procedure>

## ShowPlayTime
<procedure title="Animation Play Date 보이기/숨기기" collapsible="true">
<note>ShowPlayTime(visible)</note>

**Example**
```Javascript
//Animation Play Date 보이기/숨기기
let player = new vizcore.Player(view, vizcore, VIZCore);
player.ShowPlayTime(false);
```
**Parameters**

| Name    | Type    | Description   |
|---------|---------|---------------|
| visible | Boolean | 재생 날짜 보이기/숨기기 |
</procedure>