# VIZWide3D

<procedure>

>**VIZWide3D는** 대용량 3D 모델, 모델 구조, 사용자 정의 속성, PMI 정보와 기타 내용을 포함하여 웹 브라우저에서 3D 웹 어플리케이션을 개발할 수 있습니다. 
또한, 클리핑, 측정 및 마크업 기능을 제공합니다.
</procedure>

## 구성 요소 및 특징
<procedure>

<tip>VIZWide3D는 2 가지 주요 구성요소로 이루어져 있습니다.</tip>

* **VIZPub(Publisher)는** 웹 서버에 배포되는 독립 실행형 실행파일(콘솔)입니다. <br/>VIZPub Professional 라이선스가 필요하며, 
다양한 CAD 형식을 VIZWide3D에서 활용가능한 "경량 3D 파일 형식 [VIZ(W)]" 형식으로 변환합니다.
<br/>또한, 변환된 VIZ 파일을 통해 다양한 용도로 재활용이 가능한 메타데이터 및 미리보기 이미지를 추출할 수 있습니다.
  
* **VIZWide3D** 스크립트는 브라우저 내에서 3D 모델을 가시화하고, 상호작용하는 클라이언트 기반 JavaScript 애플리케이션입니다. 
<br/>VIZWide3D는 모든 주요 데스크탑 및 모바일 플랫폼의 모든 주요 HTML5 지원 브라우저에서 작동합니다.


<tip>VIZWide3D는 웹 브라우저 내에서 CAD 모델을 조회하고, 상호작용을 지원할 수 있는 무설치(Zero-Install) 클라이언트측 구성 요소입니다.</tip>


<tip>VIZWide3D는 웹 서버에 연결하여 VIZPub(변환기)에서 생성한 "VIZW(VIZ Web MODEL)"를 조회합니다.
뷰어는 개발자가 기능의 모든 측면을 제어할 수 있는 Open API를 제공합니다.</tip>
<tip>VIZWide3D는 변환된 VIZW에 포함되어 있는 3D 형상의 지오메트리 데이터를 클라이언트의 웹 브라우저로 모두 전송되고, WebGL을 통해 렌더링되므로 사용자의 상호작용 처리 성능이 향상됩니다.</tip>

</procedure>

## API

<procedure>

* [**Animation**](Animation.md)
* [**ContextMenu**](ContextMenu.md)
* [**Disassembly**](Disassembly.md) 
* [**Frame**](Frame.md)
* [**GeometryUtility**](GeometryUtility.md)
* [**Model**](Model.md) 
* [**ModelTree**](ModelTree.md) 
* [**Object3D**](Object3D.md) 
  * [**Color**](Color.md) 
  * [**CustomEdge**](CustomEdge.md) 
  * [**Find**](Find.md) 
  * [**GeometryProperty**](GeometryProperty.md) 
  * [**Transform**](Transform.md) 
  * [**UDA**](UDA.md) 
* [**Panel**](Panel.md) 
* [**Player**](Player.md) 
* [**Review**](Review.md)
  * [**Measure**](Measure.md) 
  * [**Note**](Note.md)
  * [**Section**](Section.md) 
* [**ShapeDrawing**](ShapeDrawing.md) 
* [**Toolbar**](Toolbar.md) 
* [**View**](View.md) 
  * [**Control**](Control.md) 
  * [**ViewCube**](ViewCube.md) 
  * [**Walkthrough**](Walkthrough.md) 
  * [**Weather**](Weather.md) 
  * [**Xray**](Xray.md)
* [**VIZWeb**](VIZWeb.md) 

</procedure>