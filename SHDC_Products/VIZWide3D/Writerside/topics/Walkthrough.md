# Walkthrough

## Action
<procedure title="WalkThrough 이동 Key down, key press, Mouse down등의 이벤트 연동" collapsible="true">
<note>Action(state)</note>

**Example**
```Javascript
//WalkThrough 사용 설정
vizcore.View.Walkthrough.Enable(true);
// 앞으로 이동
vizcore.View.Walkthrough.Action(VIZCore.Enum.ACTION_STATE.FORWARD);
```
**Parameters**

| Name  | Type                       | Description        |
|-------|----------------------------|--------------------|
| state | 	VIZCore.Enum.ACTION_STATE | WalkThrough Action |
</procedure>

## Avatar
<procedure title="WalkThrough 아바타 사용 설정" collapsible="true">
<note>Avatar(enable)</note>

**Example**
```Javascript
//WalkThrough 사용 설정
vizcore.View.Walkthrough.Enable(true);
//WalkThrough 아바타 사용 설정
vizcore.View.Walkthrough.Avatar(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## Enable
<procedure title="WalkThrough 사용 설정" collapsible="true">
<note>Enable(enable)</note>

**Example**
```Javascript
//WalkThrough 사용 설정
vizcore.View.Walkthrough.Enable(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EndAction
<procedure title="WalkThrough 이동 종료 Key up, Mouse up등의 이벤트 연동" collapsible="true">
<note>EndAction(state)</note>

**Example**
```Javascript
// 앞으로 이동 종료
vizcore.View.Walkthrough.EndAction(VIZCore.Enum.ACTION_STATE.FORWARD);
```
**Parameters**

| Name  | Type                       | Description        |
|-------|----------------------------|--------------------|
| state | 	VIZCore.Enum.ACTION_STATE | WalkThrough Action |
</procedure>

## MoveAvatarPosition
<procedure title="WalkThrough 아바타 위치 설정" collapsible="true">
<note>MoveAvatarPosition(pos)</note>

**Example**
```Javascript
//WalkThrough 아바타 위치 설정
vizcore.View.Walkthrough.MoveAvatarPosition(new VIZCore.Vector3(83720,-9762,22561));
```
**Parameters**

| Name | Type            | Description |
|------|-----------------|-------------|
| pos  | VIZCore.Vector3 | 이동 위치       |
</procedure>