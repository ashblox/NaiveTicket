# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket? '0' is returned.

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior? The machine will print a ticket regardless of what the balance is. The balance after printing a ticket is always zero.
	* What happens if you insert too much money into the machine – do you receive any refund? No. The balance is always zeroed as a result of printing a ticket.
	* What happens if you do not insert enough and then try to print a ticket? The machine will still print a ticket (even if you haven't entered any money).

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different? The new price is printed on the ticket (in place of the previous price).

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part. public class Student { ... } public class LabClass { ... }

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class? Yes. There are two expected identifier errors in the class name and the TicketMachine contstuctor does not work. You cannot compile the code and therefore you cannot run the program.

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram? The TicketMachine class 'box' is cross-hatched, indicating that the code needs to be compiled but there are errors prohibiting you from doing so.
	* What error message do you get when you now press the compile button? <identifier> expected (twice - once after class and once at the end of TicketMachine). You also get the error invalid method declaration; return type required for public TicketMachine(int ticketCost)
	* Do you think this message clearly explains what is wrong? It's not crystal clear, but I believe 'public' is the identifier that it is expecting to be BEFORE class and it's not recognized when placed after class.

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class. It is!

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
Fields: price, balance, total; Constructor: TicketMachine; Methods: getPrice(), getBalance(), insertMoney(), and printTicket()

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class? The constructor doesn't name a return type; the methods either return integers or 'void' meaning they return nothing. 

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count; an integer
private Student representative; an object of class Student
private Server host; an object of class Server
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive; alive
private Person tutor; tutor
private Game game; game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible? Yes, the box on the diagram for the class is cross-hatched, indicating that the code cannot be compiled.
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
* Once again, experiment via the editor. Yes, the semicolon is expected.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`. private int status;

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name) class Student
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price) two parameters - a string and a double
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields? Int (pages); String or Enum (color); String (name)

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.

### Exercise 2.19: name = petsName;

### Exercise 2.21: There really isn't much of a difference - only the parameter which is returned (either price or balance).

### Exercise 2.22: What is the balance of the machine? (Conversely, How much money was fed into the machine?)

### Exercise 2.23: It does not, but it is better practice (convention) to have them match.

### Exercise 2.24: public int getTotal() { return total; }

### Exercise 2.25: 'missing return statement"

### Exercise 2.26: getPrice returns an integer whereas printTicket returns nothing (indicated by void)

### Exercise 2.27: They do not have return statements. As indicated by their headers, they do not return anything (indicated by void).

### Exercise 2.29: A constructor would not have a return indicator - i.e. would not say void.

### Exercise 2.30: price = ticketCost;

### Exercise 2.31: score = score + points;

### Exercise 2.32: price = price - amount;

### Exercise 2.35: The parameter, price, is set to one value for the first TicketMachine and another value for the second. That value is being passed in to the statement.

### Exercise 2.36: It would print the word price instead of the value associated with the parameter.

### Exercise 2.37: It would print literally - # price cents. 

### Exercise 2.38: No, both just print words literally - neither passes in a variable value. 

### Exercise 2.39: You can no longer create machines with different ticket prices. The price will always be 1000 cents.

### Exercise 2.40: It is a mutator. 

### Exercise 2.41: A mutator.

### Exercise 2.43: The balance is still zero when the error message prints. If you insert zero, you still get the error message but no amount shows after the colon.

### Exercise 2.44: It adds zero to the balance (and does not spit out an error message).

### Exercise 2.46: In Naive Ticket, if a ticket is printed, the entire balance is committed to the total, not just the price of a ticket. The balance is then zeroed, regardless of however much money is left over. The new Ticket Machine corrects these errors, reducing the balance by the cost of the ticket and updating the total only with the price of a ticket (not the entire balance).

### Exercise 2.47: No, if the value of balance is less than the value of price, the ticket won't print and you will get an error message.

### Exercise 2.49: int saving = price * discount;

### Exercise 2.50: int mean = total / count;

### Exercise 2.51: if (price > budget) { System.out.println("Too expensive"); } else { System.out.println("Just right"); }

### Exercise 2.52: if (price > budget) { System.out.println("Too expensive. Budget is only " + budget); } else { System.out.println("Just right"); }

### Exercise 2.53: The balance is already zero when you return it.

### Exercise 2.54: 'missing return statement' - the return statement of a method is always it's final statement. No further statements in the method will be executed.

### Exercise 2.56: It is a mutator. Although it gives you access to the value of total, it does in effect change the total also. By causing change to the state of the object, it classifies as a mutator.




