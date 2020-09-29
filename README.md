# Pseudocode Note 1

## Deklarasi dan Assignment Variable

Tipe data pada saat melakukan deklarasi dan assignment sebuah variable harus jelas. Dua penulisan di bawah ini adalah contoh yang diharapkan.

```
// Tipe data ditentukan dari nilai yang diberikan pada variable
STORE variableName WITH <value>

// Tipe data disebutkan dengan jelas, diikuti dengan nilai yang diberikan pada variable
STORE variableName AS <data-type> WITH <value>
```

Sebuah variable dapat memiliki nilai yang ditentukan belakangan. Umumnya, penulisan ini digunakan untuk menggambarkan user input. Dua penulisan di bawah ini adalah contoh yang diharapkan.

```
// data-type dapat diisi dengan tipe data seperti STRING, NUMBER, BOOLEAN, dsb.
STORE variableName WITH ANY <data-type>

// data-type dapat diisi dengan tipe data seperti STRING, NUMBER, BOOLEAN, dsb.
STORE variableName AS <data-type> WITH ANY VALUE
```

## Reassign Variable

Nilai dari sebuah variable dapat diperbarui (reassign). Update nilai variable dapat dilakukan menggunakan keyword `SET ... WITH ...`. Berikut adalah penulisan yang diharapkan.

```
// Deklarasi dan assignment variable
STORE variableName WTIH ANY NUMBER

// Reassign variable
SET variableName WITH 10
```

## Conditional

Pseudocode conditional dapat dituliskan seperti di bawah.

```
IF statement
  ...
ELSE IF statement
  ...
ELSE
  ...
END IF
```

## Mathematical & Re-assignment Operators (+ * x / % dsb)

```
STORE variableName WITH ANY NUMBER

SET variableName WITH variableName PLUS 10        // +=
SET variableName WITH variableName MINUS 10       // -=
SET variableName WITH variableName TIMES 10       // *=
SET variableName WITH variableName DIVIDE BY 10   // /=
SET variableName WITH variableName MODULUS BY 10  // %= modulus (sisa bagi)
```

## Comparison Operators

```
STORE variableName WITH ANY NUMBER

IF variableName MORE THAN 10             // >
  ...
ELSE IF variableName MORE THAN EQUAL 10  // >=
  ...
ELSE IF variableName LESS THAN 10        // <
  ...
ELSE IF variableName LESS THAN EQUAL 10  // <=
  ...
ELSE IF variableName EQUAL 10            // ==
  ...
ELSE IF variableName STRICT EQUAL 10     // ===
  ...
ELSE IF variableName NOT EQUAL 10        // !=
  ...
END IF
```

## Logical Operators (&& || !)
```
IF condition1 AND condition2      // &&
  ...
ELSE IF condition1 OR condition2  // ||
  ...
ELSE IF NOT condition1            // !
  ...
END IF
```

## Display or Print or `console.log`

Jika hendak menampilkan output, kita dapat menggunakan keyword `DISPLAY`.

```
STORE variableName WITH ANY STRING
STORE variableName2 WITH ANY STRING

// Menampilkan nilai variableName
DISPLAY variableName

// Menampilkan nilai variableName2
DISPLAY variableName2

// Menampilkan nilai variableName dan nilai variableName2 yang digabung dengan string lain
DISPLAY "Nilai variableName" CONCAT WITH variableName CONCAT WITH "Nilai variableName2" CONCAT WITH variableName2
```


## Example 1

Hitunglah luas persegi panjang yang memiliki panjang dan lebar

```
ALGORITMA

1. simpan panjang dengan nilai 10cm
2. simpan lebar dengan nilai 10cm
3. hitung panjang dikali lebar (panjang x lebar)
4. simpan hasil kalkulasi kedalam luas
5. tampilkan luas dari persegi panjang

PSEUDOCODE 

STORE length AS NUMBER WITH ANY VALUE 
STORE width AS NUMBER WITH ANY VALUE
STORE area WITH 0

CALCULATE width TIMES height
SET area WITH CALCULATION RESULT

DISPLAY area
```

## Example 1

Buat sebuah pseudocode yang akan menampilkan pesan berdasarkan hasil pembacaan suhu tubuh seseorang. Apabila suhu tubuhnya lebih dari 36 derajat, maka pesan yang ditampilkan adalah `You are sick`. Jika tidak, maka yang ditampilkan adalah `You are healthy`.

```
STORE temperature WITH ANY NUMBER VALUE
IF temperature MORE THAN 36 
    DISPLAY "You are sick"
ELSE
    DISPLAY "You're healthy"
END IF 

```

## Example 2

Kembangkan kode program pada contoh sebelumnya. Apabila uang yang dimiliki orang tersebut kurang dari 1000000, maka tampilkan `You cannot do swab test`. Jika tidak, maka yang ditampilkan adalah `You should do swab test`. Pemeriksaan uang hanya dilakukan jika suhu tubuh orang tersebut lebih dari 36 derajat.

```
STORE temperature WITH ANY NUMBER VALUE
STORE money WITH ANY NUMBER VALUE

IF temperature MORE THAN 36 
    DISPLAY "You are sick"
    IF money MORE THAN EQUAL TO 1000000
        DISPLAY "You should do swab test"
    ELSE
        DISPLAY "You cannot do swab test"
    END IF
ELSE
    DISPLAY "You're healthy"
END IF
```

```
STORE temperature WITH ANY NUMBER VALUE
STORE money WITH ANY NUMBER VALUE
IF temperature MORE THAN 36 
    DISPLAY "You are sick"
ELSE
    DISPLAY "You're healthy"
END IF 
IF temperature MORE THAN 36 AND money MORE THAN EQUAL TO 1000000
    DISPLAY "You should do swab test"
ELSE IF temperature MORE THAN 36 AND money LESS THAN 1000000
    DISPLAY "You cannot do swab test"
END IF 
```
