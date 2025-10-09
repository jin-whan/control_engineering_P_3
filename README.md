# control_engineering_P_3
## 2019732056 최진환
### P3.1
![P3.1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fc2H1Lm%2FbtsQ3jInng2%2FAAAAAAAAAAAAAAAAAAAAAFgqCDpDqnoDiAWcyM2A0f3m1yoa1u7-SeHHAlU-cA1y%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DU0SO1GlPV8lsBnCvfkMVArUu4qM%253D)
운동방정식은  

$$M\ddot{y}+b\dot{y}+ky=F(t)$$

(a) 상태변수는  

$$x_1=y_1$$

$$x_2=\dot{y}_1$$

(b) 상태변수로 표현된 1차 미분방정식은

$$\dot{x}_1=x_2$$

$$\dot{x}_2=-\frac{k}{M}x_1-\frac{b}{M}x_2+\frac{1}{M}F(t)$$

(c) 상태미분방정식은

$$\begin{bmatrix}\dot{x}_1\\\\\dot{x}_2\end{bmatrix}
=\begin{bmatrix}0&1\\\\-\frac{k}{M}&-\frac{b}{M}\end{bmatrix}
\begin{bmatrix}x_1\\\\x_2\end{bmatrix}
+\begin{bmatrix}0\\\\\frac{1}{M}\end{bmatrix}F(t)$$

출력방정식은

$$y=
\begin{bmatrix}1&0\end{bmatrix}
\begin{bmatrix}x_1\\\\x_2\end{bmatrix}
+[0]F(t)
$$

### P3.3
![P3.3](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FcwnAUe%2FbtsQ5jUHjK6%2FAAAAAAAAAAAAAAAAAAAAANx0Qye7i0f3rlkHQCBQqMd-WGzLwskAHwWW5RZMrj8m%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DUmcpbmtzCPFgI%252FgyB9VUwqt4fUE%253D)

$$x_1(t)=i_L(t)$$

$$x_2(t)=v_c(t)$$

KVL을 적용하면

$$v_L=L\frac{di_L}{dt}$$

$$\dot{x}_1=\frac{1}{L}x_2+\frac{1}{L}v_1-\frac{1}{L}v_2 $$

KCL을 적용하면

$$i_c=C\frac{dv_c}{dt}$$

$$\dot{x}_2=\frac{1}{C}x_1+\frac{1}{RC}x_2-\frac{1}{RC}v_2 $$

상태방정식은

$$\begin{bmatrix}\dot{x}_1\\\\\dot{x}_2\end{bmatrix}
=\begin{bmatrix}0&\frac{1}{L}\\\\\frac{1}{C}&\frac{1}{RC}\end{bmatrix}
\begin{bmatrix}x_1\\\\x_2\end{bmatrix}
+\begin{bmatrix}\frac{1}{L}&-\frac{1}{L}\\\\0&-\frac{1}{RC}\end{bmatrix}
\begin{bmatrix}v_1\\\\v_2\end{bmatrix}$$

부분해답과 다르지만 A의 2,1 에서 1/L 이 나오려면 그림과 같이 커패시터의 극성을 사용해야하고 그 극성을 그대로 KCL에 사용하면 부분해답과 부호가 다른 값이 나오게 됩니다.

### P3.5
![P3.5_1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbSCDKD%2FbtsQ2zdK7DB%2FAAAAAAAAAAAAAAAAAAAAAD3a4wd6Go16pQm2Vqwwfqu42_dTkwRQvQC3xA9TA9MP%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DnNFbyqW%252FXrn7UtAJ2WK5GQ3OFEo%253D)
![P3.5_2](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FbmBtbj%2FbtsQ2up7CP0%2FAAAAAAAAAAAAAAAAAAAAAEvaP9qv3d7SnWKHF9XyVej7Q-8L4aukmLA9hzhjwlXN%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D9yGxGFomfP2WyiJKI2qdUgAdkXo%253D)

(a) 순방향 전달함수 G(s)=Y(s)/( R(s)-Y(s) ) 는

$$G(s)=\frac{s+2}{s^3+5s^2-24s}$$

$$T(s)=\frac{G(s)}{1+G(s)}=\frac{s+2}{s^3+5s^2-23s+2}$$

(b) 상태변수 모델은

$$Y(s)=sZ(s)+2Z(s)$$

$$R(s)=s^3Z(s)+5s^2Z(s)-23sZ(s)+2Z(s)$$

$$y(t)=\dot{z}(t)+2z(t)$$

$$r(t)=z^{(3)}(t)+5\ddot{z}(t)-23\dot{z}(t)+2z(t) $$

$$z^{(3)}(t)=-2z(t)+23\dot{z}(t)-5\ddot{z}(t)+r(t) $$

$$x_1=z$$

$$x_2=\dot{z}$$

$$x_3=\ddot{z}$$

$$\begin{bmatrix}\dot{x}_1\\\\\dot{x}_2\\\\\dot{x}_3\end{bmatrix}
=\begin{bmatrix}0&1&0\\\\0&0&1\\\\-2&23&-5\end{bmatrix}
\begin{bmatrix}x_1\\\\x_2\\\\x_3\end{bmatrix}
+\begin{bmatrix}0\\\\0\\\\1\end{bmatrix}r(t)$$

$$y(t)=\begin{bmatrix}2&1&0\end{bmatrix}
\begin{bmatrix}x_1\\\\x_2\\\\x_3\end{bmatrix}$$

### P3.12
![P3.12](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FRs9C8%2FbtsQ3iQfPQO%2FAAAAAAAAAAAAAAAAAAAAAM7nhy_TzMlwE9jdVzsqLGUFWbrNSsFIIvNg0DzyR_JC%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3DHz%252FVNmXb%252BzbTPLNQTPy7Z8tgqPc%253D)

```
syms b0 b1 a0 a1 a2 s
b0 = 40;
b1 = 8;
a0 = 48;
a1 = 44;
a2 = 12;
b = [0 0 b1 b0];
a = [1 a2 a1 a0];
[A B C D] = tf2ss(b,a)

Phi = ilaplace(inv(s*eye(3)-A))
```
(a) 상태공간모델

$$\dot{X}=\begin{bmatrix}\-12&-44&-48\\\\1&0&0\\\\0&1&0\end{bmatrix}X
+\begin{bmatrix}1\\\\0\\\\0\end{bmatrix}R(s)$$

$$Y=\begin{bmatrix}0&8&40\end{bmatrix}X$$

(b) 상태천이행렬

$$\Phi(t)=
\begin{bmatrix}
\frac{1}{2}e^{-2t} - 4e^{-4t} + \frac{9}{2}e^{-6t} & 5e^{-2t} - 32e^{-4t} + 27e^{-6t} & 12e^{-2t} - 48e^{-4t} + 36e^{-6t} \\\\
-\frac{1}{4}e^{-2t} + e^{-4t} - \frac{3}{4}e^{-6t} & -\frac{5}{2}e^{-2t} + 8e^{-4t} - \frac{9}{2}e^{-6t} & -6e^{-2t} + 12e^{-4t} - 6e^{-6t} \\\\
\frac{1}{8}e^{-2t} - \frac{1}{4}e^{-4t} + \frac{1}{8}e^{-6t} & \frac{5}{4}e^{-2t} - 2e^{-4t} + \frac{3}{4}e^{-6t} & 3e^{-2t} - 3e^{-4t} + e^{-6t}
\end{bmatrix}
$$

### P3.17
![P3.17](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fs5RGm%2FbtsQ5iO2pPC%2FAAAAAAAAAAAAAAAAAAAAAE1gBdoHCqEbsTDuopXnt5QP4OJtLl-t56pMF7DBPLO1%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1761922799%26allow_ip%3D%26allow_referer%3D%26signature%3D%252BmVe3hFHX76jkV%252BQpLJSbwk4o8c%253D)

```
syms s
A = [1 1 -1;4 3 0;-2 1 10];
B = [0;0;4];
C = [1 0 0];

Phi=inv(s*eye(3)-A);
G = C*Phi*B
```

$$G(s) = -\frac{4(s - 3)}{s^3 - 14s^2 + 37s + 20}$$

.
.
.
.
.
.
.
.
.
.









