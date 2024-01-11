# Initialization

<deflist>
<def title="onConfiguration function">

초기 환경설정 변경 콜백 함수

```Javascript
let onConfiguration =()=>{
    //VIZCore Path 경로 지정
    //vizcore.Configuration.Default.Path = "../";    
    
    //좌표축 설정
    //vizcore.Configuration.Render.CoordinateAxis.Visible = false;
};
```        
</def>
<def title="onBefore function">

WebAssembly 파일 위치 변경 시 다운로드 경로 지정

WebAssembly의 기본 경로 : `VIZCore/lib/shdcore/shdcore.wasm`

```Javascript
let onBefore =()=>{
    // WebAssembly 다운로드를 위한 shdcore.wasm 파일이 있는 경로를 지정     
    // vizcore.Main.ShdCore.setPath("../", 'VIZCore/lib/shdcore/shdcore.wasm');
};
```        
</def>
<def title="onInit function">

VIZWide3D / VIZWeb3D 초기화 완료 시의 콜백 함수

```Javascript
let onInit = ()=>{
    // Toolbar 사용
    let toolbar = new vizcore.Toolbar(view, vizcore, VIZCore);

    // ContextMenu 사용
    let context = new vizcore.ContextMenu(view, vizcore, VIZCore);

    // Add Event Handler : Progress Event (로딩 이벤트)
    vizcore.Model.OnStreamProgressChangedEvent(function(e){
        
    });

    // Add Event Handler : Object Selected Event (모델 선택 이벤트)
    vizcore.Object3D.OnObject3DSelected(onSelectEvent);

    // View Info 확인
    let OnViewDrawInfo = function (event) {
         
    }
    vizcore.View.OnViewDrawInfoEvent(OnViewDrawInfo);

    // 단일 VIZWide3D 용 VIZW 파일의 헤더 열기
    //vizcore.Model.OpenHeader("VIZCore/Model/toycar/vizw/toycar_wh.vizw", "Sample", onModelLoadingCompleted);
    
    // 단일 VIZWeb3D 용 VIZW 모델 파일 열기
    //vizcore.Model.Open("./VIZCore/Model/toycar.vizw");
};  
```

* [OnStreamProgressChangedEvent API](Model.md#onstreamprogresschangedevent)
* [OnObject3DSelected API](Object3D.md#onobject3dselected)
* [OnViewDrawInfoEvent API](View.md#onviewdrawinfoevent)
* [OpenHeader API](Model.md#openheader)
* [Open API](Model.md#open)
</def>
<def title="콜백 함수를 변수에 지정">

```Javascript
let option = {
        event : {
        
            // 초기화가 완료 된 후 콜백 함수
            onInit : onInit,            
            
            // WebAssembly 다운로드 경로를 지정하는 콜백 함수           
            onBefore : onBefore,
            
            // 초기 환경설정을 변경하는 콜백 함수
            onConfiguration : onConfiguration,
        }
    }
vizcore.Init(option);
```
</def>
</deflist>