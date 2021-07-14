# AWK

## Shantanu N Kulkarni

### Slide 1

*Basic Structure*

	awk 'pattern { action }' filename

pattern + action = main block / text block

*Multiple main/text blocks possible*
	
	awk 'pattern1 { action1 } 
	'pattern2 { action2 }'  filename

*Multiple actions also supported like this,*

	awk 'pattern1 { action1; action2 }' filename

_Things  to remember_

### Slide 2

*Sample data file*

Marks of three students in 3 subjects

amit 90 80 70
ajay 60 75 35
shan 99 89 86

	awk '{ print }' data
	awk '{ print $0 }' data

	awk '{ print $1 }' data
	awk '{  print $1, $3 }' data

	awk '{ print NF }' data
	awk '{ print $NF }' data
	awk '{ print NR }' data

### Slide 3

	awk '{  print $1, ($2+$3+$4)/3 }' data

	awk '/amit/ { print $0 }' data
	awk '/amit/' data
	awk '!/amit/' data

	awk '$2 == 60' data

	awk '/amit/ || $3 > 80' data



