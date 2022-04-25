# Aggregate

```
data = data.frame (subjects = c("java", "python", "java", "java", "php", "php"), 
id = c(1, 2, 3, 4, 5, 6), 
names = c("manoj", "sai", "mounika", "durga", "deepika", "roshan"), 
marks = c(89, 89, 76, 89, 90, 67))

print (data)
print (aggregate (data$marks, list (data$subjects), FUN=sum))
print (aggregate (data$marks, list (data$subjects), FUN=min))
print (aggregate (data$marks, list (data$subjects), FUN=max))
```

# Armstrong

```
n = as.integer(readline(prompt = "Input : "))

sum = 0
temp = n

while(temp > 0){
	digit = temp %% 10
	sum = sum + (digit^3)
	temp = floor(temp / 10)
}

if(n == sum){
	print(paste(n, " is Armstrong"))
}else{
	print(paste(n, " is not Armstrong"))
}
```

# Calculator

```
add <- function(x,y){
  return(x+y)
}

subtract <- function(x,y){
  return(x-y)
}

multiply <- function(x,y){
  return(x*y)
}

divide <- function(x,y){
  return(x/y)
}

print("Select Operation")
print("1.Addition 2.Subtract 3.Multiplication 4.Division")

choice=as.integer(readline(prompt = "Enter Choice: "))
x=as.integer(readline(prompt = "No 1: "))
y=as.integer(readline(prompt = "No 2: "))

operator <- switch(choice, "+", "-", "", "/")
result <- switch(choice, add(x,y),subtract(x,y),multiply(x,y), divide(x,y))
print(paste(x, operator,y,"=",result))
```

# EDA IRIS

```
values = iris 

#View (values)
#str (values)

minn = min (values$Sepal.Length) 
print (minn)

maxx = max (values $Sepal.Length) 
print (maxx)

r = range(values $ Sepal.Length) 
print (r)

mean = mean(values$Sepal.Length) 
print (mean)

median = median (values$Sepal.Length) 
print (median)

a = quantile (values$Sepal.Length) 
print (q)

ql = quantile (values$Sepal.Length, 0.25) 
print (ql)

sd = sd (values$Sepal.Length) 
print (sd)

variance = var (values$Sepal.Length)
print (variance)

iqr = IQR (values $Sepal.Length) 
print (iqr)

s = summary (values) 
print (s)

vect = c(12,4,10,9,3,8,20,18,24) 
hist (vect) 
hist (vect, col = "blue", border ="Green")
plot (vect) 
plot (vect, type="o")
```

# Factorial (Using Recursion)

```
n = as.integer(readline(prompt = "Input : "))

fact <- function(n){
	if(n == 0){
		return(1)
	}else{
		return(n*fact(n-1))
	}
}

print(fact(n))
```

# Factorial (Without Recursion)

```
n = as.integer(readline(prompt = "Input : "))

fact = 1
if(n < 0){
	print("Invalid")
}else if(n == 0){
	print(0)
}else{
	for(i in 1:n){
		fact = fact * i
	}
}

print(fact)
```

# Fibonacci (Using Recursion)

```
n = as.integer(readline(prompt = "Input : "))

fibo <- function(n){
	if(n <= 1){
		return(n)
	}else{
		return(fibo(n-1) + fibo(n-2))
	}
}

if(n <= 0){
	print("Invalid")
}else{
	for(i in 0:(n-1)){
		print(fibo(i))
	}
}
```

# Fibonacci (Without Using Recursion)

```
n = as.integer(readline(prompt = "Input : "))

n1 = 0
n2 = 1

ctr = 2

if(n <= 0){
	print("Invalid")
}else{
	if(n == 1){
		print(n1)
	}else{
		print(n1)
		print(n2)
		while(ctr < n){
			nth = n1 + n2
			print(nth)
			n1 = n2
			n2 = nth
			ctr = ctr + 1
		}
	}
}
```

# Matrix (asinteger)

```
rows = as.integer(readline(prompt = "Enter rows : "))
columns = as.integer(readline(prompt = "Enter columns : "))

values = readline(prompt = "Enter Numbers of matrix : ")

values = strsplit(values, " ")
values = as.integer(values[[1]])

vect = c(values)

print(matrix(values, nrow = rows, ncol = columns))
```

# Matrix (asmatrix)

```
rows = as.integer(readline(prompt = "Enter Rows : "))
columns = as.integer(readline(prompt = "Enter Columns : "))

values = readline(prompt("Enter number of matrix : "))

values = strsplit(values, " ")
values = as.matrix(as.interger(values[[1]]))

print(matrix(values, nrow = rows, ncol = columns))
```

# Matrix Operations
```
r1 = as.integer(readline(prompt = "Enter row 1 : "))
c1 = as.integer(readline(prompt = "Enter column 1 : "))

values1 = readline(prompt = "Enter numbers of matrix 1: ")
values1 = strsplit(values1, " ")
values1 = as.integer(values1[[1]])

matrix1 = matrix(c(values1), r1, c1)

r2 = as.integer(readline(prompt = "Enter row 2 : "))
c2 = as.integer(readline(prompt = "Enter column 2 : "))

values2 = readline(prompt = "Enter numbers of matrix 2: ")
values2 = strsplit(values2, " ")
values2 = as.integer(values2[[1]])

matrix2 = matrix(c(values2), r2, c2)

add <- function(a, b){
	if((r1 == r2) && (c1 == c2)){
		return (a+b)
	}
}

sub <- function(a, b){
	if((r1 == r2) && (c1 == c2)){
		return (a-b)
	}
}

print(add(matrix1, matrix2))
print(sub(matrix1, matrix2))
print(matrix1 %*% matrix2)
print(matrix1 %% matrix2)
print(matrix1 / matrix2)
```

# Regression and Corelation

```
data(mtcars) 
head(mtcars) 
input<-mtcars

input$am <-as.factor(input$am) 
levels(input$am) <-c("AT", "MT") 
fit<-lm(mpg~am,data=input) 

summary(fit)
m3 <-lm(mpg ~ hp + am + wt, data = mtcars)

summary(m3)
d<-mtcars[c(-11,-10, -9,-8)]
d
cr<-cor(d)
library(corrplot) 
corrplot(cr,method="pie")
```

# Students Plot

```
student_marks =c(12,88,77,90,67,58,95,81,70,85)
names(student_marks)=c("Pratibha","Krutika","Pratibha","Purva","Siddhi","Jigna","Vinayak","Aditya","Shaan","Rahul")

pie(student_marks, labels=names(student_marks),col="green",main="Pie Chart", radius=1,col.main="red")

barplot(student_marks, xlab="Students", ylab="Marks", col="lightblue",col.axis="darkgreen",col.lab="black", border="black")

boxplot(student_marks~names(student_marks))
boxplot(student_marks, xlab="Box Plot", ylab="Age",col.axis = "darkgreen", col.lab = "darkgreen")

hist(student_marks, main = "Histogram", xlab = 
       "Marks",
     col.lab = "darkgreen",
     col.main = "darkgreen", col = "yellow")

plot(student_marks, type= "o", col = "green", xlab = "Students", ylab =
       "Marks",
     main = "Line Graph")
plot(x = student_marks, y= NULL, xlab = "Students", ylab=
       "Marks",main="ScatterPlot",
     col.lab = "darkgreen", col.main = "darkgreen", col.axis 
     = "darkgreen")
```

# Sum of N natural numbers (With Recursion)

```
n = as.integer(readline(prompt = " ENter : "))

calculate <- function(n){
	if(n <= 1){
		return (n)
	}else{
		return (n + calculate(n-1))
	}	
}

print(calculate(n))
```

# Sum of N natural numbers (Without Recursion)

```
n = as.integer(readline(prompt = "ENter : "))

if(n < 0){
	print("Invalid")
}else{
	sum = 0
	while(n > 0){
		sum = sum + n
		n = n - 1
	}
	print(sum)
}	
```
