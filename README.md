
***************************************** Some Notes ********************************************

1. The Driver class contans the main method.

2. The program requests the current date when each user logs on. This is not very convenient,
but allows to test the program with one run. Accordingly, the program does not save its data
in any files, each run starts all over again. New books are added/updated through the staff menu.
The menu is pretty intuitive and easy to use as the user is informed what input is expected. The
program also informs the user about the actions performed (for example, when a book is requested,
the program reports whether it added the book to the wait list or to the checkout list).

3. All user input is validated, the program does not allow invalid data. Allthough we didn't
specifically learn exception handling in class, I used the knowledge from my previous java experience.

4. To terminate the program, we need to press Ctrl-D. This will correctly terminate the program at any point.



******************************* Sample Output *****************************************************

Enter date as DD/MM/YYYY: 1/1/2000
Enter username: a
Enter user type (1 - Staff, 2 - Member): 1

1. Add new book
2. Update existing book
3. Pay penalties for a user
0. Exit

Enter your option: 1
Enter book title: a
Enter book description: a
Enter book location: a
Enter number of book copies: 1
a; a; a; 1(1)

1. Add new book
2. Update existing book
3. Pay penalties for a user
0. Exit

Enter your option: 0

Enter date as DD/MM/YYYY: 1/1/2000
Enter username: b
Enter user type (1 - Staff, 2 - Member): 2
b, welcome to the library!
Balance: $0.00

1. Request book
2. Return book
3. Extend date
0. Exit

Enter your option: 1
Enter book title: a
The book added to checkout list.

1. Request book
2. Return book
3. Extend date
0. Exit

Enter your option: 0
b, goodbye!

Enter date as DD/MM/YYYY: 1/1/2001
Enter username: b
b, welcome to the library!
You got a $182.50 penalty
Balance: $182.50
a: Due 15/01/2000

1. Request book
2. Return book
3. Extend date
0. Exit

Enter your option: 0
b, goodbye!

Enter date as DD/MM/YYYY: 1/1/2001
Enter username: a

1. Add new book
2. Update existing book
3. Pay penalties for a user
0. Exit

Enter your option: 3
Enter username: b

1. Add new book
2. Update existing book
3. Pay penalties for a user
0. Exit

Enter your option: 0

Enter date as DD/MM/YYYY: 1/1/2001
Enter username: b
b, welcome to the library!
Balance: $0.00
a: Due 15/01/2000

1. Request book
2. Return book
3. Extend date
0. Exit

Enter your option: ^D
Goodbye!




**************************** Short Description of Some Classes ************************************

The application contains 9 important classes:

1. Driver: entry point of the program. Just runs the main loop of the library.

2. Library (based on LibraryInterface): It is a storage for all users and all books. Provides methods for 
finding and adding new users and books. In addition to this, it implements the main library loop.

3. Book: It simply stores information about the book and provides access to this information.

4. User: This is the base class for all users- both staff and members. Each of the derived classes must 
implement two abstract methods – login() to handle user login and menu() to implement their own menu.

5. Staff: Implements the menu and 3 necessary operations for stuff.

6. Member: Implements the menu and 3 necessary operations for members.

7. CheckoutItem: This stores information about the book added to the checkout list 
for a member and provides a number of methods to work with it.

8. Date: Class based on java.util.Date. It has additional methods for working with the date.

9. IOUtility: This class contains methods for working with user input. No other class works 
directly with user input, only through the methods of this class.
