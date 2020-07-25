> この記事は[レヴィC曲線](https://ja.wikipedia.org/wiki/レヴィC曲線)から翻訳されています。


**レヴィC曲線（英：Lévy C curve、レヴィ曲線、レヴィ・ドラゴンとも呼ばれる）**は、数学において最初に記述された[自己相似](../Page/自己相似.md "wikilink")[フラクタル](../Page/フラクタル.md "wikilink")である。その図形の[微分可能性について](https://ja.wikipedia.org/wiki/微分可能関数 "wikilink")1906年に[アーネスト・チェザロ](https://ja.wikipedia.org/wiki/アーネスト・チェザロ "wikilink")、1910年にによって分析されたが、現在では[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")の[数学者](../Page/数学者.md "wikilink") [ポール・レヴィの名前を冠している](https://ja.wikipedia.org/wiki/ポール・レヴィ_\(数学者\) "wikilink")、彼はその図形の自己相似性について初めて言及し、[コッホ曲線](../Page/コッホ曲線.md "wikilink")と同じ種類の代表的な曲線として幾何学的な構造を規定した。 これは、特殊な倍周期曲線、である。

## Lシステムによる記述

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Levy_C_construction.png "wikilink") [サムネイル](https://ja.wikipedia.org/wiki/ファイル:Levy_C_Curve.svg "wikilink") [Lシステムを使用する場合](../Page/L-system.md "wikilink")、C曲線の作成は直線から始める。 この線を斜辺として使用して、45°、90°、45°の角度の[二等辺三角形](../Page/二等辺三角形.md "wikilink")を作成する。元の線は、この三角形の他の2つの辺に置き換えられる（図1の2段階まで）。

次の段階で、2つの新しい線は、それぞれ別の直角二等辺三角形の底辺を形成し、それぞれの三角形の二等辺に置き換えられる。したがって、2段階後、曲線は元の線と同じ長辺で、半分の短辺の長方形のコの字型の図形となる（図1の3段階まで）。

後続の各段階で、曲線の各直線部は、その直線部を底辺として構築された直角二等辺三角形の二等辺に次々と置き換えられる。*n*段階後、曲線は2 <sup>*n*</sup>の線分で構成され、各線分は元の線より2 <sup>*n* / 2</sup>倍小さくなる（図1の4段階以降）。

このLシステムは次のように記述できる。

<table>
<tbody>
<tr class="odd">
<td><p><strong>変数</strong> ：</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>定数</strong> ：</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><strong>開始</strong> ：</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>置換規則</strong> ：</p></td>
<td></td>
</tr>
</tbody>
</table>

ここで "  "は「前方への直線」を意味し、「+」は「時計回りに45°回転」を意味し、「 − 」は「反時計回りに45°回転」を意味する。

この「無限」プロセスの極限であるフラクタル曲線は、レヴィC曲線と呼ばれる。その名前は、アルファベットの文字「C」に類似していることに由来し、その文字が装飾された状態のものを特にレヴィC曲線と称している。 この曲線は、「[ピタゴラスの木](https://ja.wikipedia.org/wiki/ピタゴラスの木 "wikilink")」によく似ている。

C曲線の[ハウスドルフ次元](https://ja.wikipedia.org/wiki/ハウスドルフ次元 "wikilink")は2に等しい（開集合を含む）が、境界の次元は約1.9340である[1](http://mathworld.wolfram.com/LevyFractal.html) 。

### バリエーション

標準的なC曲線は、45°の二等辺三角形を使用して作成される。C曲線のバリエーションは、45°以外の角度の二等辺三角形を使用して作成することができる。 角度が60°未満である限り、各段階で導入される新しい線は、それぞれが置き換える線よりも短いので、構築プロセスは極限曲線に向かう傾向となる。45°未満の角度では、「カール」が少なくなるフラクタルが生成される。

## 反復関数系(IFS)による記述

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Lévy's_C-curve_\(IFS\).jpg "wikilink") [反復関数システム](../Page/反復関数系.md "wikilink") （IFS、または事実上の[カオスゲーム](../Page/カオスゲーム.md "wikilink")の IFS手法）を使用する場合、C曲線の構築はやや簡単である。 これには、二つの「規則」を必要とする、すなわち、[平面](../Page/平面.md "wikilink")上の2つの点が、それぞれ[スケール因子](https://ja.wikipedia.org/wiki/スケール因子 "wikilink") の1/と関連付けられる。第1の規則は45°の回転、第2の規則は -45°の回転である。この規則が、ある点\[*X*, *y* \]に対し反復的に実行される、このときに2つの規則がランダムに選択適用され、回転と拡大縮小の規則に関連付けられたパラメーターが用いられる、そして2次元の変換関数によりC曲線に対応する点が得られる。

複素数を使用すると、IFSは以下のように表せる。

  -
    \(f_1(z)=\frac{(1-i)z}{2}\)
    \(f_2(z)=1+\frac{(1+i)(z-1)}{2}\)

初期値は　\(S_0 = \{0,1\}\)

また実数を使用したIFSでも記述できる\[1\]。

\(f_1(x,y) = \begin{bmatrix} \ 0.5 & \ -0.5 \ \\ 0.5 & \ 0.5 \end{bmatrix} \begin{bmatrix} \ x \\ y \end{bmatrix}\)

\(f_2(x,y) = \begin{bmatrix} \ 0.5 & \ 0.5 \ \\ -0.5 & \ 0.5 \end{bmatrix} \begin{bmatrix} \ x \\ y \end{bmatrix} + \begin{bmatrix} \ 0.5 \\ 0.5 \end{bmatrix}\)

上記の式を展開すると、以下の式が得られる。これらの関数を反復的に計算してプロットするとレヴィC曲線を描画できる\[2\]。

*ƒ*<sub>1</sub>

  -
    *x* <sub>*n* + 1</sub> = 0.5 *x* <sub>*n*</sub> - 0.5 *y* <sub>*n*</sub>
    *y* <sub>*n* + 1</sub> = 0.5 *x* <sub>*n*</sub> + 0.5 *y* <sub>*n*</sub>

*ƒ*<sub>2</sub>

  -
    *x* <sub>*n* + 1</sub> = 0.5 *x* <sub>*n*</sub> + 0.5 *y* <sub>*n*</sub> + 0.5
    *y* <sub>*n* + 1</sub> = −0.5 *x* <sub>*n*</sub> + 0.5 *y* <sub>*n*</sub> + 0.5

## コンピュータによる生成

### プログラム構文例

``` java

// Java Sample Implementation of Levy C Curve

import java.awt.Color;
import java.awt.Graphics;
import java.awt.Graphics2D;
import javax.swing.JFrame;
import javax.swing.JPanel;
import java.util.concurrent.ThreadLocalRandom;

public class C_curve extends JPanel {

    public float x, y, len, alpha_angle;
    public int iteration_n;

    public void paint(Graphics g) {
        Graphics2D g2d = (Graphics2D) g;
        c_curve(x, y, len, alpha_angle, iteration_n, g2d);
    }

    public void c_curve(double x, double y, double len, double alpha_angle, int iteration_n, Graphics2D g) {
        double fx = x;
        double fy = y;
        double length = len;
        double alpha = alpha_angle;
        int it_n = iteration_n;
        if (it_n > 0) {
            length = (length / Math.sqrt(2));
            c_curve(fx, fy, length, (alpha + 45), (it_n - 1), g); // Recursive Call
            fx = (fx + (length * Math.cos(Math.toRadians(alpha + 45))));
            fy = (fy + (length * Math.sin(Math.toRadians(alpha + 45))));
            c_curve(fx, fy, length, (alpha - 45), (it_n - 1), g); // Recursive Call
        } else {
            Color[] A = {Color.RED, Color.ORANGE, Color.BLUE, Color.DARK_GRAY};
            g.setColor(A[ThreadLocalRandom.current().nextInt(0, A.length)]); //For Choosing Different Color Values
            g.drawLine((int) fx, (int) fy, (int) (fx + (length * Math.cos(Math.toRadians(alpha)))), (int) (fy + (length * Math.sin(Math.toRadians(alpha)))));
        }
    }

    public static void main(String[] args) {
        C_curve points = new C_curve();
        points.x = 200; // Stating x value
        points.y = 100; // Stating y value
        points.len = 150; // Stating length value
        points.alpha_angle = 90; // Stating angle value
        points.iteration_n = 15; // Stating iteration value

        JFrame frame = new JFrame("Points");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.add(points);
        frame.setSize(500, 500);
        frame.setLocationRelativeTo(null);
        frame.setVisible(true);

    }
}
```

### 表計算ソフトの例

さきの反復関数系を使用し、バーンズリーらにより示されたランダム・アルゴリズム\[3\]\[4\]を適用することでもレヴィC曲線を描画できる。
すなわち、反復関数*ƒ*<sub>1</sub>、*ƒ*<sub>2</sub>をそれぞれ50%の確率でランダムに選択し、反復的に計算を実行すればよい\[5\]。以下に表計算ソフトの入力例を示す。 [代替文=](https://ja.wikipedia.org/wiki/ファイル:Levy_C_curve.jpg "wikilink")

|   | A        | B   | C     | D     | E   | F   | G   | H   |
| - | -------- | --- | ----- | ----- | --- | --- | --- | --- |
| 1 | IFS      | a   | b     | c     | d   | e   | f   | p   |
| 2 | ƒ1       | 0.5 | \-0.5 | 0.5   | 0.5 | 0   | 0   | 0.5 |
| 3 | ƒ2       | 0.5 | 0.5   | \-0.5 | 0.5 | 0.5 | 0.5 |     |
| 4 | random   | ƒ   | X     | Y     |     |     |     |     |
| 5 |          |     | 0     | 0     |     |     |     |     |
| 6 | \=RAND() | B8  | C8    | D8    |     |     |     |     |

なお、B8,C8,D8のセルには以下のような条件判定の関数を入力する。

  - B8=IF(A6\<($H$2),1,2)
  - C8=IF(B6=1,$B$2\*C5+$C$2\*D5+$F$2,$B$3\*C5+$C$3\*D5+$F$3)
  - D8=IF(B6=1,$D$2\*C5+$E$2\*D5+$G$2,$D$3\*C5+$E$3\*D5+$G$3)

最終6行目をオートフィルで適当な行数だけコピーし、XY散布図とするとレヴィC曲線が得られる。各変換式ƒの係数a,b,c,d,e,fと確率pは任意に変更可能である。

各列は以下のような計算を行っている。

  - A列:乱数を発生させる。
  - B列:乱数をもとに確率pに応じた条件判定を行い、用いる変換ƒを決める。
  - C列:先に決めた変換ƒに対応する計算をおこない、Xを求める。
  - D列:先に決めた変換ƒに対応する計算をおこない、Yを求める。
  - 新たなXとYは前の行のXとYの値を使用し、反復的に計算を進める。

## 脚注

<references />

## 参考文献

  - Paul Lévy, *Plane or Space Curves and Surfaces Consisting of Parts Similar to the Whole* (1938), reprinted in *Classics on Fractals* Gerald A. Edgar ed. (1993) Addison-Wesley Publishing .
  - E. Cesaro, *Fonctions continues sans dérivée*, Archiv der Math. und Phys. **10** (1906) pp 57–63.
  - G. Faber, *Über stetige Funktionen II*, Math Annalen, **69** (1910) pp 372–443.
  - S. Bailey, T. Kim, R. S. Strichartz, *Inside the Lévy dragon*, *American Mathematical Monthly* **109(8)** (2002) pp 689–703

## 関連項目

  - [ドラゴン曲線](https://ja.wikipedia.org/wiki/ドラゴン曲線 "wikilink")
  - [ピタゴラスの木](https://ja.wikipedia.org/wiki/ピタゴラスの木 "wikilink")

[Category:アフィン幾何学](https://ja.wikipedia.org/wiki/Category:アフィン幾何学 "wikilink") [Category:フラクタル](https://ja.wikipedia.org/wiki/Category:フラクタル "wikilink")

1.
2.
3.  [p370,"8 Application to Computer Graphics", Fractals Everywhere](https://wwwf.imperial.ac.uk/~jswlamb/M345PA46/%5BB%5D%20chap%20IX.pdf), Boston, MA: Academic Press, 1993,
4.
5.