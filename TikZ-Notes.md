# 1. 绘制直线和曲线
## 1.1 绘制直线
### 1.1.1 基本语法
```latex
\begin{tikzpicture}
\draw (0,0) --(1,2);
\end{tikzpicture}
```
### 1.1.2 绘制带有网格的
```latex
\begin{tikzpicture}
\draw (0,0) --(1,2) -- (2,3) -- (1,0);
\draw[help lines] (0,0) grid (2,3);  %网格及其范围
\end{tikzpicture}
```
## 1.2 放大图像
### 1.2.1 基本语法
```latex
\begin{tikzpicture}[scale=3] %横纵均放大3倍
\draw (0,0) -- (1,1);
\end{tikzpicture}

```
### 1.2.3 控制放大维度
```latex
\begin{tikzpicture}[xscale=3] %以x轴放大及其放大倍数
\draw (0,0) -- (1,1);
\end{tikzpicture}
```
```latex
\begin{tikzpicture}[xscale=2.5,yscale=0.5] %x、y轴放大及放大倍数
\draw (0,0) -- (1,1);
\end{tikzpicture}
```
## 1.3 向量及坐标轴
### 1.3.1 向量基本语法
```latex
both extremities:
\begin{tikzpicture}
\draw [->] (0,0) -- (2,0);
\draw [<-] (0, -0.5) -- (2,-0.5);
\draw [|->] (0,-1) -- (2,-1);
\end{tikzpicture}
```
### 1.3.2 坐标轴
```latex
axes (we will see later how to label them):
\begin{tikzpicture}
\draw [<->] (0,2) -- (0,0) -- (3,0); %%%注意语法
\end{tikzpicture}
```
## 1.4 线的粗细
### 1.4.1 基本语法
```latex
\begin{tikzpicture}
\draw [ultra thick] (0,1) -- (2,1);
\draw [thick] (0,0.5) -- (2,0.5);
\draw [thin] (0,0) -- (2,0);
\end{tikzpicture}
```
### 1.4.2 绘制灰色的辅助线
```latex
\begin{tikzpicture}
\draw [<->] (0,2) -- (0,0) -- (4,0);
\draw [thick] (0,1.5) -- (3,0);
\draw [ultra thick] (0,0) -- (2,2);
\draw [help lines] (1,0) -- (1,1) -- (0,1);
\end{tikzpicture}
```
### 1.4.3 自定义粗细（2种度量方法）
```latex
\begin{tikzpicture}
\draw [line width=12] (0,0) -- (2,0);
\draw [line width=0.2cm] (4,.75) -- (5,.25);
\end{tikzpicture}
```
## 1.5 虚线和点
### 1.5.1 基本语法
```latex
\begin{tikzpicture}
\draw [dashed, ultra thick] (0,1) -- (2,1); %虚线，粗细
\draw [dashed] (0, 0.5) -- (2,0.5); %虚线
\draw [dotted] (0,0) -- (2,0); %点线
\end{tikzpicture}
```
## 1.6 颜色
### 1.6.1 基本语法
```latex
\begin{tikzpicture}
\draw [gray] (0,1) -- (2,1);
\draw [red] (0, 0.5) -- (2,0.5);
\draw [blue] (0,0) -- (2,0);
\end{tikzpicture}
```
## 1.7 应用
### 1.7.1 适当的颜色、粗细使用在文本中即为高亮
```latex
\draw [yellow, line width=6]
(0,0) -- (.5,0); \end{tikzpicture}
```
## 1.8 曲线
### 1.8.1 基本语法
```latex
\begin{tikzpicture}
\draw [blue] (0,0) rectangle (1.5,1);
\draw [red, ultra thick] (3,0.5) circle [radius=0.5];;
\draw [gray] (6,0) arc [radius=1, start angle=45, end angle= 120]; %arc 弧
\end{tikzpicture}
```
### 1.8.2 倒角
```latex
\begin{tikzpicture}
\draw [<->, rounded corners, thick, purple] (0,2) -- (0,0) -- (3,0);
\end{tikzpicture}
```
### 1.8.3 多个点绘制曲线（利用Mathematica等获取点列）
```latex
\begin{tikzpicture}[xscale=25,yscale=5]
\draw [<->, help lines] (0.6,1.34) -- (0.6,1) -- (1.05,1);
\draw[orange] (0.6, 1.0385) --
(0.61, 1.06372) -- (0.62, 1.08756) -- (0.63, 1.11012) -- (0.64,
1.13147) -- (0.65, 1.15166) -- (0.66, 1.17074) -- (0.67, 1.18874) -- (0.68,
1.20568) -- (0.69, 1.22157) -- (0.7, 1.23643) -- (0.71, 1.25026) -- (0.72,
1.26307) -- (0.73, 1.27486) -- (0.74, 1.28561) -- (0.75, 1.29534) -- (0.76,
1.30402) -- (0.77, 1.31165) -- (0.78, 1.31821) -- (0.79, 1.32369) -- (0.8,
1.32806) -- (0.81, 1.33131) -- (0.82, 1.3334) -- (0.83, 1.33431) -- (0.84,
1.334) -- (0.85, 1.33244) -- (0.86, 1.32956) -- (0.87, 1.32533) -- (0.88,
1.31966) -- (0.89, 1.3125) -- (0.9, 1.30373) -- (0.91, 1.29325) -- (0.92,
1.2809) -- (0.93, 1.26649) -- (0.94, 1.24976) -- (0.95, 1.23032) -- (0.96,
1.2076) -- (0.97, 1.18065) -- (0.98, 1.14763) -- (0.99, 1.1038) -- (0.991,
1.09836) -- (0.992, 1.09261) -- (0.993, 1.0865) -- (0.994, 1.07994) -- (0.995,
1.07282) -- (0.996, 1.06497) -- (0.997, 1.0561) -- (0.998, 1.04563) -- (0.999,
1.03209) -- (0.9991, 1.03042) -- (0.9992, 1.02866) -- (0.9993,
1.02679) -- (0.9994, 1.02478) -- (0.9995, 1.0226) -- (0.9996, 1.02019) -- (0.9997,
1.01747) -- (0.9998, 1.01424) -- (0.9999, 1.01005) -- (0.9999,
1.01005) -- (0.99991, 1.00953) -- (0.99992, 1.00898) -- (0.99993,
1.0084) -- (0.99994, 1.00778) -- (0.99995, 1.0071) -- (0.99996,
1.00634) -- (0.99997, 1.00549) -- (0.99998, 1.00448) -- (0.99999, 1.00317) -- (1,
1) ;
\end{tikzpicture}
```
### 1.8.4 简便方法绘制曲线
```latex
\begin{tikzpicture}
\draw[very thick] (0,0) to [out=90,in=195] (2,1.5); %坐标从(0,0)到(2,1.5)，切线角度从90°到195°
\end{tikzpicture}
```
### 1.8.5 应用举例 绘制长曲线
```latex
\begin{tikzpicture}
\draw [<->,thick, cyan] (0,0) to [out=90,in=180] (1,1)
to [out=0,in=180] (2.5,0) to [out=0,in=-135] (4,1) ;
\draw[help lines] (0,0) grid (1,4);
\end{tikzpicture}
```
## 1.9 绘制函数
### 1.9.1 应用举例
```latex
\begin{tikzpicture}[xscale=13,yscale=3.8]
\draw [<->] (0,0.8) -- (0,0) -- (0.5,0);
\draw[green, ultra thick, domain=0:0.5] plot (\x, {0.025+\x+\x*\x});
\end{tikzpicture}
```
```latex
\begin{tikzpicture}[yscale=1.5]
\draw [help lines, <->] (0,0) -- (6.5,0);
\draw [help lines, ->] (0,-1.1) -- (0,1.1);
\draw [green,domain=0:2*pi] plot (\x, {(sin(\x r)* ln(\x+1))/2});
\draw [red,domain=0:pi] plot (\x, {sin(\x r)});
\draw [blue, domain=pi:2*pi] plot (\x, {cos(\x r)*exp(\x/exp(2*pi))});
\end{tikzpicture}
```



# 2 填充区域
## 2.1 填充简单的几何图形
### 2.1.1 代码示例
```latex
\begin{tikzpicture}
 %fill只填充几何图形内，默认黑色，图形颜色想全部统一要改变框线颜色
\draw [fill=red,ultra thick] (0,0) rectangle (1,1);
\draw [fill=red,ultra thick,red] (2,0) rectangle (3,1);
\draw [blue, fill=blue] (4,0) -- (5,1) -- (4.75,0.15) -- (4,0);
\draw [fill] (7,0.5) circle [radius=0.1];
\draw [fill=orange] (9,0) rectangle (11,1);
\draw [fill=white] (9.25,0.25) rectangle (10,1.5);

%\path可无边框
\begin{tikzpicture}
\path [fill=gray] (0,0) rectangle (1.5,1);
\draw [fill=yellow] (2,0) rectangle (3.5,1);
\end{tikzpicture}

\end{tikzpicture}
```
## 2.2 填充任意区域
### 2.2.1 代码示例
```latex
\begin{tikzpicture}
\draw [ultra thick] (0,0) to [out=87,in=150] (1,1) -- (.85,.15) -- (0,0);
\draw [ultra thick, fill=purple] (2,0) to [out=87,in=150] (3,1) -- (2.85,.15) -- (2,0);
\path [fill=purple] (4,0) to [out=87,in=150] (5,1) -- (4.85,.15) -- (4,0);
\end{tikzpicture}
```
# 3 在图片中插入标签
## 3.1 代码示例
### 3.1.1 正中心
```latex
\begin{tikzpicture}
\draw [thick, <->] (0,2) -- (0,0) -- (2,0);
\node at (1,1) {yes}; %yes在坐标(1,1)的正中心
\end{tikzpicture}
```
### 3.1.2 上、下、左、右
```latex
\begin{tikzpicture}
\draw [thick, <->] (0,2) -- (0,0) -- (2,0);
\draw[fill] (1,1) circle [radius=0.025];
\node [below] at (1,1) {below};
\node [above] at (1,1) {above};
\node [left] at (1,1) {left};
\node [right] at (1,1) {right};
\end{tikzpicture}
```
### 3.1.3 上、下/左、右
```latex
\begin{tikzpicture}[scale=2]
\draw [thick, <->] (0,1) -- (0,0) -- (1,0);
\draw[fill] (1,1) circle [radius=0.025];
\node [below right, red] at (.5,.75) {below right};
\node [above left, green] at (.5,.75) {above left};
\node [below left, purple] at (.5,.75) {below left};
\node [above right, magenta] at (.5,.75) {above right};
\end{tikzpicture}
```
### 3.1.4 应用举例
```latex
%This makes it possible to label axes and points:
\begin{tikzpicture}[xscale=3, yscale=1.5]
\draw [thick, <->] (0,1) -- (0,0) -- (1,0);
\node [below right] at (1,0) {$x$};
\node [left] at (0,1) {$y$};
\draw[fill] (.4,.6) circle [radius=.5pt];
\node[above right] (.4,.6) {$A$};
\end{tikzpicture}

%The same result by other codes
\begin{tikzpicture}[xscale=3, yscale]
\draw [thick, <->] (0,1) node [left] {$y$}
-- (0,0) -- (1,0) node [below right] {$x$};
\draw[fill] (.4,.6) circle [radius=.5pt]
node[above right] (.4,.6) {$A$};
\end{tikzpicture}
```
```latex
\begin{tikzpicture}[xscale=1.3]
\draw [thick] (0,0) -- (9,0);
\draw (0,-.2) -- (0, .2);
\draw (3,-.2) -- (3, .2);
\draw (6,-.2) -- (6, .2);
\draw (9,-.2) -- (9, .2);
\node[align=left, below] at (1.5,-.5)%
{This happens\\in period 1\\and is aligned\\ left};
\node[align=center, below] at (4.5,-.5)%
{This happens\\in period 2\\and is centered};
\node[align=right, below] at (7.5,-.5)%
{This happens\\in period 2\\and is right\\aligned};
\end{tikzpicture}
```


# 4 与Beamer结合
### 应用举例
```latex
\begin{frame}
a few lines
\begin{center}
\begin{tikzpicture}
\draw [blue, ultra thick] (-1,2) -- (6,3);
\uncover<1>{\draw [green,thick] (-4,3) -- (2,2.5);}
\uncover<2>{\draw [red,thick] (0,0) -- (0,5);}
\end{tikzpicture}
\end{center}
and something under.
\end{frame}
```