# Weather

## EnableCloud
<procedure title="환경 날씨 구름 활성화" collapsible="true">
<note>EnableCloud(enable)</note>

**Example**
```Javascript
//환경 날씨 구름 활성화
vizcore.View.Weather.EnableCloud(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 활성화/비활성화    |
</procedure>

## EnableRain
<procedure title="환경 날씨 비 활성화" collapsible="true">
<note>EnableRain(enable)</note>

**Example**
```Javascript
//환경 날씨 비 활성화
vizcore.View.Weather.EnableRain(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 활성화/비활성화    |
</procedure>

## EnableSnow
<procedure title="환경 날씨 눈 활성화" collapsible="true">
<note>EnableSnow(enable)</note>

**Example**
```Javascript
//환경 날씨 눈 활성화
vizcore.View.Weather.EnableSnow(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 활성화/비활성화    |
</procedure>

## GetCloudOpion
<procedure title="환경 날씨 구름 설정값 반환" collapsible="true">
<note>GetCloudOpion() → {object}</note>

**Example**
```Javascript
//환경 날씨 구름 설정값 반환
let opt = vizcore.View.Weather.GetCloudOpion();
```
**Returns**

| Type   | Description   |
|--------|---------------|
| object | 날씨 구름 설정 파라미터 |
</procedure>

## GetRainOpion
<procedure title="환경 날씨 비 설정값 반환" collapsible="true">
<note>GetRainOpion() → {object}</note>

**Example**
```Javascript
//환경 날씨 비 설정값 반환
let opt = vizcore.View.Weather.GetRainOpion();
```
**Returns**

| Type   | Description  |
|--------|--------------|
| object | 날씨 비 설정 파라미터 |
</procedure>
 

## GetSnowOpion
<procedure title="환경 날씨 눈 설정값 반환" collapsible="true">
<note>GetSnowOpion() → {object}</note>

**Example**
```Javascript
//환경 날씨 눈 설정값 반환
let opt = vizcore.View.Weather.GetSnowOpion();
```
**Returns**

| Type   | Description  |
|--------|--------------|
| object | 날씨 눈 설정 파라미터 |

</procedure>

## SetCloudDrawCount
<procedure title="환경 날씨 구름 그려지는 수 설정" collapsible="true">
<note>SetCloudDrawCount(count)</note>
 
**Example**
```Javascript
//환경 날씨 구름 그려지는 수 설정
vizcore.View.Weather.SetCloudDrawCount(3);
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| count | number | 구름 그려지는 수   |
</procedure>

## SetCloudOpion
<procedure title="환경 날씨 구름 설정값 적용" collapsible="true">
<note>SetCloudOpion(opt)</note>

**Example**
```Javascript
//환경 날씨 구름 설정값 반환
let opt = vizcore.View.Weather.GetCloudOpion();
//환경 날씨 구름 설정값 적용
vizcore.View.Weather.SetCloudOpion(opt);
```

**Parameters**

| Name | Type   | Description     |
|------|--------|-----------------|
| opt  | object | GetCloudOpion() |
</procedure>

## SetCloudTemplate
<procedure title="환경 날씨 구름 적용" collapsible="true">
<note>SetCloudTemplate(level)</note>

**Example**
```Javascript
//환경 날씨 구름 적용
vizcore.View.Weather.SetCloudTemplate(3);
```
**Parameters**

| Name  | Type   | Description                                                 |
|-------|--------|-------------------------------------------------------------|
| level | number | 0 ~ 4 (0 = 구름 없음, 1 = 조금, 2 = 보통, 3 = 많음, 4 = 흐린 구름 매우 많음 ) |
</procedure>

## SetMistTemplate
<procedure title="환경 날씨 안개 적용" collapsible="true">
<note>SetMistTemplate(level)</note>

**Example**
```Javascript
//환경 날씨 안개 적용
vizcore.View.Weather.SetMistTemplate(3);
```
**Parameters**

| Name  | Type   | Description                                        |
|-------|--------|----------------------------------------------------|
| level | number | 0 ~ 4 (0 = 없음, 1 = 연함, 2 = 보통, 3 = 짙음, 4 = 매우 짙음 ) |
</procedure>

## SetRainDrawCount
<procedure title="환경 날씨 비 그려지는 수 설정" collapsible="true">
<note>SetRainDrawCount(count)</note>

**Example**
```Javascript
//환경 날씨 비 그려지는 수 설정
vizcore.View.Weather.SetRainDrawCount(5);
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| count | number | 비 그려지는 수    |
</procedure>

## SetRainOpion
<procedure title="환경 날씨 비 설정값 적용" collapsible="true">
<note>SetRainOpion(opt)</note>

**Example**
```Javascript
//환경 날씨 비 설정값 반환
let opt = vizcore.View.Weather.GetRainOpion();
//환경 날씨 비 설정값 적용
vizcore.View.Weather.SetRainOpion(opt);
```

**Parameters**

| Name | Type   | Description    |
|------|--------|----------------|
| opt  | object | GetRainOpion() |
</procedure>

## SetRainTemplate
<procedure title="정의된 날씨(비) 적용" collapsible="true">
<note>SetRainTemplate(level)</note>

**Example**
```Javascript
//정의된 날씨(비) 적용
vizcore.View.Weather.SetRainTemplate(2);
```
**Parameters**

| Name  | Type   | Description                                        |
|-------|--------|----------------------------------------------------|
| level | number | 0 ~ 4 (0 = 맑음, 1 = 조금, 2 = 보통, 3 = 많음, 4 = 매우 많음 ) |
</procedure>

## SetRepeatRender
<procedure title="정의된 날씨 반복 재생" collapsible="true">
<note>SetRepeatRender(enable)</note>

**Example**
```Javascript
//정의된 날씨 반복 재생
vizcore.View.Weather.SetRepeatRender(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| enable | boolean | 활성화 / 비활성화  |
</procedure>

## SetSnowDrawArea
<procedure title="환경 날씨 눈 그려지는 영역 설정" collapsible="true">
<note>SetSnowDrawArea(bbox)</note>

**Example**
```Javascript
//모델 전체 BoundBox 반환
let bbox = vizcore.Object3D.GetBoundBox();
//환경 날씨 눈 그려지는 영역 설정
vizcore.View.Weather.SetSnowDrawArea(bbox);
```
**Parameters**

| Name | Type         | Description |
|------|--------------|-------------|
| bbox | VIZCore.BBox | 눈 그려지는 영역   |
</procedure>

## SetSnowDrawCount
<procedure title="환경 날씨 눈 그려지는 수 설정" collapsible="true">
<note>SetSnowDrawCount(count)</note>

**Example**
```Javascript
//환경 날씨 눈 그려지는 수 설정
vizcore.View.Weather.SetSnowDrawCount(4);
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| count | number | 눈 그려지는 수    |
</procedure>

## SetSnowOpion
<procedure title="환경 날씨 눈 설정값 적용" collapsible="true">
<note>SetSnowOpion(opt)</note>

**Example**
```Javascript
//환경 날씨 눈 설정값 반환
let opt = vizcore.View.Weather.GetSnowOpion();
//환경 날씨 눈 설정값 적용
vizcore.View.Weather.SetSnowOpion(opt);
```

**Parameters**

| Name | Type   | Description    |
|------|--------|----------------|
| opt  | object | GetSnowOpion() |
</procedure>

## SetSnowTemplate
<procedure title="정의된 날씨(눈) 적용" collapsible="true">
<note>SetSnowTemplate(level)</note>

**Example**
```Javascript
//정의된 날씨(눈) 적용
vizcore.View.Weather.SetSnowTemplate(4);
```
**Parameters**

| Name  | Type   | Description                                        |
|-------|--------|----------------------------------------------------|
| level | number | 0 ~ 4 (0 = 맑음, 1 = 조금, 2 = 보통, 3 = 많음, 4 = 매우 많음 ) |
</procedure>