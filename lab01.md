<h3>Prática 01</h3>

Utilizando o Quartus Prime Lite Edition, utilizar duas entradas que controlam dois leds através do Verilog. Esta primeira prática tem como objetivo fazer uma introdução do programa Quartus, e realizar a simulação através do Questa Intel Started FPGA.

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
<img src="https://github.com/mitoedson/eletronicadigital/blob/Labs/Clipboard01.jpg">


