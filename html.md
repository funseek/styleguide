# HTMLコーディングの際の注意点

## はじめに
株式会社FunseekでのHTMLコーディングの注意点など記載。

## 注意点
### タグを必ず閉じる

[例]  
✕
```
<input type="number"  className="form-control">
```
◯
```
<input type="number"  className="form-control" />
```

### インデントをする

[例]  
✕
```
<tr>
  <td>hoge</td></tr>
```
◯
```
<tr>
  <td>hoge</td>
</tr>
```

### formタグでレイアウト調整をしない
[例]
✕
```
<form className="form-horizontal">
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
</form>
<form className="form-horizontal">
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
</form>
```
◯
```
<div className="horizontal">
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
</div>
<div className="horizontal">
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
  <div className="form-group">
    <label  className="col-sm-2 control-label">hoge</label>
    <input type="text" className="form-control" />
  </div>
</div>
```
※ただし明確にformの範囲を理解してい記述している場合はOK

### タブはスペース２
### Reactで実装する場合はjQuery依存のjsを利用しない（JSでHTMLを生成しているようなライブラリは特にNG）
### cssはscssで書く
### scssで命名規則を意識して書く（ディレクトリ構成なども）

