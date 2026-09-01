# 🧵 Text Processing (sed, awk, cut, tr)

## 🩹 sed — Stream Editor

Replace first "test" per line, PRINT result only (file unchanged)

```bash
sed 's/test/TestAI/' server.txt
```

Same, but edit the file in place (`-i`)

```bash
sed -i 's/test/TestAI/' server.txt
```

Replace ALL occurrences per line (`g` = global), in place

```bash
sed -i 's/test/TestAI/g' server.txt
```

Delete line 1

```bash
sed -i '1d' server.txt
```

Insert text before line 4

```bash
sed -i '4i\welcome to' server.txt
```

Delete the last line (`$` = last line)

```bash
sed -i '$d' server.txt
```

Append text after the last line

```bash
sed -i '$a\You like devops' server.txt
```

Strip Windows CRLF line endings (fix `\r` issues)

```bash
sed -i 's/\r$//' server.sh
```

## 📊 awk — Pattern Scanning & Column Processing

Print first column (fields split by whitespace)

```bash
awk '{print $1}' server.txt
```

Print second column, using "," as field separator

```bash
awk -F',' '{print $2}' data.csv
```

Print line number + full line

```bash
awk '{print NR, $0}' server.txt
```

## ✂️ cut / tr — Quick Field & Character Tools

Extract field 1 using "," as delimiter

```bash
cut -d',' -f1 data.csv
```

Extract characters 1-5 of each line

```bash
cut -c1-5 server.txt
```

Convert lowercase to uppercase

```bash
tr 'a-z' 'A-Z' < server.txt
```

Delete all spaces

```bash
tr -d ' ' < server.txt
```
