---
layout: post
title: "
Xác suất cơ bản"
author: "KhanhNV"
tags: Prob
usemathjax: true
---

Xác suất có điều kiện
Với hai biến cố A, B. Xác suất có điều kiện là xác suất của biến cố A với điều kiện biến cố B đã xảy ra.

Công thức:

$$
\begin{equation}
P(A \mid B)=\frac{P(A, B)}{P(B)}
\end{equation}
$$

Suy ra: $$\begin{equation}
P(A, B)=P(A) P(B \mid A)=P(B) P(A \mid B)
\end{equation}$$


Trong đó: P(A,B) hay P(AB) là xác suất của A và B, xảy ra khi cả hai biến cố A, B xảy ra.
Nếu A, B độc lập (biến cố A xảy ra hay không cũng không ảnh hưởng tới biến cố B). Thì: 
P(A,B) = P(A)P(B)

Mở rộng cho n biến cố:
P (A1A2A3...An) = P(A1).P(A2|A1).P(A3|A2A1)...
P(An|A1A2...An-1)
Nếu A1,A2,...An độc lập thì:
P(A1,A2,...An) = P(A1)P(A2)...P(An)

Công thức Xác suất toàn phần và Bayes
a, Công thức Xác suất toàn phần

Cho A1,A2,A3,...An là nhóm biến cố đầy đủ (là nhóm biến cố xung khắc, tổng của chúng bao phủ hết không gian mẫu) 
Nhóm biến cố xung khắc có nghĩa các biến cố trong nhóm đôi một xung khắc với nhau. 2 biến cố xung khắc là hai biến cố không cùng xảy ra trong cùng một phép thử.

P(B) = P(B|A1)P(A1) +P(B|A2)P(A2)+...+P(B|An)P(An)
 P(B) = i=1nP(B)P(B|Ai)

b, Công thức Bayes
P(A|B) = P(B|A)P(A)P(B)

Ví dụ: Phun thuốc trừ sâu cho lúa 3 lần liên tiếp trong 1 tuần. Xác suất sâu bị chết sau lần phun 1 là 0,5. Nếu sâu sống sót thì xác suất sâu bị chết sau lần phun 2 là 0,7. Tương tự sau lần phun 3 là 0,9. Tìm xác suất để sau bị chết sau đợt phun thuốc
Lời giải:
	Gọi Ailà biến cố: "Sâu chết trong lần phun thuốc thứ i", i=1,2,3
	A là biến cố: "Sâu chết trong đợt phun thuốc"
Ta có: A = A1+ A1A2+ A1A2A3
 P(A) = P(A1) +P(A1)P(A2|A1) + P(A1)P(A2|A1)P(A3|A2A1)
	    = 0,5 + 0,5.0,7 + 0,5.(1-0,7).0,9
	    = 0,5 + 0,35 + 0,135 = 0,985

Đại lượng ngẫu nhiên (ĐLNN)
Ví dụ như gieo 1 con xúc xắc, Đại lượng ngẫu nhiên X là số chấm xuất hiện (1,2,3,4,5,6)

	a, Đại lượng ngẫu nhiên rời rạc
Là đại lượng ngẫu nhiên có tập giá trị vô hạn hoặc hữu hạn các số thực
	
Đặc trưng cho ĐLNN rời rạc là bảng phân phối xác suất.
ĐLNN X={x1,x2,...xn}với P{X=xi}=pi
	
	Bảng phân phối xác suất: i=1npi=1
		
X
x1
x2
...
xn
P
p1
p2
...
pn


	b, Đại lượng ngẫu nhiên liên tục
Là đại lượng ngẫu nhiên có tập giá trị trong (a,b) hoặc [a,b]
Mô tả ĐLNN liên tục bằng cách dùng hàm mật độ
Hàm mật độ xác suất dùng để ước lượng độ tập trung xác suất tại lân cận điểm nào đó. 
P(aXb) = abf(x)dx	
Hàm mật độ f(x) là hàm số thỏa mãn 2 điều kiện:
f(x)0; x(-,+)
-+f(x)dx =1

Kỳ vọng, phương sai, độ lệch chuẩn
a, Kỳ vọng
Là giá trị trung bình mà ĐLNN đó nhận được
Ký hiệu: E(X)

E(X) = i=1nxipi nếu X là ĐLNN rời rạc
E(X) = -+x.f(x)dx nếu X là ĐLNN liên tục

Ví dụ: Cho X là ĐLNN rời rạc và có bảng phân phối như sau:

X
-1
0
2
3
5
P
0,1
0,2
0,1
0,3
0,3


Tính E(X)
Lời giải:
E(X) = i=15xipi= -1.0,1 + 0.0,2 + 2.0,1 + 3.0,3 + 5.0,3 = 2,5

b, Phương sai 
Đánh giá mức độ phân tán của các giá trị X quanh E(X)
Phương sai nhỏ: Mức độ tập trung của X quanh E(X) cao
Phương sai lớn: Mức độ phân tán lớn, các giá trị X càng xa E(X)
Ký hiệu: D(X)

D(X) = E(X - E(X))2 hay D(X) = E((X-)2) 
với =E(X)
Biểu thức tương đương: D(X) = E(X2) -(E(X))2

Trong đó: E(X2)= i=1nxi2pi nếu X rời rạc
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






