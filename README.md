Download Link: https://assignmentchef.com/product/solved-cpt121-task-5-2-3-practice-exercises-working-with-arrays-of-objects
<br>
<strong>Task 5.2.3 Practice Exercises – Working with Arrays of Objects </strong>

<ol>

 <li><strong> Assume that the application class below makes use of the Account class discussed previously </strong>import java.util.*; public class TestAccounts2</li>

</ol>

{ public static void main(String args[])

{

String accountID, name; double balance; Scanner sc = new Scanner(System.in));

/*** Array used to store up to 10 accounts ***/

Account[] accounts = new Account[10];

<strong>/*** CODE for part a) goes here ***/ </strong>…

<strong>/*** CODE for part c) goes here *** … </strong>

// print details for all accounts

System.out.println(“Account Details”);

<strong>/*** Code for part b) goes here ***/ … </strong>

}

}

<ol>

 <li>Write code to populate the array with the Accounts containing the following details:</li>

</ol>

<table width="366">

 <tbody>

  <tr>

   <td width="129">ID</td>

   <td width="123">Name</td>

   <td width="113">Balance</td>

  </tr>

  <tr>

   <td width="129">S5234</td>

   <td width="123">David</td>

   <td width="113">$1000</td>

  </tr>

  <tr>

   <td width="129">S1239</td>

   <td width="123">Cliff</td>

   <td width="113">$2000</td>

  </tr>

  <tr>

   <td width="129">S4236</td>

   <td width="123">Martin</td>

   <td width="113">$3000</td>

  </tr>

  <tr>

   <td width="129">S8850</td>

   <td width="123">Jane</td>

   <td width="113">$5000</td>

  </tr>

 </tbody>

</table>

Note that the array capacity will exceed the number of objects stored and thus need to consider how to manage working with this partially filled array in latter requirements.

<ol>

 <li>Write code which iterates through the objects that are currently stored in the array and prints their details to the screen. Your iteration loop should cease executing once it has gone past the last object in the array.</li>

 <li>Write code segments at the point following the comment for part C) in the sample code above which do each of the following:

  <ol start="2000">

   <li>Iterate through the objects currently stored in the array and add 1% interest to any account with a balance &gt; $2000.</li>

   <li>Prompt user to enter an account ID, locate the Account object with that ID and process a withdrawal (getting the withdrawal amount from the user).</li>

  </ol></li>

</ol>

If the ID is not found or the withdrawal fails then an appropriate error message should be displayed to the user.

If the withdrawal is successful then display the new balance to the user.

<ul>

 <li>Prompt the user to enter the names of two Account holders to organise a transfer for, locate the Accounts with the specified names and proceed with a transfer from the first account to the second.</li>

</ul>

If either one or both of the accounts are not found, or the attempting transfer of funds fails, then a suitable error message should be displayed to the user.

If the transfer is successful then display the new balances for the two Accounts to the user.

<em>Note that you should only use the one search loop to locate the to Accounts in question as this is a more efficient approach to the problem. </em>




<ol>

 <li><strong>Account p,q; </strong></li>

</ol>

<strong>for (int i=0;i&lt;3; i++) </strong>

<strong>{ </strong>

<strong>if(accounts[i].getName().compareTo(“Martin”) == 0) p = accounts[i]; </strong>

<strong>else if(accounts[i].getName().compareTo(“David”) == 0) q = accounts[i]; </strong>

<strong>} </strong>

<strong>p.transfer(q,100); </strong>

<strong> </strong>

<ol>

 <li><strong>Replace the for loop with a do while loop so that the user may repeatedly print the account details by specifying the account ID. If no such ID exist print appropriate error message. After each iteration the user should be prompted whether to continue. </strong></li>

</ol>

Enter Account ID:                  <em>s4236 </em>

Acount details: Name = Martin                   Balance = $3000

Continue (Y/N) ? <em>Y </em>

Enter Account ID:                  <em>s5234 </em>

Acount details: Name = David                  Balance = $1000

Continue (Y/N) ? <em>Y </em>

Enter Account ID:                 <em>s5444 </em>

No such account exist Continue (Y/N) ? <em>N </em>

Bye for now.




<strong>( Hint: You need to use the getID() method ) </strong>

<ol>

 <li><strong>What will be the output of the program below ? Why ? Trace through with diagrams. </strong></li>

</ol>

class MyInt { private int val;




public MyInt(int n)

{ val = n;

}

public void setVal(int n)

{ val = n;

}

public int getVal()

{ return val;

}

}




public class TrySwap { public static void intSwap(int x, int y) { int temp = x; x = y; y = temp;

}

public static void refSwap(MyInt x, MyInt y) {

MyInt temp = x; x = y; y = x;

}

public static void contentSwap(MyInt x, MyInt y) { int temp = x.getVal();

x.setVal(y.getVal());

y.setVal(temp);

}

public static void main (String[] args) { int u = 10; int v = 20;




MyInt num1 = new MyInt(10);

MyInt num2 = new MyInt(20);




intSwap(u,v);

System.out.println(“u = ” + u + ” v = ” + v );

refSwap(num1, num2);

System.out.println(“num1 = ” + num1.getVal()


” num2 =” + num2.getVal() );  contentSwap(num1, num2);

System.out.println(“num1 = ” + num1.getVal()


” num2 =” + num2.getVal() );




}

}