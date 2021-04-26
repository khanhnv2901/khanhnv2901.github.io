---
layout: post
title: "
Xác suất cơ bản"
author: "KhanhNV"
tags: Prob
usemathjax: true
toc: true
---

Lý thuyết xác suất là công cụ cơ bản và là tiền đề cho học máy. Việc nắm vững lý thuyết xác suất rất quan trọng. Trong phần này, tôi sẽ tóm lược lại một số lý thuyết cơ bản.


<aside markdown="1">
<h2>Mục lục</h2>
* ToC
{:toc}
</aside>


# 1.Xác suất có điều kiện


Với hai biến cố $A$, $B$. Xác suất có điều kiện là xác suất của biến cố $A$ với điều kiện biến cố $B$ đã xảy ra.

Công thức:

$$
\begin{equation}
P(A \mid B)=\frac{P(A, B)}{P(B)}
\end{equation}
$$

Suy ra: 	$$\begin{equation}
P(A, B)=P(A) P(B \mid A)=P(B) P(A \mid B)
\end{equation}$$


Trong đó: $P(A,B)$ hay $P(AB)$ là xác suất của $A$ và $B$, xảy ra khi cả hai biến cố $A$, $B$ xảy ra.

  - Nếu $A, B$ độc lập (biến cố $A$ xảy ra hay không cũng không ảnh hưởng tới biến cố $B$). Thì: 

$$
\begin{equation}
P(A,B) = P(A)P(B)
\end{equation}
$$

* Mở rộng cho n biến cố:

$$
\begin{equation}
P(A_1 A_2 A_3 \ldots A_n) = P(A_1).P(A_2 \mid A_1).P(A_3 \mid A_2 A_1) \ldots P(A_n \mid A_1 A_2 \ldots A_(n-1))
\end{equation}
$$

* Nếu $A_1, A_2, \ldots ,A_n$ độc lập thì:

$$
\begin{equation}
P(A_1,A_2, \ldots ,A_n) = P(A_1)P(A_2) \cdots P(A_n)
\end{equation}
$$

# 2.Công thức Xác suất toàn phần và Bayes
## 2.1 Công thức Xác suất toàn phần

Cho $A_1, A_2, A_3, \ldots ,A_n$ là nhóm biến cố đầy đủ (là nhóm biến cố xung khắc, tổng của chúng bao phủ hết không gian mẫu) 

Nhóm biến cố xung khắc có nghĩa các biến cố trong nhóm đôi một xung khắc với nhau. 2 biến cố xung khắc là hai biến cố không cùng xảy ra trong cùng một phép thử.

$$
\begin{equation}
P(B) = P(B \mid A_1)P(A_1) + P(B \mid A_2)P(A_2) + \cdots + P(B \mid A_n)P(A_n)
\end{equation}
$$

Công thức rút gọn: 

$$
\begin{equation}
P(B) = \sum_{i=1}^{N} P(B)P(B \mid A_i)
\end{equation}
$$

## 2.2 Công thức Bayes

$$
\begin{equation}
P(A \mid B) = P(B \mid A)P(A)P(B)
\end{equation}
$$

* Ví dụ: Phun thuốc trừ sâu cho lúa 3 lần liên tiếp trong 1 tuần. Xác suất sâu bị chết sau lần phun 1 là 0,5. Nếu sâu sống sót thì xác suất sâu bị chết sau lần phun 2 là 0,7. Tương tự sau lần phun 3 là 0,9. Tìm xác suất để sau bị chết sau đợt phun thuốc
	> *Lời giải:*
	>
	> Gọi $A_i$ là biến cố: "Sâu chết trong lần phun thuốc thứ $i$", $i$=1,2,3
	> 
	> $A$ là biến cố: "Sâu chết trong đợt phun thuốc"
	> 
	> Ta có: $A = A_1 + A_1 A_2 + A_1 A_2 A_3$
	> 
	> Suy ra:
	> 
	> $P(A) = P(A_1) + P(A_1)P(A_2 \mid A_1) + P(A_1)P(A_2 \mid A_1)P(A_3 \mid A_2 A_1)$
	> 
	> = 0,5 + 0,5.0,7 + 0,5.(1-0,7).0,9
	> 
	> = 0,5 + 0,35 + 0,135 = 0,985


# 3. Đại lượng ngẫu nhiên (ĐLNN)

* Ví dụ như gieo 1 con xúc xắc, Đại lượng ngẫu nhiên $X$ là số chấm xuất hiện $(1,2,3,4,5,6)$

## 3.1 Đại lượng ngẫu nhiên rời rạc

* Là đại lượng ngẫu nhiên có tập giá trị vô hạn hoặc hữu hạn các số thực
	
* Đặc trưng cho ĐLNN rời rạc là bảng phân phối xác suất.

* ĐLNN $X = {x_1, x_2, \ldots ,x_n}$ với $P{X = x_i}=p_i$
	
	Bảng phân phối xác suất: $\sum_{i=1}^{N} P_i = 1$

	|:--------------|:-----------|:-------------|:-------------:|:-------------|
	| $X$           | $x_1$      | $x_2$        | ...           | $x_n$        |
	|:--------------|:-----------|:-------------|:-------------:|:-------------|
	| $P$           | $p_1$      | $P_2$        | ...           | $p_n$        |
	


## 3.2 Đại lượng ngẫu nhiên liên tục

Là đại lượng ngẫu nhiên có tập giá trị trong $(a,b)$ hoặc $[a,b]$

* Mô tả ĐLNN liên tục bằng cách dùng hàm mật độ

* Hàm mật độ xác suất dùng để ước lượng độ tập trung xác suất tại lân cận điểm nào đó. 

$$
\begin{equation}
P(a \leq X \leq b) = \int_{a}^{b} f(x) \,dx 
\end{equation}
$$
	
* Hàm mật độ f(x) là hàm số thỏa mãn 2 điều kiện:
	* $ f(x) \geq 0; \forall x \in (- \infty , + \infty ) $
	* $ \int_{- \infty}^{+ \infty} f(x) \,dx = 1 $

# 4. Kỳ vọng, phương sai, độ lệch chuẩn
## 4.1 Kỳ vọng

* Là giá trị trung bình mà ĐLNN đó nhận được

* Ký hiệu: E(X)

$$
\begin{equation}
E(X) = \sum_{i=1}^n x_i p_i nếu X là ĐLNN rời rạc
\end{equation}
$$

$$
\begin{equation}
\int_{- \infty}^{+ \infty} x f(x) \,dx nếu X là ĐLNN liên tục
\end{equation}
$$


* *Ví dụ*: Cho $X$ là ĐLNN rời rạc và có bảng phân phối như sau:


	|:--------------|:-----------|:-------------|:--------------|:-------------|:-------------|
	| $X$           | -1         | 0            |2              | 3            | 5            |
	|:--------------|:-----------|:-------------|:--------------|:-------------|:-------------|
	| $P$           | 0.1        | 0.2          | 0.1           | 0.3          | 0.3          |


	* Tính E(X)
	
	> Lời giải:\\
	> E(X) = $ \sum_{i=1}^5 x_i p_i $ = -1.0,1 + 0.0,2 + 2.0,1 + 3.0,3 + 5.0,3 = 2,5

## 4.2 Phương sai 
* Đánh giá mức độ phân tán của các giá trị X quanh E(X)
* Phương sai nhỏ: Mức độ tập trung của X quanh E(X) cao
* Phương sai lớn: Mức độ phân tán lớn, các giá trị X càng xa E(X)
* Ký hiệu: D(X)

$$
\begin{equation}
D(X) = E(X - E(X))^2 hay D(X) = E((X - \mu)^2) với \mu = E(X)
\end{equation}
$$

Biểu thức tương đương: $ D(X) = E(X^2) -(E(X))^2 $

Trong đó: E(X^2)= \sum_{i=1}^5 x_i ^2 p_i nếu X rời rạc
	       E(X2)= -+x2f(x)dx nếu X liên tục
c, Độ lệch chuẩn 
	Kí hiệu:  
=D(X)

	Vì phương sai là bình phương giá trị trung bình của các khoảng cách từ các giá trị của X tới giá trị trung bình của nó. Nên dễ dẫn tới các giá trị sai. Vì vậy chúng ta đưa nó về giá trị gốc bằng cách căn, giá trị này được gọi là độ lệch chuẩn.

Phân phối xác suất
5.1. Đối với đại lượng ngẫu nhiên rời rạc
 a, Phân phối nhị thức 
	Là phân phối khi tiến hành n lần phép thử Bernoulli. Gọi X là số lần xuất hiện biến cố A với P(A) = p, p R, 0p1

Phép thử Bernoulli:
	Ý nghĩa: xác suất để A xuất hiện đúng m lần trong n lần thực hiện một phép thử. (n phép thử độc lập)

	Công thức: Pn(m,p) = Cnmpm(1-p)n-m

Ví dụ phép thử Bernoulli: Xác suất trúng đích của một xạ thủ là 0,7. Tìm xác suất để xạ thủ này bắn 5 viên đạn thì 4 viên trúng đích.

	Lời giải:
	Gọi A là biến cố: "Xạ thủ bắn trúng đích"
	Ta có P(A) = 0,7.
	Gọi B là biến cố: "Xạ thủ bắn 5 viên trúng đích 4 viên"
	Áp dụng công thức với n=5, m=4, p=0,7
	
	Ta có: P(B) = Pn(m,p) = Cnmpm(1-p)n-m
				        = C54.0,74.(1-0,7)5-4 = 0,36015
	Vậy xác suất để xạ thủ bắn 5 viên có 4 viên trúng đích là 0,36015

Trở lại với phân phối nhị thức:
Nói ngắn gọn, Phân phối nhị thức thể hiện xác suất để X lần thành công trong n phép thử, với xác suất thành công p của mỗi phép thử.

Công thức:  P(X=x) = Cnx.px.(1-p)n-x, với x=0,1,2..n

Tính chất: E(X) = np, D(X) = np(1 - p)

Ta nói X tuân theo phân phối nhị thức:  X Bin(n,p)

Có thể thấy phép thử Bernoulli là trường hợp đặc biệt của phân phối nhị thức với n = 1, Bin(1,p)

b, Phân phối Poisson
	-Là phân phối nhị thức với trường hợp n rất lớn, p rất nhỏ. 
Đặt  = np. Ta có:
	p(x) = Cnx.px.(1-p)n-x = n!x!(n-x)! .(n)x.(1-n)n-x
	       = n!nx.(n-x)! .xx!.(1-n)n-x


Vì n rất lớn nên (1-n)x1, (1-n)ne- , với e = n(1+1n)n và n!nx.(n-x)! 1 nên suy ra: p(x) xx!.e-

Tính chất: E(X) = D(X) = 

Ta nói X tuân theo phân phối Poisson: XP()

Ví dụ: Một máy dệt có 5000 ống sợi, xác suất trong một phút một ống sợi bị đứt là 0,0002. Tìm xác suất để trong 1 phút không quá 2 ống sợi bị đứt.

Lời giải: 

Gọi X là ĐLNN chỉ số ống sợi bị đứt.
Do n lớn, và p nhỏ nên XP() với =np = 5000.0,002 = 1

Xác suất để trong 1 phút có không quá 2 sợi bị đứt là:
P(X2) = P(X=0) + P(X=1) + P(X=2)
	     = 00!.e-1+ 11!.e-1+ 22!.e-1= 0,9225
Vậy xác suất trong 1 phút có không quá 2 sợi bị đứt là 0,9225






