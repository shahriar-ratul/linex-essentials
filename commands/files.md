# Text Processing (sed, awk, cut, tr)

## sed — Stream Editor

sed 's/test/TestAI/' server.txt        // replace first "test" per line, PRINT result only (file unchanged)
sed -i 's/test/TestAI/' server.txt     // same, but edit the file in place (-i)
sed -i 's/test/TestAI/g' server.txt    // replace ALL occurrences per line (g = global), in place

sed -i '1d' server.txt                 // delete line 1
sed -i '4i\welcome to' server.txt      // insert text before line 4
sed -i '$d' server.txt                 // delete the last line ($ = last line)
sed -i '$a\You like devops' server.txt // append text after the last line

sed -i 's/\r$//' server.sh             // strip Windows CRLF line endings (fix "\r" issues)

## awk — Pattern Scanning & Column Processing

awk '{print $1}' server.txt            // print first column (fields split by whitespace)
awk -F',' '{print $2}' data.csv        // print second column, using "," as field separator
awk '{print NR, $0}' server.txt        // print line number + full line

## cut / tr — Quick Field & Character Tools

cut -d',' -f1 data.csv                 // extract field 1 using "," as delimiter
cut -c1-5 server.txt                   // extract characters 1-5 of each line
tr 'a-z' 'A-Z' < server.txt            // convert lowercase to uppercase
tr -d ' ' < server.txt                 // delete all spaces
