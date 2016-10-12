TP Shell
find . -name \*.java

find . -name \*.java | wc -l

find . -name \*.java -exec wc -l {} \;

find . -name \*.java -exec wc -c {} \; | sort -nr | tail -10

#!/bin/bash

total=0
for i in $(find . -name \*.java);
do 
	total+=$(wc -l);
	
done
echo $total
