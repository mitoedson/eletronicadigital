<h3>Prática 01</h3>

<b>Código</b>
<pre>
/* ----------------------------------------------------------------------------
  Company:    UFABC - Engenharia de Informação - CECS
  Engineer:   João Ranhel  
  Create Date:    10/05/2017 
  
  Design Name:    Praticas de Eletrônica Digital (ESTI002-17)
  Module Name:    controle_da_lampada
  Language:       Verilog-2001
  
Descrição: 
Circuito que controla uma lâmpada por múltiplos interruptores - PROJETO #1 
O estilo utilizado é dataflow (somente conexão entre portas lógicas)
Equação a implementar (Projeto #1): L = ~A.~B.C + ~A.B.~C + A.~B.~C + A.B.C
-----------------------------------------------------------------------------*/

module controle_da_lampada             // nome do módulo = nome do arquivo.v
  (
  input a, b, c,                       // ports in: conecte às chaves sliders
  output l                             // port out: conecte a um LED na placa!
  );
  
  wire x1, x2, x3, x4;                 // requer4 fios intermediários (x1..x4)
  
  assign x1 = ~a & ~b & c;             // 1o. termo da equação
  assign x2 = ~a & b & ~c;             // 2o. termo da equação
  assign x3 = a & ~b & ~c;             // 3o. termo da equação
  assign x4 = a & b & c;               // 4o. termo da equação
  
  assign l = x1 | x2 | x3 | x4;        // soma de produtos final...
    
endmodule
  
// -------------- final do código LONGO da prática 01 --------------------------
</pre>

<b>Simulação no Questa</b>
<p>
<img src="https://github.com/mitoedson/eletronicadigital/blob/Labs/Clipboard02.jpg">
<p>
<b>Comentários</b><br>
Quando uma das três variáveis recebe um sinal de entrada, o led 'l' acenderá. No entanto, caso um outro sinal de entrada é recebido por outra variável, o led se apagará. Ou seja, o led somente se acenderá quando apenas uma variável, ou todas as três variáveis receberem o sinal de entrada. Caso contrário, o led se apagará.
<p>
O código pode ser simplificado como abaixo:
<pre>
 module Projeto01             // nome do módulo = nome do arquivo.v
  (
  input a, b, c,                       // ports in: conecte às chaves sliders
  output l                             // port out: conecte a um LED na placa!
  );
  
  assign l = (~a & ~b & c) | (~a & b & ~c) | (a & ~b & ~c) | a & b & c;        // soma de produtos final...
endmodule 
</pre>
<p>
Ou simplificando mais um pouco, utilizando a porta XOR (^)...
<pre>
module Projeto01             // nome do módulo = nome do arquivo.v
  (
  input a, b, c,                       // ports in: conecte às chaves sliders
  output l                             // port out: conecte a um LED na placa!
  );
  
  assign l = a ^ b ^ c;        // soma de produtos final...
endmodule 
</pre>
<p>
Inserindo mais uma variável, temos:
<pre>
module Projeto01             // nome do módulo = nome do arquivo.v
  (
  input a, b, c, d,                     // ports in: conecte às chaves sliders
  output l                             // port out: conecte a um LED na placa!
  );
  
  assign l = a ^ b ^ c ^ d;        // soma de produtos final...
endmodule
</pre>
<p>
Obtemos a seguinte forma de onda:
<img src="https://github.com/mitoedson/eletronicadigital/blob/Labs/Clipboard03.jpg">
