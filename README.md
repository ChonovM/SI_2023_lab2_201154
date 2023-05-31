Втора лабораториска вежба по Софтверско инженерство 


Мартин Чонов, бр. на индекс 201154 

 

Control Flow Graph 
 
https://prnt.sc/GG1d2nMaTNsU
 

Цикломатска комплексност 

Цикоматската комплексност според формулата е 21, 38 ребра - 25 јазли + 2*4 излезни точки. 

Тест случаи според критериумот Every statement 

Test case за линија 2 (null check): 

Input: user = null, 

Expected output: RuntimeException with message "Mandatory information missing!" 

Test case за линија 3 (username null check): 

Input: user = new User(null, "password", "email") 

Expected output: user.getUsername() е null, па setUsername() ќе биде повикан со user.getEmail(). 

Test case за линија 6 (email format check): 

Input: user = new User("username", "password", "email") 

Expected output: user.getEmail() содржи "@" и ".", па same = 0 

Test case за линија 8 (loop итерација): 

Input: user = new User("username", "password", "email"), allUsers = [user1, user2, user3] 

Expected output: Циклусот врти три пати поради 3-те users во allUsers 

Test case за линија 10 (email comparison): 

Input: user = new User("username", "password", "email"), allUsers = [user1, user2, user3] 

Expected output: existingUser.getEmail() е спореден со user.getEmail() 

Test case за линија 12 (username comparison): 

Input: user = new User("username", "password", "email"), allUsers = [user1, user2, user3] 

Expected output: existingUser.getUsername() е спореден со user.getUsername() 

Test case за линија 17 (password кондиција - Не содржи username, должина помала од 8): 

Input: user = new User("username", "pass", "email"), allUsers = [user1, user2] 

Expected output: Должината е помала од 8 или го содржи username па ќе врати false. 

Test case за линија 22 (special character check - password contains special character): 

Input: user = new User("username", "pass!word", "email"), allUsers = [user1, user2, user3] 

Expected output: Password содржи специјални карактери, па функцијата ќе врати same == 0. 

 

 

Тест случаи според критериумот Every path 

.... 

Објаснување на напишаните unit tests 

... ... 

 
