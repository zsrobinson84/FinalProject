Project Description: 
In my freshman final project, I used Python to visualize a selection sort. Upon launch, the platform displays sixteen columns with randomly generated heights and six interactive buttons on the right-hand side: New Sort, Run, Pause, Step, Fast Mode, and New Size. When the program is run, the program sorts the columns from shortest to tallest, using two green boxes to indicate the current column it is comparing with the tallest column it has seen yet. When the current box reaches the last unsorted column, the program swaps the last column with the max column and restarts from the beginning. 
The buttons on the right-hand side of the screen enables the user to customize the program and analyze how selection sort works. They work as follows:
1.	New Sort restarts the program from the beginning, maintaining the most recent size input (where size is the number of columns and adjustable). 
2.	Run begins the selection sort if the program was just started or continues where it left off if it was paused.
3.	Pause enables the user to stop the sort at any point.
4.	Step enables the user to move through the selection sort piece by piece. For example, in the top image on the right, clicking the step button would move the rightmost green box one column to the right.
5.	Fast Mode increases the speed of each step and can only be used if the program is running.
6.	New Size enables the user to input a custom size (or number of columns) and hit enter to enact the change. The inputted size must be a number and between one and thirty-two (inclusive). 
The program is designed to be user friendly through the use of colors: Unsorted columns are light blue, sorted columns are black, and selected buttons are a darker shade of gray than unselected buttons. The green box indicating the tallest column is labeled with the description “max” below it to prevent confusion.

Code Description:
I created the Box class and initialized an object for each individual column. This enabled me to keep track of the height, color, and coordinates. Additionally, it helped me track if a column was the tallest, sorted, highlighted, or shown. A column is highlighted if it is the current column being compared or if it is the max column. I also created the sideBox class for the interactive buttons on the right of the screen, making my code more efficient when drawing the boxes, and helping me execute the correct action if a button was selected.   

At a high level my code works by creating and following an answer key. After initializing an object for each column and storing it in a list named app.board, I call getAnswerKey(app). This method uses app.board to create a two-dimensional list named “answer” that contains every step needed to transform the unsorted columns into sorted ones. Then, in my method takeStep(app), the program moves through every step in order and adjusts the graphics accordingly. 

Please note: this visualization was created using a CMU library (cmu_graphics) and will not run on without it. However, I've included a link to install the library, along with a link to a demonstration video showing the program in action.

Video link of program: https://youtu.be/qbdmu-rRJYk 
Link to install cmu_graphics: https://academy.cs.cmu.edu/desktop 

