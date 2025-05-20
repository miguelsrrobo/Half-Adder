## Half-Adder


<p align = "center">
  <img src="https://github.com/miguelsrrobo/Half-Adder/blob/main/half-adder.png" alt="Rinha logo" width="30%" />
</p>

## 🔹 O que é um Half-Adder?

Um **Half-Adder** é um circuito lógico **combinacional** que realiza a soma de dois bits: `A` e `B`.

Ele produz dois resultados:

* **Soma (Sum ou S)**: o bit resultante da soma.
* **Carry (C ou Cout)**: o bit de "vai um" (retenção), caso a soma ultrapasse 1.

---

## 🔹 Tabela-Verdade do Half-Adder

| A | B | Soma (S) | Carry (C) |
| - | - | -------- | --------- |
| 0 | 0 | 0        | 0         |
| 0 | 1 | 1        | 0         |
| 1 | 0 | 1        | 0         |
| 1 | 1 | 0        | 1         |

---

## 🔹 Expressões Lógicas

* **Soma (S)** = `A XOR B`
* **Carry (C)** = `A AND B`

---

## 🔹 Implementação em Verilog (Exemplo)

```verilog
module half_adder (
    input A,
    input B,
    output Sum,
    output Carry
);

assign Sum = A ^ B;      // XOR
assign Carry = A & B;    // AND

endmodule
```

---

## 🔹 Aplicações

O Half-Adder é usado como bloco básico em:

* **Full-Adders** (Somador Completo)
* **Somadores em cascata** para somar números binários maiores
* **ALUs** (Unidades Lógicas e Aritméticas)
