# Animation

## AddAnimationItem

<procedure title="애니메이션 추가" collapsible="true">

<note>AddAnimationItem(ids, startTime, duration, startColor, endColor)</note>

**Example**

```Javascript
// 애니메이션 시작일 지정
vizcore.Animation.SetStartDate(new Date(2022,7,9), 1);
//노드 이름에 해당하는 노드 반환
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);
//지정된 노드 하위 BodyID 목록 반환
let ids = vizcore.Object3D.GetBodyIdsByNode(nodes);

// 애니메이션 추가
vizcore.Animation.AddAnimationItem(
    ids                                                 // Body IDs(Array or Number)
    ,0                                                  // 시작 시간
    ,10                                                 // 재생 시간
    ,new VIZCore.Color(255,0,0,255)                     //시작 색상 (R, G, B, A)
    ,new VIZCore.Color(0,255,0,255)                    //종료 색상 (R, G, B, A)
);

// 애니메이션 시작
vizcore.Animation.Start();
```

**Parameters**

| Name        | Type           | Description               |
|-------------|----------------|---------------------------|
| ids         | Array          | Body IDs(Array or Number) |
| startTime   | Number         | 시작 시간                     |
| duration    | Number         | 재생 시간                     |
| startColor  | VIZCore.Color  | 시작 색상                     |
| endColor    | VIZCore.Color  | 종료 색상                     |

</procedure>

## AddNoteAnimation
<procedure title="노트 애니메이션 키 등록" collapsible="true">
<note>AddNoteAnimation(key)</note>

**Example**
```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

let text = [];
text.push('3D Note #1');
text.push('3D Note #2');

note.text.value = text;                             // Array
note.text.position = new VIZCore.Vector3(0, 0, 0);  // x, y, z
note.style.font.size = 10;                          // number
note.style.font.color.set(0, 56, 101, 255);          // R, G, B, A
note.style.border.type = 1;                          // 0 (Rectangle), 1(Rounded Rectangle)
note.style.border.color.set(41, 143, 194, 255);      // R, G, B, A
note.style.background.color.set(255, 255, 255, 200); // R, G, B, A

//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);

//노트 애니메이션 템플릿 등록
vizcore.Animation.AddNoteAnimation2DTemplate(
    "ANIMATION1"                     // Animation Key
    , [noteId]                        // Note ID Array
    , 1                              // Action Kind
    , 1000                           // Duration (ms.)
    , new VIZCore.Vector3(0.3, 0.1, 0.1) // 시작 위치 ( -1 ~ +1 )
    , new VIZCore.Vector3(0.1, 0.1, 0.1)   // 종료 위치 ( -1 ~ +1 )
);

//노트 애니메이션 키 등록
vizcore.Animation.AddNoteAnimation("ANIMATION1");

//노트 애니메이션 재생
vizcore.Animation.StartNoteAnimation();
```
**Parameters**

| Name | Type   | Description   |
|------|--------|---------------|
| key  | String | Animation Key |
</procedure>

## AddNoteAnimation2DTemplate
<procedure title="노트 애니메이션 템플릿 등록" collapsible="true">
<note>AddNoteAnimation2DTemplate(key, noteId, actionKind, duration, start, end)</note> 

**Example**

```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);

//노트 애니메이션 템플릿 등록
vizcore.Animation.AddNoteAnimation2DTemplate(
    "ANIMATION1"                     // Animation Key
    , [noteId]                        // Note ID Array
    , 1                              // Action Kind
    , 1000                           // Duration (ms.)
    , new VIZCore.Vector3(0.3, 0.1, 0.1) // 시작 위치 ( -1 ~ +1 )
    , new VIZCore.Vector3(0.1, 0.1, 0.1)   // 종료 위치 ( -1 ~ +1 )
);
```

**Parameters**

| Name       | Type            | Description     |
|------------|-----------------|-----------------|
| key        | String          | Animation Key   |
| noteId     | Array           | Note Id Array   |
| actionKind | Number          | Action Kind     |
| duration   | Number          | Duration        |
| start      | VIZCore.Vector3 | Start Position  |
| end        | VIZCore.Vector3 | End Position    |
</procedure>

## Clear
<procedure title="애니메이션 데이터 초기화(삭제)" collapsible="true">
<note>Clear()</note>

**Example**
```Javascript
//애니메이션 데이터 초기화
vizcore.Animation.Clear();
```
</procedure>

## ClearNoteAnimation
<procedure title="노트 애니메이션 초기화(삭제)" collapsible="true">
<note>ClearNoteAnimation()</note>

**Example**
```Javascript
//노트 애니메이션 초기화(삭제)
vizcore.Animation.ClearNoteAnimation();
```
</procedure>

## EnableEvent
<procedure title="애니메이션 이벤트 제어 활성화 시 이벤트 발생" collapsible="true">
<note>EnableEvent(enable)</note>

**Example**
```Javascript
//애니메이션 이벤트 제어 활성화 시 이벤트 발생
vizcore.Animation.EnableEvent(true);
```
**Parameters**

| Name    | Type      | Description |
|---------|-----------|-------------|
| enable  | Boolean   | 활성화/비활성화    |
</procedure>

## GetPlayTime
<procedure title="애니메이션 재생 시간 반환" collapsible="true">
<note>GetPlayTime() → {Number}</note>

**Example**
```Javascript
//애니메이션 재생 시간 반환
let time = vizcore.Animation.GetPlayTime();
```
**Returns**

| Type    | Description |
|---------|-------------|
| Number  | 재생 시간       |

</procedure>

## Init
<procedure title="애니메이션 초기화" collapsible="true">
<note>Init()</note>

**Example**
```Javascript
// 애니메이션 초기화
vizcore.Animation.Init();
```
</procedure>

## IsAnimationPlay
<procedure title="애니메이션 재생 상태 확인" collapsible="true">

<note>IsAnimationPlay() → {Boolean}</note>

**Example**
```Javascript
//애니메이션 재생 상태 확인
let play = vizcore.Animation.IsAnimationPlay();
```
**Returns**

| Type      | Description |
|-----------|-------------|
| Boolean   | 재생 상태       |

</procedure>

## Pause
<procedure title="애니메이션 일시 정지" collapsible="true">
<note>Pause()</note>

**Example**
```Javascript
//애니메이션 일시 정지
vizcore.Animation.Pause();
```
</procedure>

## SetEventInterval
<procedure title="애니메이션 이벤트 발생 시간 설정" collapsible="true">
<note>SetEventInterval(val)</note>

**Example**
```Javascript
// 이벤트 발생시간 3초 설정
vizcore.Animation.SetEventInterval(3000);
```
**Parameters**

| Name  | Type    | Description    |
|-------|---------|----------------|
| val   | Number  | 이벤트 발생 시간(ms)  |
</procedure>

## SetPlayTime
<procedure title="애니메이션 재생 시간 설정" collapsible="true">
<note>SetPlayTime(tick)</note>

**Example**
```Javascript
//애니메이션 재생 시간 5초 설정
vizcore.Animation.SetPlayTime(5000);
```
**Parameters**

| Name   | Type    | Description      |
|--------|---------|------------------|
| tick   | Number  | Animation 재생 시간  |
</procedure>

## SetRestoreStatus
<procedure title="애니메이션 재생 시 자동 색상 복원 설정" collapsible="true">
<note>SetRestoreStatus(enable)</note>

**Example**
```Javascript
// 자동 색상 복원 설정
vizcore.Animation.SetRestoreStatus(true);
```
**Parameters**

| Name    | Type      | Description |
|---------|-----------|-------------|
| enable  | Boolean   | 활성화/비활성화    |
</procedure>

## SetStartDate
<procedure title="애니메이션 시작일 지정" collapsible="true">
<note>SetStartDate(date, offset)</note>

**Example**
```Javascript 
// 애니메이션 시작일 지정
vizcore.Animation.SetStartDate(                     
new Date(2022,7, 9)                           // 시작일
,1);                                          // 1초 재생시간 기준 1 Day 변화
```
**Parameters**

| Name     | Type    | Description                |
|----------|---------|----------------------------|
| date     | Date    | 시작일                        |
| offset   | Number  | 재생시간(1초)에 따른 Date 변화량(Day) |
</procedure>

## Start
<procedure title="애니메이션 시작" collapsible="true">
<note>Start()</note>

**Example**
```Javascript
// 애니메이션 시작
vizcore.Animation.Start();
```
</procedure>

## StartNoteAnimation
<procedure title="노트 애니메이션 재생(시작)" collapsible="true">
<note>StartNoteAnimation()</note>

**Example**
```Javascript
//노트 애니메이션 재생
vizcore.Animation.StartNoteAnimation();       
```
</procedure>

## Stop
<procedure title="애니메이션 정지" collapsible="true">
<note>Stop()</note>

**Example**
```Javascript
//애니메이션 정지
vizcore.Animation.Stop();
```
</procedure>

## --- Event Listener ---

## OnChangedFrameEvent
<procedure title="애니메이션 재생 이벤트 등록" collapsible="true">
<note>OnChangedFrameEvent(listener)</note>

**Example**
```Javascript

// Event : onChangedFrameEvent
let onChangedFrameEvent = function (event) {
    console.log(event.data);
}

// Add Event Handler : 애니메이션 재생 이벤트
vizcore.Animation.OnChangedFrameEvent(onChangedFrameEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnChangedPlayTimeEvent
<procedure title="애니메이션 재생 시간 변경 이벤트 등록" collapsible="true">
<note>OnChangedPlayTimeEvent(listener)</note>

**Example**
```Javascript

// Event : onChangedPlayTimeEvent
let onChangedPlayTimeEvent = function (event) {
    console.log(event);
}

// Add Event Handler : 애니메이션 재생 시간 변경 이벤트
vizcore.Animation.OnChangedPlayTimeEvent(onChangedPlayTimeEvent);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>
