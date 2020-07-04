> この記事は[Memento パターン](https://ja.wikipedia.org/wiki/Memento_パターン)から翻訳されています。


**memento パターン**（[英](../Page/英語.md "wikilink"): **Memento pattern**、日本: **メメント パターン**）はソフトウェアの[デザインパターンの一つで](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、オブジェクトを以前の状態に(ロールバックにより)戻す能力を提供する。

memento パターンは二つのオブジェクトによって用いられる。'originator'と'caretaker' である。'originator' は内部状態を持つオブジェクトである。caretaker は originator に何らかの動作を行うが、変更を戻す能力を持ちたいとする。まず、caretaker は originator に memento を要求する。次に任意の操作（あるいは一連の操作）を行う。操作を行う前の状態に戻すために、memento オブジェクトを originator に返却する。memento オブジェクト自体は、[不透明オブジェクト](https://ja.wikipedia.org/wiki/:en:opaque_data_type "wikilink")( caretaker が変更してはいけないもの) である。このパターンを用いる場合、originator がほかのオブジェクトやリソースを変更してしまうかどうか注意が必要である。memento パターンは単一のオブジェクトに対して働くためである。

memento パターンの古典的な例として、[擬似乱数](../Page/擬似乱数.md "wikilink")発生器や、[有限オートマトン](../Page/有限オートマトン.md "wikilink")の状態などがある。

## Memento パターンの例

### Java

以下の [Java](https://ja.wikipedia.org/wiki/Java "wikilink") プログラムは、 Memento パターンを "undo" に使った場合を示す。

``` java
import java.util.*;

class Originator {
    private String state;
    /* メモリを消費する多数の private のデータで状態に関係しないものは保存されるべきでない。
     * memento は小さなオブジェクトであるべき */


    public void set(String state) {
        System.out.println("Originator: Setting state to "+state);
        this.state = state;
    }

    public Object saveToMemento() {
        System.out.println("Originator: Saving to Memento.");
        return new Memento(state);
    }
    public void restoreFromMemento(Object m) {
        if (m instanceof Memento) {
            Memento memento = (Memento)m;
            state = memento.getSavedState();
            System.out.println("Originator: State after restoring from Memento: "+state);
        }
    }

    private static class Memento {
        private String state;

        public Memento(String stateToSave) { state = stateToSave; }
        public String getSavedState() { return state; }
    }
}

class Caretaker {
    private List<Object> savedStates = new ArrayList<Object>();

    public void addMemento(Object m) { savedStates.add(m); }
    public Object getMemento(int index) { return savedStates.get(index); }
}

class MementoExample {
    public static void main(String[] args) {
        Caretaker caretaker = new Caretaker();

        Originator originator = new Originator();
        originator.set("State1");
        originator.set("State2");
        caretaker.addMemento( originator.saveToMemento() );
        originator.set("State3");
        caretaker.addMemento( originator.saveToMemento() );
        originator.set("State4");

        originator.restoreFromMemento( caretaker.getMemento(1) );
    }
}
```

出力:

`Originator: Setting state to State1`
`Originator: Setting state to State2`
`Originator: Saving to Memento.`
`Originator: Setting state to State3`
`Originator: Saving to Memento.`
`Originator: Setting state to State4`
`Originator: State after restoring from Memento: State3`

### Ruby

以下の [Ruby](../Page/Ruby.md "wikilink") プログラムで同じパターンを示す。

``` ruby
#!/usr/bin/env ruby -KU

require 'rubygems'
require 'spec'

class Originator
  class Memento
    def initialize(state)
      # Originator の元の状態を壊しても、この Memento オブジェクトが初回以降の restore で
      # 破壊されないよう dup が必要
      @state = state.dup
    end

    def state
      # Originator の元の状態を壊しても、この Memento オブジェクトが二度目の restore で
      # 破壊されないよう dup が必要
      @state.dup
    end
  end

  attr_accessor :state

  # メモリに巨大なデータが多数あり、state から再構成可能であるように見せる
  def save_to_memento
    Memento.new(@state)
  end

  def restore_from_memento(m)
    @state = m.state
  end

end

class Caretaker < Array; end

describe Originator do
  before(:all) do
    @caretaker = Caretaker.new
    @originator = Originator.new

    @originator.state = "State1"
  end

  it "should have original state" do
    @originator.state.should == 'State1'
  end

  it "should update state" do
    @originator.state = "State2"
    @originator.state.should == 'State2'
  end

  it "should save memento" do
    @caretaker << @originator.save_to_memento
    @caretaker.size.should == 1
  end

  it "should update state after save to memento" do
    @originator.state = "State3"
    @originator.state.should == 'State3'
  end

  it "should save to memento again" do
    @caretaker << @originator.save_to_memento
    @caretaker.size.should == 2
  end

  it "should update state after save to memento again" do
    @originator.state = "State4";
    @originator.state.should == 'State4'
  end

  it "should restore to original save point" do
    @originator.restore_from_memento @caretaker[0]
    @originator.state.should == 'State2'
  end

  it "should restore to second save point" do
    @originator.restore_from_memento @caretaker[1]
    @originator.state.should == 'State3'
  end

  it "should restore after pathological munging of restored state" do
    @originator.state[-1] = '5'
    @originator.state.should == 'State5'
    @originator.restore_from_memento @caretaker[1]
    @originator.state.should == 'State3'
  end

  it "should restore after pathological munging of original state" do
    @originator.state = "State6"
    @originator.state.should == 'State6'
    @caretaker << @originator.save_to_memento
    @originator.state[-1] = '7'
    @originator.state.should == 'State7'
    @originator.restore_from_memento @caretaker[2]
    @originator.state.should == 'State6'
  end
end
```

## 関連項目

  - [Facade パターン](../Page/Facade_パターン.md "wikilink")
  - [永続データ構造](../Page/永続データ構造.md "wikilink")

## 外部リンク

  - [Description](http://adapower.com/index.php?Command=Class&ClassID=Patterns&CID=271) by [Matthew Heaney](https://ja.wikipedia.org/wiki/Matthew_Heaney "wikilink")
  - [Memento UML Class Diagram](http://dofactory.com/Patterns/PatternMemento.aspx) with C\# and .NET code samples

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")