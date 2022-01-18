# core-code
core code bootcamp

> # **Week 1**
> ## **Tuesday**
> - Java language is compiled or interpreted?  
>  &nbsp;&nbsp;&nbsp;&nbsp; Java is both, because it creates the BYTECODE file to iterpret by the JVM.  
> - Create an algorithm to calculate the equivalent of your local currencty to USD  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 1 – Set current_exchange rate  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 2 – Get amount_to_convert  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 3 – Mutiply current_exchange * amunt_to_convert  
>  &nbsp;&nbsp;&nbsp;&nbsp; Step 4 – Get amount converted  
> -  Why is pseudocode helpful?  
>   &nbsp;&nbsp;&nbsp;&nbsp; To understand the problem and plan the solution.  
> - Create a pseudocode to calculate the aproximated age of a user base on the year they born  
> &nbsp;&nbsp;&nbsp;&nbsp; INICIO  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; Y <-- 2022  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; BORN <-- 1991  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; CALCULAR AGE <-- Y - BORN  
> &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; DEVOLVER AGE  
> &nbsp;&nbsp;&nbsp;&nbsp; FIN  
> - Why are flowcharts important to us as developers?  
>  To us as developers a flowchart can help us to define the process and flow of our solution, is important to define it before we write some line of code or some PSEUDOCODE  because it should help us determine if our solution ends solving the problem.  
> ## **Wednesday**  
> 1. Learn about binary, decimal and hexadecimal numbers.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 2. Translate the year you where born to binary, decimal and hexadecimal.  
> &nbsp;&nbsp;&nbsp;&nbsp; -  11111000111  
> &nbsp;&nbsp;&nbsp;&nbsp; -  1991  
> &nbsp;&nbsp;&nbsp;&nbsp; -  7C7  
> 3. Translate 51966 into hexadecimal and binary.  
> &nbsp;&nbsp;&nbsp;&nbsp; - CAFE  
> &nbsp;&nbsp;&nbsp;&nbsp; - 1100101011111110  
> 4. Use a Low-level language, for example MIPS aseembler, to do so, you will need to follow this guide. We recomend to check the guide first but also this presentation could be helpful.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 5. Base on the examples and the guide of the low-level language: 5.1 Create a program to add two numbers given by the user 5.2 Create a program that display your name  
> - 5.1  
```assembly
.data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
.text
    main:
	li $v0, 4
	la $a0, number1
	syscall
	
	li $v0, 5
	syscall
	
	move $t0, $v0
	
	
    
	li $v0, 4
	la $a0, number2
	syscall
	
	li $v0, 5
	syscall
	
	move $t1, $v0
	
	add $t2, $t0, $t1
	
	li $v0, 1
	move $a0, $t2
	syscall
```
> - 5.2  
```assembly
.data
	name: .asciiz "\nLuis Eduardo Sotoj Teque"
.text
    main:
	li $v0, 4
	la $a0, name
	syscall
```

> ## **Thursday**  
> 1. Search for real word applications of Javascript.  
> &nbsp;&nbsp;&nbsp;&nbsp; Slack was build with JavaScript.  
> 2. (optional but great) Watch this video.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 3. (optional but great) Watch this video.  
>  &nbsp;&nbsp;&nbsp;&nbsp; Done.  
>  4. Follow the github course, you can find it here.  
>  &nbsp;&nbsp;&nbsp;&nbsp; Done.  
>  


> # **Week 2**  
> ## **Monday**  
> 1. Follow the github course.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.  
> 2. Watch this video.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.
> 3. Read this.  
> &nbsp;&nbsp;&nbsp;&nbsp; Done.
> 4. Create an account in Codewars.  
> &nbsp;&nbsp;&nbsp;&nbsp; User: https://www.codewars.com/users/lsotoj
> 

  





