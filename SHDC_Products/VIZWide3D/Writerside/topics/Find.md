# Find

## GetNodeByName
<procedure title="노드 이름에 해당하는 노드 반환" collapsible="true">
<note>GetNodeByName(keyword, fullMatch) → {Array}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//노드 색상 변경
vizcore.Object3D.Color.SetColorByNode(nodes, new VIZCore.Color(255, 125, 0, 255));
```
**Parameters**

| Name      | Type    | Description                     |
|-----------|---------|---------------------------------|
| keyword   | String  | 검색어                             |
| fullMatch | Boolean | 검색어 일치 여부 - True(일치), False(포함) |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | Node Array  |
</procedure>

## GetNodeByNames
<procedure title="노드 이름에 해당하는 노드 반환" collapsible="true">
<note>GetNodeByNames(keyword, fullMatch) → {Array}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByNames(     //Array
    ['PIPE101','PIPE101']   // Keyword
    , true      // Full Match
);
//노드 색상 변경
vizcore.Object3D.Color.SetColorByNode(nodes, new VIZCore.Color(255, 125, 0, 255));
```
**Parameters**

| Name      | Type    | Description                     |
|-----------|---------|---------------------------------|
| keyword   | Array   | 검색어                             |
| fullMatch | Boolean | 검색어 일치 여부 - True(일치), False(포함) |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | Node Array  |
</procedure>

## GetNodeMapByNames
<procedure title="노드 이름에 해당하는 노드맵 반환" collapsible="true">
<note>GetNodeMapByNames(keyword, fullMatch, importChild, importChild) → {Map}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드맵 반환
let nodes = vizcore.Object3D.Find.GetNodeMapByNames(
    ['PIPE101'], true, true, true 
);
```
**Parameters**

| Name        | Type    | Description                                   |
|-------------|---------|-----------------------------------------------|
| keyword     | Array   | 검색어                                           |
| fullMatch   | Boolean | 검색어 일치 여부 - True(일치), False(포함)               |
| importChild | Boolean | 하위 노드 포함 여부 - True(포함), False(포함하지 않음)        |
| importChild | Boolean | 검색 대상이 아닌 노드 포함 여부 - True(포함), False(포함하지 않음) |

**Returns**

| Type | Description |
|------|-------------|
| Map  | Node map    |
</procedure>

## QuickSearch
<procedure title="노드 이름에 해당하는 노드 반환" collapsible="true">
<note>QuickSearch(keyword, fullMatch) → {Array}</note>

**Example**
```Javascript
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.QuickSearch(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//노드 색상 변경
vizcore.Object3D.Color.SetColorByNode(nodes, new VIZCore.Color(255, 125, 0, 255));
```
**Parameters**

| Name      | Type    | Description                     |
|-----------|---------|---------------------------------|
| keyword   | String  | 검색어                             |
| fullMatch | Boolean | 검색어 일치 여부 - True(일치), False(포함) |

**Returns**

| Type  | Description |
|-------|-------------|
| Array | Node Array  |
</procedure>