# HTMLコーディングの際の注意点

## はじめに
株式会社FunseekでのHTMLコーディングの注意点など記載。

## 注意点
- タグを必ず閉じる

[例]  
✕
```
<input type="number"  className="form-control">
```
◯
```
<input type="number"  className="form-control" />
```

- インデントをする

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

- タブはスペース２
- Reactで実装する場合はjQuery依存のjsを利用しない（JSでHTMLを生成しているようなライブラリは特にNG）
- cssはscssで書く
- scssで命名規則を意識して書く（ディレクトリ構成なども）

