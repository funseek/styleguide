# Git ブランチ命名規則

## はじめに
株式会社FunseekでのGitブランチ命名規則について述べる。

## リリース前
基本的にはmainブランチで作業を行う。

## リリース後
### ブランチ名一覧
* main
* develop
* feature
* issues
* fix

## ブランチ名詳細
### main
本番環境で動作しているブランチ

### develop
開発中のコミットがマージされて動作確認が行われるブランチ

### feature
命名規則
```
feature/バージョン番号
```

[例]
```
feature/ver1.0.1
```

時期リリースの開発で使用するブランチ

### issues
GitHubのissuesに対応するブランチ  

命名規則
```
issues/issue番号
```

### fix
命名規則
```
fix/チケット番号
```

[例]
```
fix/190
```

バグFixをおこなうブランチ

