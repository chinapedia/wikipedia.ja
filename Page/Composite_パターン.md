> この記事は[Composite パターン](https://ja.wikipedia.org/wiki/Composite_パターン)から翻訳されています。


**Composite パターン**（コンポジット・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink") (Gang of Four; 4人のギャングたち) によって定義された [デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。「構造に関するパターン」に属する。Composite パターンを用いると[ディレクトリ](../Page/ディレクトリ.md "wikilink")と[ファイルなどのような](../Page/ファイル_\(コンピュータ\).md "wikilink")、[木構造を伴う](../Page/木構造_\(データ構造\).md "wikilink")[再帰的](https://ja.wikipedia.org/wiki/再帰的 "wikilink")な[データ構造](../Page/データ構造.md "wikilink")を表すことができる。

Composite パターンにおいて登場する[オブジェクトは](../Page/オブジェクト_\(プログラミング\).md "wikilink")、「枝」と「葉」であり、これらは共通のインターフェースを実装している。そのため、枝と葉を同様に扱えるというメリットがある。

## クラス図

Composite パターンの[クラス図](../Page/クラス図.md "wikilink")を以下に挙げる。

[center](https://ja.wikipedia.org/wiki/ファイル:Composite_UML_class_diagram_\(fixed\).svg "wikilink")

## 利用例

**Composite パターン**を用いて[ディレクトリ](../Page/ディレクトリ.md "wikilink")構造を表す[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プログラムの例を示す。 このプログラムは、

  - 枝を表すクラス : Folderクラス
  - 葉を表すクラス : Fileクラス
  - 共通インタフェース : FileInterfaceインタフェース
  - 実行例を示すためのクラス : DirectoryUserクラス

から構成される。

``` java
 import java.util.ArrayList;
 import java.util.List;

 interface FileInterface {
    public void defaultMethod(int depth);
    public List<FileInterface> getChildren();
    public boolean addComponent(FileInterface c);
    public boolean removeComponent(FileInterface c);
 }


 class File implements FileInterface {

    private String name;

    public File(String name) {
        this.name = name;
    }

    public void defaultMethod(int depth) {
        for (int i = 0; i < depth; i++) System.out.print("  ");
        System.out.println("file:" + this.name);
    }

    public List<FileInterface> getChildren() { return null; }
    public boolean addComponent(FileInterface c) { return false; }
    public boolean removeComponent(FileInterface c) { return false; }

 }


 class Folder implements FileInterface {
    private String name;
    private List<FileInterface> fileList = new ArrayList<FileInterface>();
    public Folder(String name) { this.name = name; }

    public void defaultMethod(int depth) {
        for (int i = 0; i < depth; i++)
            System.out.print("  ");
        System.out.println("folder:" + name);
        for (FileInterface file : fileList) {
            file.defaultMethod(depth + 1);
        }
    }

    public List<FileInterface> getChildren() { return this.fileList; }
    public boolean addComponent(FileInterface c) { return this.fileList.add(c); }
    public boolean removeComponent(FileInterface c) { return this.fileList.remove(c); }
 }


 public class DirectoryUser {
    public static void main(String [] args){
        FileInterface root = new Folder("root");
        FileInterface usr = new Folder("usr");
        FileInterface var = new Folder("var");
        FileInterface home = new Folder("home");
        FileInterface user1 = new Folder("user1");
        FileInterface file1 = new File("file1");

        root.addComponent(usr);
        usr.addComponent(var);
        root.addComponent(home);
        home.addComponent(user1);
        user1.addComponent(file1);
        root.defaultMethod(0);

    }
 }
```

実行結果

``` text
folder:root
  folder:usr
    folder:var
  folder:home
    folder:user1
      file:file1
```

## 注意事項

[thumb](https://ja.wikipedia.org/wiki/ファイル:Composite_UML_object_diagram_with_self_reference.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Composite_UML_object_diagram_with_loop_reference.svg "wikilink") Composite パターンを用いる際には、データ構造がきちんと木構造を保つようにしなければならない。 親子関係が循環してしまった場合、`Component#operation()`を実行した際に[無限ループ](../Page/無限ループ.md "wikilink")に陥るからである。

例えば、[利用例のソースコードを書き換えた以下のプログラムは](https://ja.wikipedia.org/wiki/#利用例 "wikilink")、処理が

`dir1.defaultMethod(0);`

の行に達した時に、無限に出力し続けてしまう。

``` java
 public class LoopExample {
    public static void main(String [] args){
        FileInterface dir1 = new Folder("dir1");
        FileInterface dir2 = new Folder("dir2");
        FileInterface dir3 = new Folder("dir3");

        dir1.addComponent(dir2);
        dir2.addComponent(dir3);
        dir3.addComponent(dir1);
        dir1.defaultMethod(0);
    }
 }
```

## 関係するパターン

  - [Interpreter パターン](../Page/Interpreter_パターン.md "wikilink") : 文法表現が Composite パターンとなる場合が多い。

## 関連項目

  - [木構造 (データ構造)](../Page/木構造_\(データ構造\).md "wikilink")
  - [再帰データ型](../Page/再帰データ型.md "wikilink")
  - [再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")
  - [無限ループ](../Page/無限ループ.md "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")