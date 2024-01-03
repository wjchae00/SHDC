# Toolbar

## Toolbar 생성

<procedure title="Toolbar 생성">

<note>new Toolbar(view, vizcore, VIZCore)</note>

**Example**
```Javascript
//Toolbar 생성
let view = document.getElementById("view");
let createtoolbar = new vizcore.Toolbar(view, vizcore, VIZCore);
```
**Parameters**

| Name    | Type   | Description      |
|---------|--------|------------------|
| view    | Object | HTML Element     |
| vizcore | Object | Core Instance    |
| VIZCore | Object | VIZCore Instance |
</procedure>

## AddButton 

<procedure title="버튼 생성" collapsible="true">
<note>AddButton(item)</note>

**Example**
```Javascript
//Toolbar 생성
import { VIZCore } from "./VIZCore/VIZCore.js";
let view = document.getElementById("view");
let vizcore = new Core(view);
let createtoolbar = new createToolbar(view, vizcore, VIZCore);
//버튼 object
let button = createtoolbar.GetButtonObj();
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.subButton = [subButton];                     //button sub
button.callback = callback;                         //button callback
//버튼 생성
createtoolbar.AddButton([button]);
```
**Parameters**

| Name | Type  | Description    |
|------|-------|----------------|
| item | Array |  button object |
</procedure>


## AddSubButton
<procedure title="서브 버튼 추가" collapsible="true">
<note>AddSubButton(parentId, child)</note>

**Example**
```Javascript
//Toolbar 생성
import { VIZCore } from "./VIZCore/VIZCore.js";
let view = document.getElementById("view");
let vizcore = new Core(view);
let createtoolbar = new createToolbar(view, vizwide3d, VIZCore);
//버튼 object
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.subButton = [subButton];                     //button sub
button.callback = callback;                         //button callback
//버튼 생성
createtoolbar.AddButton([button]);
//버튼 object
let subbutton = createtoolbar.GetButtonObj();
subbutton.id = "button";                            //button id
subbutton.checked = true;                           //button checked
subbutton.callback = callback;                      //button callback
//서브 버튼 추가
createtoolbar.AddSubButton(button.id ,[subbutton]);
```
**Parameters**

| Name     | Type   | Description        |
|----------|--------|--------------------|
| parentId | String | 서브 버튼 추가할 부모 버튼 id |
| child    | Array  | subbutton array    |
</procedure>

## GetButtonObj
<procedure title="버튼 object" collapsible="true">
<note>GetButtonObj(id, imageSrc, backgroundColor, checked, callback, subButton, tooltip)</note>

**Example**
```Javascript
//Toolbar 생성
import { VIZCore } from "./VIZCore/VIZCore.js";
let view = document.getElementById("view");
let vizcore = new Core(view);
let createtoolbar = new vizwide3d.Toolbar(view, vizwide3d, VIZCore);
//버튼 object
let subbutton = createtoolbar.GetButtonObj();
subbutton.id = "subbutton";                         //button id
subbutton.checked = fasle;                          //button checked
subbutton.callback = subcallback;                   //button callback
//버튼 object
let button = createtoolbar.GetButtonObj();
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.subButton = [subButton];                     //button sub
button.callback = callback;                         //button callback
```
**Parameters**

| Name            | Type    | Description            |
|-----------------|---------|------------------------|
| id              | String  | button id              |
| imageSrc        | String  | button image           |
| backgroundColor | String  | button backgroundColor |
| checked         | Boolean | button checked         |
| callback        | Object  | button callback        |
| subButton       | Array   | button sub             |
| tooltip         | String  | button tooltip text    |
</procedure>

## SetCheckButton
<procedure title="Button Check" collapsible="true">
<note>SetCheckButton(id, check)</note>

**Example**
```Javascript
//버튼 object
let button = createtoolbar.GetButtonObj();
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.callback = callback;                         //button callback
//Button Check
createtoolbar.SetCheckButton(id, true);
```
**Parameters**

| Name  | Type    | Description    |
|-------|---------|----------------|
| id    | String  | button id      |
| check | Boolean | button checked |
</procedure>

## SetCheckButtonImg 
<procedure title="Button Check Image" collapsible="true">
<note>SetCheckButtonImg(id, check)</note>

**Example**
```Javascript
//버튼 object
let button = createtoolbar.GetButtonObj();
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.callback = callback;                         //button callback
//Button Check Image
createtoolbar.SetCheckButtonImg(id, true);
```
**Parameters**

| Name  | Type    | Description    |
|-------|---------|----------------|
| id    | String  | button id      |
| check | Boolean | button checked |
</procedure>

## Show 
<procedure title="Toolbar 보이기/숨기기" collapsible="true">
<note>Show(visible)</note>

**Example**
```Javascript
//Toolbar 생성
import { VIZCore } from "./VIZCore/VIZCore.js";
let view = document.getElementById("view");
let vizcore = new Core(view);
let createtoolbar = new vizwide3d.Toolbar(view, vizwide3d, VIZCore);
//Toolbar 보이기/숨기기
createtoolbar.Show(true);
```
**Parameters**

| Name    | Type    | Description       |
|---------|---------|-------------------|
| visible | Boolean | Toolbar show/hide |
</procedure>

## ShowButton
<procedure title="Button 보이기/ 숨기기" collapsible="true">
<note>ShowButton(id, show)</note>

**Example**
```Javascript
//버튼 object
let button = createtoolbar.GetButtonObj();
button.id = "button";                               //button id
button.checked = true;                              //button checked
button.callback = callback;                         //button callback
//Button 보이기/ 숨기기
createtoolbar.ShowButton(button.id, true);
// 기본 제공 버튼은 toolbar.Element 에서 확인 가능
console.log(createtoolbar.Element);
```
**Parameters**

| Name | Type    | Description |
|------|---------|-------------|
| id   | String  | button id   |
| show | boolean | button show |
</procedure>