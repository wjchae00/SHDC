# Note

## AddNote
<procedure title="3D 노트 추가" collapsible="true">
<note>AddNote(note) → {String}</note>

**Example**
```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

let text = [];                  //Array<String>
text.push('3D Note #1');
text.push('3D Note #2');

note.text.value = text;             //value
note.text.position = new VIZCore.Vector3(1000, 2000, 3000);         //생성 위치

note.style.font.size = 10;
note.style.font.color.set(0, 56, 101, 255);          // R, G, B, A
note.style.border.type = 1;                          // 0 (Rectangle), 1(Rounded Rectangle)
note.style.border.color.set(41, 143, 194, 255);      // R, G, B, A
note.style.background.color.set(255, 255, 255, 200); // R, G, B, A

//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| note | Object | Note Object |

**Returns**

| Type   | Description |
|--------|-------------|
| String | Note ID     |

</procedure> 

## AddNote2D
<procedure title="2D 노트 추가" collapsible="true">
<note>AddNote2D(text)</note>

**Example**
```Javascript
let text = [];                  //Array<String>
text.push('2D Note #1');
text.push('2D Note #2');
//2D 노트 추가
vizcore.Review.Note.AddNote2D(text);
```
**Parameters**

| Name | Type            | Description |
|------|-----------------|-------------|
| text | `Array<String>` | 노트 텍스트      |
</procedure>

## AddNote3D
<procedure title="3D 노트 추가" collapsible="true">
<note>AddNote3D(text)</note>

**Example**
```Javascript
let text = [];                  //Array<String>
text.push('3D Note #1');
text.push('3D Note #2');
//3D 노트 추가
vizcore.Review.Note.AddNote3D(text);
```
**Parameters**

| Name | Type            | Description |
|------|-----------------|-------------|
| text | `Array<String>` | 노트 텍스트      |
</procedure>

## AddNoteSurface
<procedure title="표면 노트 추가" collapsible="true">
<note>AddNoteSurface(text)</note>

**Example**
```Javascript
let text = [];                //Array<String>
text.push('Surface Note #1');
text.push('Surface Note #2');
//표면 노트 추가
vizcore.Review.Note.AddNoteSurface(text);
```
**Parameters**

| Name | Type            | Description                                  |
|------|-----------------|----------------------------------------------|
| text | `Array<String>` | 노트 텍스트 (== undefined or [] 일경우 Body 이름으로 생성) |
</procedure>

## DeleteAll
<procedure title="노트 전체 삭제" collapsible="true">
<note>DeleteAll()</note>

**Example**
```Javascript
//노트 전체 삭제
vizcore.Review.Note.DeleteAll();

//[To Do] 화면 다시그리기 호출
vizwide3d.Render();
```
</procedure>

## DeleteByID
<procedure title="노트 정보 삭제" collapsible="true">
<note>DeleteByID(id)</note>

1. Examples
```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

let text = [];                           //Array<String>
text.push('3D Note #1');
text.push('3D Note #2');

note.text.value = text;                     //value
note.text.position = new VIZCore.Vector3(1000, 2000, 3000);             //생성 위치
note.id = 2                             // noteID 지정

//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);
//노트 정보 삭제
vizcore.Review.Note.DeleteByID(2);           //Number

let ids = [10, 11];
vizcore.Review.Note.DeleteByID(ids);          //Array

//[To Do] 화면 다시그리기 호출
vizwide3d.Render();
```
**Parameters**

| Name | Type   | Description             |
|------|--------|-------------------------|
| id   | Object | 개체 아이디(Number or Array) |
</procedure>

## NewImageNote
<procedure title="이미지 노트 추가" collapsible="true">
<note>NewImageNote(image, size) → {Object}</note>

**Example**
```Javascript
//Image 생성
let img = new Image();
img.src = 'image.jpg';
img.onload = function () {
let note = vizcore.Review.Note.NewImageNote(img); //image src size
//let note = vizcore.Review.Note.NewImageNote(img, new VIZCore.Vector2(128, 128)); //set image Size

     let text = [];                                       //Array<String>
     text.push('Image Note #1');
     text.push('Image Note #2');

     note.text.value = text;
     note.text.position = new VIZCore.Vector3(0, 0, 0);          // Text
     note.drawitem.position.push(new VIZCore.Vector3(1000, 6000, 6000));  // Image Postion

     note.style.font.size = 10;
     note.style.font.color.set(0, 56, 101, 255);          // R, G, B, A

     note.style.border.enable = false;
     note.style.border.type = 1;                          // 0 (Rectangle), 1(Rounded Rectangle)
     note.style.border.color.set(41, 143, 194, 255);      // R, G, B, A

     note.style.background.enable = false;
     note.style.background.color.set(255, 255, 255, 200); // R, G, B, A

     note.style.arrow.color.set(255, 0, 0, 255);          // R, G, B, A
     note.style.arrow.size = 10;

     note.style.line.color.set(0, 0, 0, 255);             // R, G, B, A
     note.style.line.thickness = 4;

     let noteId = vizcore.Review.Note.AddNote(note);
};
```
**Parameters**

| Name  | Type            | Description                   |
|-------|-----------------|-------------------------------|
| image | Object          | Image Object                  |
| size  | VIZCore.Vector2 | image size (기본값 : 이미지 원본 사이즈) |

**Returns**

| Type   | Description |
|--------|-------------|
| Object | Note Object |

</procedure>

## NewNote3D
<procedure title="3D 노트 추가" collapsible="true">

<note>NewNote3D() → {Object}</note>

**Example**
```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

let text = [];                           //Array<String>
text.push('3D Note #1');
text.push('3D Note #2');

note.text.value = text;                     //value
note.text.position = new VIZCore.Vector3(1000, 2000, 3000);             //생성 위치

note.style.font.size = 10;
note.style.font.color.set(0, 56, 101, 255);          // R, G, B, A
note.style.border.type = 1;                          // 0 (Rectangle), 1(Rounded Rectangle)
note.style.border.color.set(41, 143, 194, 255);      // R, G, B, A
note.style.background.color.set(255, 255, 255, 200); // R, G, B, A
//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);
```
**Returns**

| Type   | Description |
|--------|-------------|
| Object | Note Object |

</procedure>

## NewNoteSurface
<procedure title="표면 노트 추가" collapsible="true">
<note>NewNoteSurface() → {Object}</note>

**Example**
```Javascript
//표면 노트 추가
let note = vizcore.Review.Note.NewNoteSurface();

let text = [];                                  //Array<String>
text.push('Surface Note #1');
text.push('Surface Note #2');

note.text.value = text;                         //value
note.text.position = new VIZCore.Vector3(1000, 2000, 3000);          // Text
note.drawitem.position.push(new VIZCore.Vector3(1000, 6000, 6000));  // Arrow

note.style.font.size = 10;
note.style.font.color.set(0, 56, 101, 255);          // R, G, B, A
note.style.border.type = 1;                          // 0 (Rectangle), 1(Rounded Rectangle)
note.style.border.color.set(41, 143, 194, 255);      // R, G, B, A
note.style.background.color.set(255, 255, 255, 200); // R, G, B, A

note.style.arrow.color.set(255, 0, 0, 255);          // R, G, B, A
note.style.arrow.size = 10;

note.style.line.color.set(0, 0, 0, 255);             // R, G, B, A
note.style.line.thickness = 4;
//노트 정보 추가
let noteId = vizcore.Review.Note.AddNote(note);
```
**Returns**

| Type   | Description |
|--------|-------------|
| Object | Note Object |

</procedure> 

## --- Event Listener ---

## OnSelectedEvent
<procedure title="노트 선택 이벤트 등록" collapsible="true">
<note>OnSelectedEvent(listener)</note>

**Example**
```Javascript
// Event : OnSelectedEvent
let onSelected = function (event) {
    console.log(event);
}

// Add Event Handler : Note Selected Event (노트 선택 이벤트)
vizcore.Review.Note.OnSelectedEvent(onSelected);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>

## OnSelectedPositionEvent
<procedure title="노트 선택 위치 반환 이벤트 등록" collapsible="true">
<note>OnSelectedPositionEvent(listener)</note>

**Example**
```Javascript
// Event : OnSelectedPositionEvent
let onSelectedPosition = function (event) {
    console.log(event); 
}

// Add Event Handler : Note Selected Position Event (노트 선택 위치 반환 이벤트)
vizcore.Review.Note.OnSelectedPositionEvent(onSelectedPosition);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>