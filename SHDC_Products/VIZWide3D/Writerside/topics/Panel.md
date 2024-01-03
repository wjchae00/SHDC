# Panel

## Panel 생성
<procedure title="Panel 생성">
<note>new Panel(element)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
```
**Parameters**

| Name | Type   | Description  |
|------|--------|--------------|
| view | Object | HTML Element |
</procedure>

## EnableResize
<procedure title="Panel 사이즈 조절 활성화" collapsible="true">
<note>EnableResize(bool)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 사이즈 조절 활성화
panel.EnableResize(false);
```
**Parameters**

| Name | Type    | Description |
|------|---------|-------------|
| bool | Boolean | 활성화/비활성화    |
</procedure>

## SetBorderColor
<procedure title="Panel 배경 색상 설정" collapsible="true">
<note>SetBorderColor(color)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 배경 색상 설정
panel.SetBorderColor({ r : 255, g : 255, b : 255, a : 255});
```
**Parameters**

| Name  | Type   | Description                           |
|-------|--------|---------------------------------------|
| color | Object | { r : 255, g : 255, b : 255, a : 255} |
</procedure>

## SetBorderColorFromRGBA
<procedure title="Panel 배경 색상 설정" collapsible="true">
<note>SetBorderColorFromRGBA(R, G, B, A)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 배경 색상 설정
panel.SetBorderColorFromRGBA(255, 255, 255, 255);
```
**Parameters**

| Name | Type   | Description  |
|------|--------|--------------|
| R    | Number | Red(0~255)   |
| G    | Number | Green(0~255) |
| B    | Number | Blue(0~255)  |
| A    | Number | Alpha(0~255) |
</procedure>

## SetContent
<procedure title="Panel Content 설정" collapsible="true">
<note>SetContent(element)</note>

**Example**
```Javascript
//Panel Content 설정
let view = document.getElementById("view");
let element = document.createElement('input');
element.style.width = "150px";
element.style.height = "50px";
//Panel 생성
let panel = new vizcore.Panel(view);
panel.SetContent(element);
```
**Parameters**

| Name    | Type   | Description  |
|---------|--------|--------------|
| element | Object | HTML Element |
</procedure>

## SetContentBackgroundColor
<procedure title="Panel Content 배경 색상 설정" collapsible="true">
<note>SetContentBackgroundColor(color)</note>

**Example**
```Javascript
//Panel Content 배경 색상 설정
panel.SetContentBackgroundColor({ r : 255, g : 255, b : 255, a : 255});
```
**Parameters**

| Name  | Type   | Description                           |
|-------|--------|---------------------------------------|
| color | Object | { r : 255, g : 255, b : 255, a : 255} |
</procedure>

## SetContentBackgroundColorFormRGBA
<procedure title="Panel Content 색상 설정" collapsible="true">
<note>SetContentBackgroundColorFormRGBA(R, G, B, A)</note>

**Example**
```Javascript
//Panel Content 색상 설정
panel.SetContentBackgroundColorFormRGBA(255,255,255,255);
```
**Parameters**

| Name | Type   | Description  |
|------|--------|--------------|
| R    | Number | Red(0~255)   |
| G    | Number | Green(0~255) |
| B    | Number | Blue(0~255)  |
| A    | Number | Alpha(0~255) |
</procedure>

## SetHeaderContent
<procedure title="Panel Header Content 설정" collapsible="true">
<note>SetHeaderContent(element)</note>

**Example**
```Javascript
//Panel Header Content 설정
let view = document.getElementById("view");
let element = document.createElement('input');
element.style.width = "150px";
element.style.height = "50px";
//Panel 생성
let panel = new vizcore.Panel(view);
panel.SetHeaderContent(element);
```
**Parameters**

| Name    | Type   | Description  |
|---------|--------|--------------|
| element | Object | HTML Element |
</procedure>

## SetLocationLeft
<procedure title="Panel 위치 설정(Left)" collapsible="true">
<note>SetLocationLeft(offset)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 위치 설정(Left)
panel.SetLocationLeft(10);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| offset | Number | Left Offset |
</procedure>

## SetLocationTop
<procedure title="Panel 위치 설정(Top)" collapsible="true">
<note>SetLocationTop(offset)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 위치 설정(Top)
panel.SetLocationTop(10);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| offset | Number | Top Offset  |
</procedure>

## SetSize
<procedure title="Panel 크기 설정" collapsible="true">
<note>SetSize(width, height)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 크기 설정
panel.SetSize(200, 300);
```
**Parameters**

| Name   | Type   | Description |
|--------|--------|-------------|
| width  | Number | 넓이          |
| height | Number | 높이          |
</procedure>

## SetTitleBackgroundColor
<procedure title="Panel Title 배경 색상 설정" collapsible="true">
<note>SetTitleBackgroundColor(color)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel Title 배경 색상 설정
panel.SetTitleBackgroundColor({ r : 255, g : 255, b : 255, a : 255});
```
**Parameters**

| Name  | Type   | Description                           |
|-------|--------|---------------------------------------|
| color | Object | { r : 255, g : 255, b : 255, a : 255} |
</procedure>

## SetTitleBackgroundColorFormRGBA
<procedure title="Panel Title 색상 설정" collapsible="true">
<note>SetTitleBackgroundColorFormRGBA(R, G, B, A)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel Title 색상 설정
panel.SetTitleBackgroundColorFormRGBA(255,255,255,255);
```
**Parameters**

| Name | Type   | Description  |
|------|--------|--------------|
| R    | Number | Red(0~255)   |
| G    | Number | Green(0~255) |
| B    | Number | Blue(0~255)  |
| A    | Number | Alpha(0~255) |
</procedure>

## SetTitleText
<procedure title="Panel Title 설정" collapsible="true">
<note>SetTitleText(text)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel Title 설정
panel.SetTitleText("Title");
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| text | String | Title       |
</procedure>

## SetTitleTextColor
<procedure title="Panel Title 색상 설정" collapsible="true">
<note>SetTitleTextColor(color)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel Title 색상 설정
panel.SetTitleTextColor({ r : 255, g : 255, b : 255, a : 255});
```
**Parameters**

| Name  | Type   | Description                           |
|-------|--------|---------------------------------------|
| color | Object | { r : 255, g : 255, b : 255, a : 255} |
</procedure>

## SetTitleTextColorFormRGBA
<procedure title="Panel Title 색상 설정" collapsible="true">
<note>SetTitleTextColorFormRGBA(R, G, B, A)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel Title 색상 설정
panel.SetTitleTextColorFormRGBA(255,255,255,255);
```
**Parameters**

| Name | Type   | Description  |
|------|--------|--------------|
| R    | Number | Red(0~255)   |
| G    | Number | Green(0~255) |
| B    | Number | Blue(0~255)  |
| A    | Number | Alpha(0~255) |
</procedure>

## Show
<procedure title="Panel 보이기/숨기기" collapsible="true">
<note>Show(visible)</note>

**Example**
```Javascript
//Panel 생성
let view = document.getElementById("view");
let panel = new vizcore.Panel(view);
//Panel 보이기/숨기기
panel.Show(true);
```
**Parameters**

| Name    | Type    | Description |
|---------|---------|-------------|
| visible | Boolean | 보이기/숨기기     |
</procedure>

## --- Event Listener ---

## OnCloseButtonEvent
<procedure title="Panel X 버튼 이벤트" collapsible="true">
<note>OnCloseButtonEvent(cbClose)</note>

**Example**
```Javascript
// Event : OnCloseButtonEvent
let cbClose = function(){
    console.log('close');
};

// Add Event Handler :  Panel X 버튼 이벤트
panel.OnCloseButtonEvent(cbClose);
```
**Parameters**

| Name    | Type   | Description       |
|---------|--------|-------------------|
| cbClose | Object | callback Function |
</procedure>

## OnResizeEvent
<procedure title="Panel 크기 변경 이벤트" collapsible="true">
<note>OnResizeEvent(cbResize)</note>

**Example**
```Javascript
// Event : OnResizeEvent
let cbResize = function(){
    console.log('resize');
};

// Add Event Handler :  Panel 크기 변경 이벤트
panel.OnResizeEvent(cbResize);
```
**Parameters**

| Name     | Type   | Description       |
|----------|--------|-------------------|
| cbResize | Object | callback Function |
</procedure>