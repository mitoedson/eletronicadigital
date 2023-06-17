<h3>Prática 00</h3>

<b>Código</b>
<pre>
/* ----------------------------------------------------------------------------
  Company:    UFABC - Engenharia de Informação - CECS
  Engineer:   João Ranhel  
  Create Date:    03/06/2017 
  
  Design Name:    Praticas de Eletrônica Digital (ESTI002-17)
  Module Name:    circuito_01
  Language:       Verilog-2001
  
Descrição: 
Este circuito é apenas para testarmos entradas e saídas do FPGA.
Nenhuma função lógica será executada, apenas a entrada gera uma saída!
Finalidade:
Entender o que é um "module", o que é in/out e usar o Quartus / Pin-Planner
-----------------------------------------------------------------------------*/

module circuito_01      // nome do módulo = nome do arquivo.v
  (
  input a, b,           // ports in: conecte às chaves sliders
  output led1, led2     // port out: conecte a um LED na placa!
  );
  
  assign led1 = a;      // a chave "a" liga o led1
  assign led2 = b;      // a chave "b" liga o led2
    
endmodule
  
// -------------- final do código --------------------------
</pre>
