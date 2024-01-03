# Model

## Add
<procedure title="복수개의 VIZWeb3D 용 VIZW 모델 파일 추가" collapsible="true">
<note>Add(models)</note>

**Example**
```Javascript
let models = [];                //URI Array
models.push("./VIZCore/Model/Sample1.vizw");
models.push("./VIZCore/Model/Sample2.vizw");
//복수개의 VIZWeb3D 용 VIZW 모델 파일 추가
vizcore.Model.Add(models);
```
**Parameters**

| Name   | Type  | Description |
|--------|-------|-------------|
| models | Array | URI Array   |
</procedure>

## AddHeader
<procedure title="VIZWide3D 용 VIZW 파일의 헤더 추가" collapsible="true">
<note>AddHeader(models)</note>

**Example**
```Javascript
function example1 () {
//모델 닫기
vizcore.Model.Close();

     let models = [];                       //URI Array
     models.push("./VIZCore/Model/Sample1_wh.vizw");
     models.push("./VIZCore/Model/Sample2_wh.vizw");
     models.push("./VIZCore/Model/Sample3_wh.vizw");
     models.push("./VIZCore/Model/Sample4_wh.vizw");
//VIZWide3D 용 VIZW 파일의 헤더 추가
     vizcore.Model.AddHeader(models);
}

//AddHeader Model Key example
function example2 () {
//모델 닫기
     vizcore.Model.Close();
// 파일 로딩 완료 시점 확인
     function onLoadModelSample1(key, loadType) {
// 구조정보 로딩 완료
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.STRUCTURE)
             console.log("onLoad Structure");
//속성정보 로딩 완료            
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.PROPERTY)
             console.log("onLoad Property");
//MATERIAL정보 로딩 완료
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.MATERIAL)
             console.log("onLoad Material");
//모델정보 로딩 완료          
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.MESH)
             console.log("onLoad Mesh");
     }

     let models = [];                        //URI Array
     models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1", onload : onLoadModelSample1});
     models.push({url:"./VIZCore/Model/Sample2_wh.vizw", key:"sample2"});
     models.push({url:"./VIZCore/Model/Sample3_wh.vizw", key:"sample3"});
     models.push({url:"./VIZCore/Model/Sample4_wh.vizw", key:"sample4"});
//VIZWide3D 용 VIZW 파일의 헤더 추가
     vizcore.Model.AddHeader(models);
}
```
**Parameters**

| Name   | Type  | Description |
|--------|-------|-------------|
| models | Array | URI Array   |
</procedure>

## Close
<procedure title="모델 닫기" collapsible="true">
<note>Close()</note>

**Example**
```Javascript
//모델 닫기
vizcore.Model.Close();
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw");
```
</procedure>

## CloseFile
<procedure title="특정 모델 닫기" collapsible="true">
<note>CloseFile(fileKeys)</note>

**Example**
```Javascript
let models = [];                         //URI Array
models.push({url:"./VIZCore/Model/Sample1_wh.vizw", key:"sample1"});
models.push({url:"./VIZCore/Model/Sample2_wh.vizw", key:"sample2"});
models.push({url:"./VIZCore/Model/Sample3_wh.vizw", key:"sample3"});
//VIZWide3D 용 VIZW 파일의 헤더 추가
vizcore.Model.AddHeader(models);

let fileKeys = ["sample1", "sample2"];          //Array<String>

//특정 모델 닫기
vizcore.Model.CloseFile(fileKeys);
```
**Parameters**

| Name     | Type            | Description |
|----------|-----------------|-------------|
| fileKeys | `Array<String>` | File Key    |
</procedure>

## GetBoundBox
<procedure title="로딩된 모델의 BoundBox 반환" collapsible="true">
<note>GetBoundBox() → {VIZCore.BBox}</note>

**Example**
```Javascript
//로딩된 모델의 BoundBox 반환
vizcore.Model.GetBoundBox();
```
**Returns**

| Type         | Description |
|--------------|-------------|
| VIZCore.BBox | BoundBox    |
</procedure>

## GetOpenFiles
<procedure title="파일 목록 반환" collapsible="true">
<note>GetOpenFiles() → {Array}</note>

**Example**
```Javascript
//파일 목록 반환
let files = vizcore.Model.GetOpenFiles();
console.log(files);
```
**Returns**

| Type  | Description    |
|-------|----------------|
| Array | Open File Keys |
</procedure>

## Open
<procedure title="단일 VIZWeb3D 용 VIZW 모델 파일 열기" collapsible="true">
<note>Open(model)</note>

**Example**
```Javascript
//모델 닫기
vizcore.Model.Close();
//단일 VIZWeb3D 용 VIZW 모델 파일 열기
vizcore.Model.Open("./VIZCore/Model/Sample.vizw");
```
**Parameters**

| Name  | Type   | Description |
|-------|--------|-------------|
| model | string | URI String  |
</procedure>

## OpenHeader
<procedure title="단일 VIZWide3D 용 VIZW 파일의 헤더 열기" collapsible="true">
<note>OpenHeader(model, key, onLoad)</note>

**Example**
```Javascript
// 파일 로딩 완료 시점 확인
function onLoadModelSample1(key, loadType) {
//HEADER정보 로딩 완료
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.HEADER)
                console.log("onLoad Header");
//구조정보 로딩 완료
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.STRUCTURE)
             console.log("onLoad Structure");
//속성정보 로딩 완료            
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.PROPERTY)
             console.log("onLoad Property");
//MATERIAL정보 로딩 완료
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.MATERIAL)
             console.log("onLoad Material");
//모델정보 로딩 완료          
         if(loadType === VIZCore.Enum.CONFIG_KEY.LOADER.COMPLETEDTIME.MESH)
             console.log("onLoad Mesh");
}
    
//모델 닫기
vizcore.Model.Close();
//단일 VIZWide3D 용 VIZW 파일의 헤더 열기
vizcore.Model.OpenHeader("./VIZCore/Model/Sample_wh.vizw", "FileID123", onLoadModelSample1);
```
**Parameters**

| Name   | Type     | Description                                            |
|--------|----------|--------------------------------------------------------|
| model  | String   | URI                                                    |
| key    | String   | File Key(지정하지 않으면 Guid 생성)                             |
| onLoad | function | 개별 다운로드 이벤트 (Key) - 지정하지 않는 경우 OnModelOpenedEvent() 호출 |
</procedure>

## --- Event Listener ---

## OnModelOpenedEvent
<procedure title="모델 열기 이벤트 등록" collapsible="true">
<note>OnModelOpenedEvent(listener)</note>

**Example**
```Javascript
// Event : OnModelOpenedEvent
let OnModelOpenedEvent = function (event) {
    // Enable Xray
    vizcore.View.Xray.Enable(true);
}

// Add Event Handler : Loading Completed Event (로딩 완료 이벤트)
vizcore.Model.OnModelOpenedEvent(OnModelOpenedEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnPropertyCompletedEvent
<procedure title="속성정보 로딩 완료 이벤트 등록" collapsible="true">
<note>OnPropertyCompletedEvent(listener)</note>

**Example**
```Javascript
// Event : OnPropertyCompletedEvent
let OnPropertyCompletedEvent = function (event) {
    console.log(event);
}

// Add Event Handler : Property Completed Event (구조정보 로딩 완료 이벤트)
vizcore.Model.OnPropertyCompletedEvent(OnPropertyCompletedEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnStreamProgressChangedEvent
<procedure title="모델 로딩 프로그레스 이벤트 등록" collapsible="true">
<note>OnStreamProgressChangedEvent(listener)</note>

**Example**
```Javascript
// Event :: OnProgressEvent
let OnProgressEvent = function (event) {
    console.log("Total : ",  event.data.total, "Current : ", event.data.current, "Percentage : ", event.data.percentage);
}

// Add Event Handler : Progress Event (로딩 이벤트)
vizcore.Model.OnStreamProgressChangedEvent(OnProgressEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnStructureCompletedEvent
<procedure title="구조정보 로딩 완료 이벤트 등록" collapsible="true">
<note>OnStructureCompletedEvent(listener)</note>

**Example**
```Javascript
// Event :: OnStructureCompletedEvent
let OnStructureCompletedEvent = function (event) {
    console.log(event);
}

// Add Event Handler : Structure Completed Event (구조정보 로딩 완료 이벤트)
vizcore.Model.OnStructureCompletedEvent(OnStructureCompletedEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>