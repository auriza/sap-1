# SAP-1: Komputer 8-bit Sederhana

## Format instruksi

SAP-1 adalah komputer 8-bit sederhana, dengan format instruksi: 4-bit MSB adalah *opcode* dan 4-bit LSB adalah alamat memori.

| Opcode | Mnemonic | Operation                              |
| ------ | -------- | -------------------------------------- |
| 0      | HLT      | Stop execution                         |
| 1      | LDA      | Load memory address content to A       |
| 2      | ADD      | Add memory address content to A        |
| 3      | SUB      | Subtract memory address content from A |
| 4      | STA      | Store A content to memory address      |
| 5      | LDI      | Load immediate value to A              |
| 6      | JMP      | Jump to memory address                 |
| 7      | OUT      | Load A content to output               |
| 8      | JZ       | Jump to memory address if zero         |
| 9      | JC       | Jump to memory address if carry        |

## Contoh program

Berikut adalah contoh program untuk menambahkan isi memori alamat #4 dengan isi memori #5, dan hasilnya dicetak ke keluaran.

```
LDA 4
ADD 5
OUT
HLT
```

Kemudian kode assembly di atas diubah menjadi kode mesin seperti berikut. Misalnya isi memori #4 dan #5 adalah 03 dan 04, maka keluaran program ini adalah 07.

```
14 25 70 00   03 04 00 00
```

Kode mesin di atas langsung dimasukkan ke RAM pada Logisim.

## Struktur komputer

Download: [sap-1.circ](sap-1.circ)

![SAP-1 Logisim](count.gif)

## Referensi

<https://www.youtube.com/watch?v=AwUirxi9eBg&list=PLowKtXNTBypGqImE405J2565dvjafglHU&index=35>
