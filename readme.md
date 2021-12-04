## Iteration
Java has three different control structures that allow the computer to perform iterative taks: 'for' loop, 'while' loop, and 'do.. while' loop

---
**The `for` loop**

The general form of a for loop is
```Java
for (initiaization; termination condition; update statement) {
	statements //body of loop
}
```
The termination condition is tested at the top of the loop; the update statement is performed at the bottom. 

**Example**
```java
for(int i = 1; i < 5; i++) {
	System.out.print(i + " ")
}

//outputs: 1 2 3 4
```

Explanation:

The *loop variable* **i** is initialized to 1, and the termination condition **i < 5** is evaluated. If it is **true**, the body of the loop is executed, and then the variable **i** is incremented according to the update statement. As soon as the termination condition is **false** (e.g i>=5), control passes to the first statement following the loop. 

*Note:*

1. The loop variable should not have its value changed inside of the loop body
2. The intializzing and update statements can use any valid constants, variables, or expressions
3. The scope of the loop variable is restricted to the loop body

### Enhanced *for* loop (For-each Loop)
This is used to iterate over an array or collection

```java
for(SomeType element: collection){
	statements
}
```
*Note:*

1. The enhanced *for* loop should be used for accessing elements in the date structure, not for replacing or removing elements
2. The loop hides the index variable that is used with arrays

## While Loops
Boolean test is preformed at the beginning of the loop, if **true**, the loop body is executed, otherwise, we continue

**Examples**
```java
//int i = 1;
int mult3 = 3;
while(mult3 < 20){
	System.out.print(mult3 + " ");
	//i++;
	mult3 += 3;
}

for(int = 3;j = 20; i += 3){
	System.out.print(i + " ")
}
```

*Note:*

1. It is possible for the body of a **while** loop to never be executed
2. Beware of infinite loops, which happens when the boolean test is never false. Don't forget to change the loop variable in the body of the loop. 

## do-while loop
Similar to a while loop, however it checks for the condition *after* executing the loop body

**Example**
```Java
int i = 1;
do{
System.out.println("Hello World");
i++;
}
```

## Nested Loop
It is indeed possible to create a loop inside the body of another loop; this is called a nested loop

```java
for(int i = 1; i < 3; i++){
	for(int j =1; j <= 4; j++){
		System.out.print("*")
	}
	System.out.pritnln();
}

output: **** [indent to next line] **** [repeat]
```

