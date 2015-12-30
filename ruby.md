# Rubyコーディング規約

## はじめに
株式会社FunseekでのRubyによりコーディングを行う際の規約について述べる。

## ソースコードの整形
### インデント
* プログラムを読みやすくするため、インデントを適宜行う。インデント 幅は2とする。また、インデントにはスペースのみを使用し、タブは使用 しない。

* privateなメソッドはprivate宣言後、インデントを行う。

  [例]
  ```ruby
  class Test
    def aaa
    end
  
    private
      def bbb
      end
  end
  ```

* whenはcaseと同じ深さに揃える

  [OK]
  ```ruby
  case
  when name == 'jun'
    puts 'Jun'
  when name == 'aki'
    puts 'Aki'
  else
    puts 'Nothing'
  end
  ```
  
  [NG]
  ```ruby
  case
    when name == 'jun'
      puts 'Jun'
    when name == 'aki'
      puts 'Aki'
    else
      puts 'Nothing'
  end
  ```


### ブロック
* ブロックは基本的にdo ... endを使用する。ただし、メソッドチェインを行う場合は{ ... }を使用する。

  [例]
  ```ruby
  s = ary.collect { |i| i.to_s }.join(",")
  ```

## コメント
コメントは「#」を使用のみ。埋め込みドキュメントは使用不可とする。（理由としてはdiffで過去差分を見た時に埋め込みドキュメントの場合、コメントかどうか判断が難しいため）

[OK]
```ruby
#def aa
#end
```

[NG]
```ruby
=begin
  def aa
  end
=end
```

## 構文に関する規約
### クラスメソッドの定義
クラスメソッドはclass << selfでまとめる。

[OK]
```ruby
class Hoge
  class << self
    def aa
      "aa"
    end

    def bb
      "bb"
    end
  end
end
```

[NG]
```ruby
class Hoge
  def self.aa
    "aa"
  end
  
  def self.bb
    "bb"
  end
end
```

### return
メソッドの値をメソッドの最後で返す場合はreturnは使用しない

[OK]
```ruby
def add(x, y)
  result = ""
  なにかしらの処理..
  result
end
```

[NG]
```ruby
def add(x, y)
  result = ""
  なにかしらの処理..
  return result
end
```

### 数値
大きな数にはアンダースコアを入れる

[OK]
```ruby
num = 1_000_000
```

[NG]
```ruby
num = 1000000
```




## 命名規約
原則として、単語の省略は行わない。
スコープが狭いループ変数には、i, j, kという名前をこの順序で使 用する。
スコープが狭い変数名には、クラス名を省略したものを使用してよい。 (例: eo = ExampleObject.new)

### クラス・モジュール名
アッパーキャメルケースを使用する

### メソッド名
スネークケースを使用する
