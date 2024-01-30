# VIZWeb

## VIZWeb 생성
<procedure title="VIZWeb 생성">
<note>new VIZWeb(viewContainer)</note>

**Example**
```Javascript
// Defalt Example
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title>Core :: SOFTHILLS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,user-scalable=no" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <link rel="stylesheet" href="VIZCore/Resource/css/VIZCore.css">
    <script type="module">
        import Core from "./VIZCore/VIZCore.js";
        import { VIZCore } from "./VIZCore/VIZCore.js";

        let viewElement = document.getElementById("view");
        viewElement.className = "VIZCore";
        let vizcore = new Core(viewElement);
        let statusInit = vizwide3d.Init();

        // When initialization is successful, basic operation is performed
        if (statusInit === true) {
            loadModel();
        }

        //=======================================
        // Function :: Load Model (*.vizw)
        //=======================================
        function loadModel() {
            vizcore.Model.OpenHeader("./VIZCore/Model/WebModel_wh.vizw");
        }
    </script>
</head>
<body>
    <div id="view"></div>
</body>
</html>






// Defalt Event Example
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title>Core :: SOFTHILLS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0,user-scalable=no" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <link rel="stylesheet" href="VIZCore/Resource/css/VIZCore.css">
    <script type="module">
        import Core from "./VIZCore/VIZCore.js";
        import { VIZCore } from "./VIZCore/VIZCore.js";

        let viewElement = document.getElementById("view");
        viewElement.className = "VIZCore";
        let vizcore = new Core(viewElement);
        let statusInit = vizwide3d.Init();

        //=======================================
        // Event :: OnModelOpenedEvent
        //=======================================
        let OnModelOpenedEvent = function (event) {
            console.log('Model Opend.');
        }

        //=======================================
        // Event :: OnObject3DSelectedEvent
        //=======================================
        let OnObject3DSelected = function (event) {
            // No Object Selected.
            if (event.data.id == -1) {
                console.log('No Object Selected.');
            }
            // Object Selected.
            else {
                // Get Data By Selected Object.
                let node = vizcore.Object3D.FromID(event.data.id);
                let parent = vizcore.Object3D.FromID(node.parentId);

                let id = node.id;
                let index = node.index;
                let nodeKind = node.kind;
                let nodeKindStr = node.kindStr;
                let parentId = node.parentId;
                let name = node.name;
                let level = node.level;
                let boundBox = node.boundBox;

                // Get Structure Data
                let nodes = vizcore.Object3D.GetNodeStructure(
                    event.data.id   // Node ID
                    , false         // Direction - True(Top Down), False(Bottom Up) 
                );

                for (let i = 0; i < nodes.length; i++) {
                    console.log('Node Name : ' + nodes[i].name);
                    }
                }
            }
        }

        // When initialization is successful, basic operation is performed
        if (statusInit === true) {
            initEvent();

            loadModel();
        }
        

        //=======================================
        // Function :: Add Event Handler
        //=======================================
        function initEvent() {
            // Add Event Handler : Loading Completed Event 
            vizcore.Model.OnModelOpenedEvent(OnModelOpenedEvent);

            // Add Event Handler : Object Selected Event
            vizcore.Object3D.OnObject3DSelected(OnObject3DSelected);
        }

        //=======================================
        // Function :: Load Model (*.vizw)
        //=======================================
        function loadModel() {
            vizcore.Model.OpenHeader("./VIZCore/Model/WebModel_wh.vizw");
        }
    </script>
</head>
<body>
    <div id="view"></div>
</body>
</html>
```
**Parameters**

| Name          | Type   | Description                  |
|---------------|--------|------------------------------|
| viewContainer | Object | HTML Div. (Division) Element |
</procedure>

## BeginUpdate
<procedure title="3D 화면 Rendering 차단" collapsible="true">
<note>BeginUpdate()</note>

**Example**
```Javascript
//3D 화면 Rendering 차단
vizcore.BeginUpdate();
```
</procedure>

## Clear
<procedure title="VIZCore Element Clear" collapsible="true">
<note>Clear()</note>

**Example**
```Javascript
//VIZCore Element Clear (인스턴스를 새로 생성하기 전 호출해야 함)
vizcore.Clear();
```
</procedure>

## Connect
<procedure title="VIZCore 라이선스 서버 연결" collapsible="true">
<note>Connect()</note>

**Example**
```Javascript
//VIZCore 라이선스 서버 연결
vizcore.Connect();
```
</procedure>

## Disconnect
<procedure title="VIZCore 라이선스 서버 연결 해제" collapsible="true">
<note>Disconnect()</note>

**Example**
```Javascript
//VIZCore 라이선스 서버 연결 해제
vizcore.Disconnect();
```
</procedure>

## Draw
<procedure title="3D 화면 갱신" collapsible="true">
<note>Draw()</note>

**Example**
```Javascript
//3D 화면 갱신
vizcore.Draw();
```
</procedure>

## EndUpdate
<procedure title="3D 화면 Rendering 차단해제" collapsible="true">
<note>EndUpdate()</note>

**Example**
```Javascript
//3D 화면 Rendering 차단해제
vizcore.EndUpdate();
```
</procedure>

## GetRepeatRender
<procedure title="화면 반복 그리기 설정 반환" collapsible="true">
<note>GetRepeatRender() → {boolean}</note>

**Example**
```Javascript
//화면 반복 그리기 설정 반환
vizcore.GetRepeatRender();
```
**Returns**

| Type    | Description                        |
|---------|------------------------------------|
| boolean | true : 반복그리기, false : Render 시 그리기 |
</procedure> 

## Render
<procedure title="3D 화면 모델 Render" collapsible="true">
<note>Render()</note>

**Example**
```Javascript
//3D 화면 모델 Render
vizcore.Render();
```
</procedure>

## Resize
<procedure title="3D 화면 크기 갱신" collapsible="true">
<note>Resize()</note>

**Example**
```Javascript
//3D 화면 크기 갱신
vizcore.Resize();
```
</procedure>

## SetRepeatRender
<procedure title="화면 반복 그리기 설정" collapsible="true">
<note>SetRepeatRender(enable)</note>

**Example**
```Javascript
//화면 반복 그리기 설정
vizcore.SetRepeatRender(true);

//주의) 잦은 렌더링으로 성능 영향이 있습니다.
```
**Parameters**

| Name   | Type    | Description                        |
|--------|---------|------------------------------------|
| enable | boolean | true : 반복그리기, false : Render 시 그리기 |
</procedure>