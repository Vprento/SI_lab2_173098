# Втора лабораториска вежба по Софтверско инженерство

## Виктор Прентовски, бр. на индекс 173098

### 1.Control Flow Graph

-Најпрвин ги нумерирав линиите код од функцијата.

<img src="https://user-images.githubusercontent.com/80844421/119828773-ccae2b80-befa-11eb-9bd8-899188294c8a.png" height="350">
-Потоа со помош на https://app.diagrams.net/ го нацртав Control Flow Graph-от според претходно нумерираните линии код од функцијата.

<img src="https://user-images.githubusercontent.com/80844421/119828777-cd46c200-befa-11eb-8476-5c97c76567c8.png" height="650">

### 2.Цикломатска комплексност

-До цикломатската комплексност на овој код стигнав на 2 начини.  
Првиот начин е преку броење на јазлите и ребрата претставени на CFG и следење на формулата v(G)=E-N+2, односно во конкретниот случај v(G)=25-19+2=8.  
Вториот начин е преку броење на предикатите и следење на формулата v(G)=P+1, односно во конкретниот случај v(G)=7+1=8.

### 3.Тест случаи според критериумот Multiple condition

-Лево од стрелката се претставени предикатните јазли како што се именувани во CFG, десно се тест случаите од аспект на TRUE или FALSE, додека пак во заградата е if условот како код.  

3.2 - T/F 	     (i<timesList.size()) 	- 2 тест случаи  
7 - TX/FT/FF 	     (hr<0||hr>24)     		- 3 тест случаи  
8 - T/F 	     (hr<0)		       	- 2 тест случаи  
11 - T/F 	     (hr<24)	       		- 2 тест случаи  
12 - TX/FT/FF 	     (min<0||min>59)  		- 3 тест случаи  
14 - FX/TF/TT 	     (sec>=0&&sec<=59)		- 3 тест случаи  
17 - FXX/TFX/TTF/TTT (hr==24&&min==0&&sec==0)   - 4 тест случаи  

### 4.Тест случаи според критериумот Every branch

-Претставени се сите тест случаи односно патеки според критериумот Every branch кој налага поминување на секоја гранка.  

(1,2),(3.1),(3.2),20  
(1,2),(3.1),(3.2),(4,5,6),7,8,9,(3.3),(3.2)     -тест вредност hr = -2  
(1,2),(3.1),(3.2),(4,5,6),7,8,10,(3.3)          -тест вредност hr = 26  
(1,2),(3.1),(3.2),(4,5,6),7,11,12,13,(3.3)	-тест вредност hr = 22, min = 77  
(1,2),(3.1),(3.2),(4,5,6),7,11,12,14,15,(3.3)	-тест вредност hr = 22, min = 25, sec = 28  
(1,2),(3.1),(3.2),(4,5,6),7,11,12,14,16,(3.3)	-тест вредност hr = 22, min = 25, sec = 79  
(1,2),(3.1),(3.2),(4,5,6),7,11,17,18,(3.3)	-тест вредност hr = 24, min = 0, sec = 0  
(1,2),(3.1),(3.2),(4,5,6),7,11,17,19,(3.3)	-тест вредност hr = 25, min = 66, sec = 78  

### 5.Gradle build project за обична Java апликација  

-Креирав Gradle проект, го именував SI_lab2_173098 и ја вметнав класата SILab2 во src/main/java.
