# Disassembly

## AddGroup
<procedure title="분해 그룹 지정" collapsible="true">
<note>AddGroup(groupId, ids)</note>

**Example**
```Javascript
let nodes = vizcore.Object3D.Find.GetNodeByName(
    'PIPE101'   // Keyword
    , true      // Full Match
);

let ids1 = vizcore.Object3D.GetBodyIdsByNode(nodes);

let ids2 = [3];           //Object ID Array
//분해 그룹 지정
vizcore.Disassembly.AddGroup("group1", ids1);
vizcore.Disassembly.AddGroup("group2", ids2);
```
**Parameters**

| Name    | Type            | Description    |
|---------|-----------------|----------------|
| groupId | String          | Group ID       |
| ids     | `Array<Number>` | Object ID List |
</procedure>

## ClearGroup
<procedure title="분해 모든 그룹 제거" collapsible="true">
<note>ClearGroup()</note>

**Example**
```Javascript
//분해 모든 그룹 제거
vizcore.Disassembly.ClearGroup();
```
</procedure>

## DisassembleAll
<procedure title="전체 개체 분해" collapsible="true">
<note>DisassembleAll(rate)</note>

**Example**
```Javascript
//전체 개체 분해
vizcore.Disassembly.DisassembleAll(1);
```

**Parameters**

| Name | Type   | Description     |
|------|--------|-----------------|
| rate | Number | 거리 비율 (기본값 1.0) |
</procedure>

## DisassembleGroup
<procedure title="지정된 그룹으로 분해" collapsible="true">
<note>DisassembleGroup(rate)</note>

**Example**
```Javascript
let ids1 = [9];           //Object ID Array  
let ids2 = [3];           //Object ID Array

//분해 그룹 지정
vizcore.Disassembly.AddGroup("group1", ids1);
vizcore.Disassembly.AddGroup("group2", ids2);

//지정된 그룹으로 분해
vizcore.Disassembly.DisassembleGroup();
```
**Parameters**

| Name | Type   | Description     |
|------|--------|-----------------|
| rate | Number | 거리 비율 (기본값 1.0) |
</procedure>

## DisassembleSelect
<procedure title="선택된 개체 분해" collapsible="true">
<note>DisassembleSelect(rate)</note>

**Example**
```Javascript
//선택된 개체 분해
vizcore.Disassembly.DisassembleSelect(1);
```

**Parameters**

| Name | Type   | Description     |
|------|--------|-----------------|
| rate | Number | 거리 비율 (기본값 1.0) |
</procedure>

## RestoreAll
<procedure title="위치 초기화" collapsible="true">
<note>RestoreAll()</note>

**Example**
```Javascript
//위치 초기화
vizcore.Disassembly.RestoreAll();
```
</procedure>