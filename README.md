# DanskeIT_CaseStudy
•	Interface IParser with 3 method signature included
1.	ProcessTheNodes :this is having the logic to find the output
2.	IsAllowed: this is having logic of allowed numbers in triangle node path
3.	ShowOutput: the final output that will be displayed
•	Class TMaxSummOddEven
It inherits Interface IParser to implement the methods
•	GatewayClass
It implements Dependency Injection
•	Finally in Program class we take input and through Dependency injection we invoke TMaxSummOddEven to show the output.




Program Logic
•	Converts the triangle into string array with new line split, each element of array here contains each row of triangle.
•	The string array is converted into 2 dimensional array
•	Send the triangle no of rows that is the string array length and the 2 dimentional array to process method
•	In process method we have initialize flag “EvenFlag” which is to identify whether to take even or odd number from the nodes and initialized as false if first element of 2 dimentional array is even or true if it is odd
•	Initialized integer variable result with first element of 2D array value
•	Initialize integer variable j as 0 which indicates position of columns in 2 d array
•	Start for loop here i is the position of rows in 2d array ,i starts with 2nd row as variable result initialized with firs row data and runs till last row of triangle which is string array length.
•	If EvenFlag is true we have to select even number so go inside that block
If both current row current column and current row next column are even add the maximum value from them to result else select the even value.update column value to +1 only if we had to select current row next column value.make evenFlag false so that we pick next value odd.
•	If EvenFlag is false we have to select odd number so go inside that block
If both current row current column and current row next column are odd add the maximum value from them to result else select the odd value.update column value to +1 only if we had to select current row next column value.make evenFlag true so that we pick next value even.

•	Once loop ends result contains the required sum
•	We have assumed for particular row and column position according to need of even or odd values selection if value not there we will go to next rows same column position and.
•	As per question and rules in pdf Maximum Sum of below input is 8186
										215 
                                        192 124
                                        117 269 442
                                        218 836 347 235
                                        320 805 522 417 345
                                        229 601 728 835 133 124
                                        248 202 277 433 207 263 257
                                        359 464 504 528 516 716 871 182
                                        461 441 426 656 863 560 380 171 923
                                        381 348 573 533 448 632 387 176 975 449
                                        223 711 445 645 245 543 931 532 937 541 444
                                        330 131 333 928 376 733 017 778 839 168 197 197
                                        131 171 522 137 217 224 291 413 528 520 227 229 928
                                        223 626 034 683 839 052 627 310 713 999 629 817 410 121
                                        924 622 911 233 325 139 721 218 253 223 107 233 230 124 233


