# StringServer
![code](https://user-images.githubusercontent.com/130100567/234160365-a9520742-a679-4d9a-b1c6-3f3d7185d2e4.png)

testing on local server

---
![save1](https://user-images.githubusercontent.com/130100567/234160408-a8621396-a71e-4e38-b1b3-c7641b2a8ecf.png)

the url is calling the handleRequest method in the StringServer.java file, 
1. it takes in a url as its argument 
2. it checks if the path of the url is equal to "/add-message"
3. if the path correct then the method checks for if the query of the url has "s=" in it 
4. finally if all of those steps are true which they are in this case, 
because this is the first time I'm inputting a string, the string variable str is emtpy therefore the strg is just the string being inputted.

---
![save2](https://user-images.githubusercontent.com/130100567/234160423-515dc74f-fc0f-46a2-b79a-581f39d3599a.png)

the url is calling the handleRequest method in the StringServer.java file, 
1. it takes in a url as its argument 
2. it checks if the path of the url is equal to "/add-message"
3. if the path correct then the method checks for if the query of the url has "s=" in it 
4. finally if all of those steps are true which they are in this case, 
since this is the second time I'm calling the method, there's already a previous string input that was saved so the page first prints the previously save string and then the new string on the next line. 
in the actual code itself, the str variable is now both those strings

---
