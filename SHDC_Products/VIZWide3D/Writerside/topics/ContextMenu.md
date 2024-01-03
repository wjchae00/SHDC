# ContextMenu

## ContextMenu 생성

<procedure title="ContextMenu 생성">
<note>new ContextMenu(view, vizcore)</note>

**Example**
```Javascript
//ContextMenu 생성
let createContextMenu = new vizcore.ContextMenu(view, vizcore);     
```
**Parameters** 

| Name    | Type   | Description   |
|---------|--------|---------------|
| view    | Object | HTML Element  |
| vizcore | Object | Core Instance |

</procedure>

## AddContextMenu

<procedure title="ContextMenu 추가" collapsible="true">
<note>AddContextMenu(item)</note>

**Example**
```Javascript
let createContextMenu = new vizcore.ContextMenu(view, vizcore);     //ContextMenu 생성

let subcallback = function()
{
// 서브 메뉴 콜백 함수
};

let subcontextmenu = createContextMenu.GetContextMenuObj();     //ContextMenu object
subcontextmenu.id = "subcontextmenu";                           //subnotextmenu id
subcontextmenu.callback = subcallback;                          //subnotextmenu callback
subcontextmenu.text = "Sub";                                    //subnotextmenu text

let callback = function()
{
// 메뉴 콜백 함수
};

let contextmenu = createContextMenu.GetContextMenuObj();        //ContextMenu object
contextmenu.id = "contextmenu";         //contextmenu id
contextmenu.subContextMenu = [subcontextmenu];      //contextmenu subContextMenu
contextmenu.callback = callback;        //contextmenu callback
contextmenu.text = "Main";              //contextmenu text

createContextMenu.AddContextMenu([contextmenu]);        //ContextMenu 추가
```
**Parameters**

| Name | Type  | Description        |
|------|-------|--------------------|
| item | Array | ContextMenu object |

</procedure>

## GetContextMenuObj
<procedure title="ContextMenu object 정보 반환" collapsible="true">
<note>GetContextMenuObj(id, callback, subButton)</note>

**Example**
```Javascript
let createContextMenu = new vizcore.ContextMenu(view, vizcore);     //ContextMenu 생성

let callback = function()
{
    // 메뉴 콜백 함수 
};

let contextmenu = createContextMenu.GetContextMenuObj();        //ContextMenu object
contextmenu.id = "contextmenu";         //contextmenu id
contextmenu.callback = callback;        //contextmenu callback
contextmenu.text = "Main";              //contextmenu text

createContextMenu.AddContextMenu([contextmenu]);        //ContextMenu 추가
```
**Parameters**

| Name      | Type   | Description          |
|-----------|--------|----------------------|
| id        | String | ContextMenu id       |
| callback  | Object | ContextMenu callback |
| subButton | Array  | ContextMenu sub      |
</procedure>

## ShowContextMenu
<procedure title="ContextMenu 보이기/숨기기" collapsible="true">
<note>ShowContextMenu(id, show)</note>

**Example**
```Javascript
//ContextMenu object
let contextmenu = createContextMenu.GetContextMenuObj();
//ContextMenu 추가
createContextMenu.AddContextMenu([contextmenu]);
//ContextMenu 보이기/숨기기
createContextMenu.ShowContextMenu("contextmenu", false);
```
**Parameters**

| Name | Type    | Description       |
|------|---------|-------------------|
| id   | String  |  ContextMenu id   |
| show | Boolean |  ContextMenu show |
</procedure>