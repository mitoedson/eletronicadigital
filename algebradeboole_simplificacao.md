<p>
<b>Exercícios:</b>
<p>
(1) X = ~(AB)C + AC + BC
<pre>
Montagem do circuito:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/circuito01_a.jpg" width=250>
</pre>
<pre>
Simplificando:
  X = C (~(AB) + A + B) = C(~A + ~B + A + B) = C((~A + A) + (~B + B)) = C(1 + 1) = C(1) = C
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh01_a.jpg" width=250>
</pre>


<p>
(2) Y = AB + ~AB * A~B + ~AB
<pre>
Simplificando:
  Y = AB + (~A * A * ~B * B) + ~AB = AB + ((~A * A)*(~B * B)) + ~AB = AB + (0 * 0) + ~AB = AB + ~AB + 0 = B(~A + A) + 0 =
    = B(1) + 0 = B + 0 = B
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh02_a.jpg" width=250>
</pre>


<p>
(3) Z = ABC + ~ABC + ~BAC
<pre>
Simplificando:
  Z = C(AB + ~AB + ~BA) = C(A(B + ~B) + ~AB) = C(A(1) + ~AB) = C(A + B) = AC + BC
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh03_a.jpg" width=250>
</pre>


<p>
(4) F = A~B~CD + ~AB~CD + ~AB~C~D + ~A~B~CD + ~~A~B~C~D + AB~C~D + ~A~B~C~D + AB~CD 
<pre>
Simplificando:
  F = ~C(A~BD + ~ABD + ~AB~D + ~A~BD + ~~A~B~D + AB~D + ~A~B~D + ABD) = ~C(A~BD + A~B~D + AB~D + ABD + ~ABD + ~AB~D + ~A~BD + ~A~B~D) = ~C(A(~BD + ~B~D + B~D + BD) + ~A(BD + B~D + ~BD + ~B~D)) =  ~C(A(~B(D + ~D) + B(~D + D)) + ~A(B(D + ~D) + ~B(D + ~D))) = ~C(A(~B(1) + B(1)) + ~A(B(1) + ~B(1))) = ~C(A(~B + B) + ~A(B + ~B)) =  ~C(A(1) + ~A(1)) = ~C(A + ~A) = ~C(1) = ~C   
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh04_a.jpg" width=250>
</pre>


<p>
(5) W = ABC + ~(~BC~A) + ~(ABC)
<pre>
Simplificando:
  W = ABC + B + ~C + A + ~A + ~B + ~C = ABC + (B + ~B) + (A + ~A) + (~C + ~C) = ABC + 1 + 1 + ~C = 1
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh05_a.jpg" width=250>
</pre>


<p>
(6) Y = A~BC + A~B~C + ~(AB) + ~B 
<pre>
Simplificando:
  Y = A~BC + A~B~C + ~(AB) + ~B = A~BC + A~B~C + ~A + ~B + ~B = ~B(AC + A~C) + ~A + (~B + ~B) = ~B(A(C + ~C)) + ~A + (~B + ~B) = ~B(A(1)) + ~A + ~B = (~BA + ~B) + ~A = ~B + ~A = ~(AB) 
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh06_a.jpg" width=250>
</pre>


<p>
(7) Z = A~BC + A~B~C + ~A~B + ~B 
<pre>
Simplificando:
  Z = ~B(AC + A~C) + (~A~B + ~B) = ~B(A(C + ~C)) + ~B = ~B(A(1)) + ~B = ~BA + ~B = ~B
</pre>
<pre>
Utilizando o Mapa de Karnaugh:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Teoria/karnaugh07_a.jpg" width=250>
</pre>

