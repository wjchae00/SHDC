# Control

## Disable
<procedure title="Control 초기화" collapsible="true">
<note>Disable(enable)</note>

**Example**
```Javascript
//Control 초기화
vizcore.View.Control.Disable(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnableCameraRotate
<procedure title="카메라(회전) 사용 설정" collapsible="true">
<note>EnableCameraRotate(enable)</note>

**Example**
```Javascript
//카메라(회전) 사용 설정
vizcore.View.Control.EnableCameraRotate(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnableClassicRotate
<procedure title="Orbit (회전) 사용 설정" collapsible="true">
<note>EnableClassicRotate(enable)</note>

**Example**
```Javascript
//Orbit (회전) 사용 설정
vizcore.View.Control.EnableClassicRotate(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnableFreeRotate
<procedure title="자유 궤도(회전) 사용 설정" collapsible="true">
<note>EnableFreeRotate(enable)</note>

**Example**
```Javascript
//자유 궤도(회전) 사용 설정
vizcore.View.Control.EnableFreeRotate(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnableLimitRotate
<procedure title="제한 궤도(회전) 사용 설정" collapsible="true">
<note>EnableLimitRotate(enable)</note>

**Example**
```Javascript
//제한 궤도(회전) 사용 설정
vizcore.View.Control.EnableLimitRotate(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnablePan
<procedure title="Pan 사용 설정" collapsible="true">
<note>EnablePan(enable)</note>

**Example**
```Javascript
//Pan 사용 설정
vizcore.View.Control.EnablePan(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## EnablePivotRotate
<procedure title="궤도(회전) 사용 설정 Z축 고정 회전" collapsible="true">
<note>EnablePivotRotate(enable)</note>

**Example**
```Javascript
//궤도(회전) 사용 설정 Z축 고정 회전
vizcore.View.Control.EnablePivotRotate(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## FixedZoomRatio
<procedure title="확대 비율 고정 설정" collapsible="true">
<note>FixedZoomRatio(enable)</note>

**Example**
```Javascript
//확대 비율 고정 설정
vizcore.View.Control.FixedZoomRatio(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 사용/미사용      |
</procedure>

## FixedZoomValue
<procedure title="확대 비율 고정 값 설정" collapsible="true">
<note>FixedZoomValue(value)</note>

**Example**
```Javascript
//확대 비율 고정 값 설정
vizcore.View.Control.FixedZoomValue(0.5);
```
**Parameters**

| Name  | Type   | Description             |
|-------|--------|-------------------------|
| value | Number | 0.0 ~ 1.0 : 낮을수록 느리게 반응 |
</procedure>

## RotateValue
<procedure title="회전 감도 설정" collapsible="true">
<note>RotateValue(value)</note>

**Example**
```Javascript
//회전 감도 설정
vizcore.View.Control.RotateValue(0.5);
```
**Parameters**

| Name  | Type   | Description             |
|-------|--------|-------------------------|
| value | Number | 0.0 ~ 1.0 : 낮을수록 느리게 반응 |
</procedure>