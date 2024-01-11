# Review

## DeleteAll
<procedure title="모든 리뷰 정보 삭제" collapsible="true">
<note>DeleteAll()</note>

**Example**
```Javascript
//모든 리뷰 정보 삭제
vizcore.Review.DeleteAll();

//[To Do] 화면 다시그리기 호출
vizcore.Render();
```
</procedure>

## DeleteByID
<procedure title="리뷰 정보 삭제" collapsible="true">
<note>DeleteByID(id)</note>

1. Examples
```Javascript
//3D 노트 생성
let note = vizcore.Review.Note.NewNote3D();

let text = [];                           //Array<String>
text.push('3D Note #1');
text.push('3D Note #2');

note.text.value = text;                     //value
note.text.position = new VIZCore.Vector3(0, 0, 0);             //생성 위치
note.id = 10                             // noteID 지정

//3D 노트 추가
let noteId = vizcore.Review.Note.AddNote(note);

//리뷰 정보 삭제
vizcore.Review.DeleteByID(10);              //Number
let ids = [10, 11];                         //Array
vizcore.Review.DeleteByID(ids);

//[To Do] 화면 다시그리기 호출
vizcore.Render();
```
**Parameters**

| Name | Type   | Description             |
|------|--------|-------------------------|
| id   | Object | 개체 아이디(Number or Array) |
</procedure>

## ExportJSON
<procedure title="리뷰 정보 JSON 내보내기" collapsible="true">
<note>ExportJSON() → {string}</note>

**Example**
```Javascript
//리뷰 정보 JSON 내보내기
let json = vizcore.Review.ExportJSON();
console.log("ExportJSON :: ", json);
```
**Returns**

| Type   | Description |
|--------|-------------|
| string | JSON 문자열    |

</procedure>

## GetItem
<procedure title="리뷰 정보 반환" collapsible="true">
<note>GetItem(id) → {Data.ReviewItem}</note>

**Example**
```Javascript
//리뷰 정보 반환
let review = vizcore.Review.GetItem(10);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | Number | 개체 아이디      |

**Returns**

| Type            | Description |
|-----------------|-------------|
| Data.ReviewItem | 리뷰 객체       |

</procedure>

## GetReview
<procedure title="리뷰 정보 반환" collapsible="true">
<note>GetReview(id) → {Data.ReviewItem}</note>

**Example**
```Javascript
//리뷰 정보 반환
let review = vizcore.Review.GetReview(10);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| id   | Number | 개체 아이디      |

**Returns**

| Type            | Description |
|-----------------|-------------|
| Data.ReviewItem | 리뷰 객체       |

</procedure>

## Select
<procedure title="리뷰 선택/선택해제 설정" collapsible="true">
<note>Select(id, select)</note>

**Example**
```Javascript
//리뷰 선택/선택해제 설정
vizcore.Review.Select(10, true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| id     | Number  | 개체 아이디      |
| select | boolean | 선택/선택해제     |
</procedure>

## SelectAll
<procedure title="전체 리뷰 선택/선택해제 설정" collapsible="true">
<note>SelectAll(select)</note>

**Example**
```Javascript
//전체 리뷰 선택/선택해제 설정
vizcore.Review.SelectAll(true);
```
**Parameters**

| Name   | Type    | Description |
|--------|---------|-------------|
| select | boolean | 선택/선택해제     |
</procedure>

## SelectByKind
<procedure title="리뷰 유형 별 선택/선택해제 설정" collapsible="true">
<note>SelectByKind(select, reviewKind)</note>

**Example**
```Javascript
//리뷰 유형 별 선택/선택해제 설정
vizcore.Review.SelectByKind(true, VIZCore.Enum.REVIEW_TYPES.RK_2D_NOTE);
```
**Parameters**

| Name       | Type                      | Description                     |
|------------|---------------------------|---------------------------------|
| select     | boolean                   | 선택/선택해제                         |
| reviewKind | VIZCore.Enum.REVIEW_TYPES | VIZCore.Enum.REVIEW_TYPES 리뷰 타입 |
</procedure>

## SetAlertLocation
<procedure title="리뷰 안내창 위치 설정" collapsible="true">
<note>SetAlertLocation(top, left)</note>

**Example**
```Javascript
//리뷰 안내창 위치 설정
vizcore.Review.SetAlertLocation(50,100);
```
**Parameters**

| Name | Type   | Description |
|------|--------|-------------|
| top  | Number | Top Offset  |
| top  | Number | Left Offset |
</procedure>

## Show
<procedure title="리뷰 보이기/숨기기 설정" collapsible="true">
<note>Show(id, visible)</note>

**Example**
```Javascript
//리뷰 보이기/숨기기 설정
vizcore.Review.Show(10, true);
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| id      | Number | 개체 아이디      |
| visible | Number | 보이기/숨기기     |
</procedure>

## ShowAll
<procedure title="전체 리뷰 보이기/숨기기 설정" collapsible="true">
<note>ShowAll(visible)</note>

**Example**
```Javascript
//전체 리뷰 보이기/숨기기 설정
vizcore.Review.ShowAll(true);
```
**Parameters**

| Name    | Type   | Description |
|---------|--------|-------------|
| visible | Number | 보이기/숨기기     |
</procedure>

## ShowByKind


<procedure title="리뷰 유형 별 보이기/숨기기 설정" collapsible="true">
<note>ShowByKind(visible, reviewKind)</note>

**Example**
```Javascript
//리뷰 유형 별 보이기/숨기기 설정
vizcore.Review.ShowByKind(true, VIZCore.Enum.REVIEW_TYPES.RK_2D_NOTE);
```
**Parameters**

| Name       | Type                      | Description                     |
|------------|---------------------------|---------------------------------|
| visible    | Number                    | 보이기/숨기기                         |
| reviewKind | VIZCore.Enum.REVIEW_TYPES | VIZCore.Enum.REVIEW_TYPES 리뷰 타입 |
</procedure>

## --- Event Listener ---

## OnReviewChangedEvent
<procedure title="리뷰 변경 이벤트" collapsible="true">
<note>OnReviewChangedEvent(listener)</note>

**Example**
```Javascript
// Event : OnReviewChangedEvent
let OnReviewChanged = function (event) {
    console.log(event);
}

// Add Event Handler : Review Change Event (리뷰 변경 이벤트)
vizcore.Review.OnReviewChangedEvent(OnReviewChanged);
```
**Parameters**

| Name     | Type   | Description    |
|----------|--------|----------------|
| listener | Object | Event Listener |
</procedure>