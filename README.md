# Karthick-Projects- // PRODUCT SURVEY FORM using HTML,CSS,JAVASCRIPT
<!DOCTYPE html>
<html>
<head>
  <title>Survey Form</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="group">
    <header class="header">
      <h1 id="title" class="text-center">CUSTOMER SURVEY FORM </h1>
    </header>
    <form id="survey-form">
      <div class="form-group">
        <strong>
          <label id="name-label" for="name">Name</label><br><br>
        </strong>
        <input type="text" name="name" id="name" class="form-control" placeholder="Enter your name" required/>
      </div>
      <div class="form-group">
        <strong>
          <label id="email-label" for="email">Email</label><br><br>
        </strong>
        <input type="email" name="email" id="email" class="form-control" placeholder="Enter your Email" required/>
      </div>
      <div class="form-group">
        <strong>
          <label id="number-label" for="number">Age <span class="clue">(optional)</span></label><br><br>
        </strong>
        <input type="number" name="age" id="number" min="10" max="99" class="form-control" placeholder="Age"/>
      </div>
      <div class="form-group">
        <p>Is this your first time using our products & services?</p>
        <label>
          <input type="radio" name="first-time" value="Yes" class="input-radio"/>Yes
        </label><br><br>
        <label>
          <input type="radio" name="first-time" value="No" class="input-radio"/>No
        </label><br><br>
      </div>
      <div class="form-group">
        <p>Would you suggest our products and services to your friends and colleagues?</p>
        <label>
          <input type="radio" name="suggest" value="Yes" class="input-radio"/>Yes
        </label><br><br>
        <label>
          <input type="radio" name="suggest" value="No" class="input-radio"/>No
        </label><br><br>
      </div>
      <div class="form-group">
        <p>Do you have suggestions to improve our services?</p>
        <textarea id="comments" class="input-textarea" name="comment" placeholder="Enter your comment here..."></textarea>
      </div>
      <button type="submit" id="submit" value="submit" class="submit-button">Submit</button>
    </form>
  </div>
</body>
</html>


:root{
  color-white: #f3f3f3;
  color-fuchsia: #db7093;
  color-darkblue-alpha: rgba(27,27,50,0.8);
  color-green: #37af65;
}
body{
  font-family: 'Poppins',sans-serif;
  font-size: 1rem;
  line-height: 1.4;
  margin: 0;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: #FFC0CB;
}
h1{
  font-weight: 400;
  line-height: 1.2;
}
p{
  font-size: 1.125rem;
  font-weight: bold;
}
h1,p{
  margin-top: 0;
  margin-bottom: 0.9rem;
}
label{
  font-size: 1.125rem;
  margin-bottom: 0.5rem;
}
input,button,select,textarea{
  margin: 0;
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
button{
  border: none;
}
.group{
  width: 100%;
  margin: 3.125rem auto 0 auto;
}

.header{
  padding: 0 0.625rem;
  margin-bottom: 1.875rem;
}
.description{
  font-style: italic;
  font-weight: 200;
  text-shadow: 1px 1px 1px rgba(0,0,0,0.4);
}
.clue{
  margin-left: 0.25rem;
  font-size: 0.9rem;
  color: #e4e4e4;
}
.text-center{
  text-align: center;
}
form{
  background: var(--color-fuchsia);
  padding: 2.5rem 0.625rem;
  border-radius: 0.25rem;
  margin-bottom: 50px;
  display: inline-block;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.form-group{
  margin: 0 auto 1.25rem auto;
  padding: 0.25rem;
}
.form-control{
  display: block;
  width: 100%;
  height: 2.375rem;
  padding: 0.375rem 0.75rem;
  color: #495057;
  background-color: #fff;
  background-chip: padding-box;
  border-radius: 0.25rem;
  transition: border-color 0.15s ease-in-out;
  box-shadow: 0.15s ease-in-out;
}
.form-control:focus{
  border-color: #80bdff;
  outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(0,123,255,0.25);
}
.input-radio,.input checkbox{
  display: inline-block;
  margin-right: 0.625rem;
  min-height: 1.25rem;
  min-width: 1.25rem;
}
.input-textarea{
  min-height: 120px;
  width: 600px;
  padding: 0.625rem;
  resize: vertical;
  border-radius: 5px;
}
.submit-button{
  display: block;
  width: 100px;
  padding: 0.75rem;
  background: #fff8dc;
  color: inherit;
  border-radius: 10px;
  cursor: pointer;
  font-weight: 600;
  float: right;
  margin-right: 7px;
}
 <script>
    document.getElementById('survey-form').addEventListener('submit', function (event) {
      event.preventDefault(); 
      
      //  logic 
      var name = document.getElementById('name').value;
      var email = document.getElementById('email').value;

      if (name.trim() === '' || email.trim() === '') {
        alert('Name and Email are required fields.');
        return;
      }

      // If all validation passes, you can  click on the submit button
      alert('Form submitted successfully!');
    });
  </script>
</body>
</html>

// Java Program To Create an array with the values (1, 2, 3, 4, 5, 6, 7) and shuffle it.
import java.util.*;

 public class Shuffle {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int[] array = {1, 2, 3, 4, 5, 6, 7};
        // Array created with values.
        Random shuff = new Random();
        // creating a Random object.
        for (int i = array.length - 1; i > 0; i--) {
            // Generate a random index from 0 to i
            int j = shuff.nextInt(i + 1);
            // Swap the elements at i and j
            int temp = array[i];
            array[i] = array[j];
            array[j] = temp;
        }
        System.out.println(Arrays.toString(array));
    }
}

//  Java Program To Check if the input is pangram or not. (Pangram is a sentence that contains all the alphabet
from a-z) 

public class Main {
    static boolean checkPangram(String str) {
        // Create an array to store the occurrence of alphabets
        boolean[] alphabetMarker = new boolean[26];

        // Convert the string to char array
        char[] strArray = str.toCharArray();

        // Iterate through the char array and mark the alphabets present
        for (char c : strArray) {
            if (Character.isLetter(c)) {
                int index = Character.toLowerCase(c) - 'a';
                alphabetMarker[index] = true;
            }
        }

        // Check if all alphabets are present
        for (boolean marker : alphabetMarker) {
            if (!marker) {
                return false;
            }
        }

        return true;
    }

    public static void main(String[] args) {
        String str =  "The quick brown fox jumps over the lazy dog";
        if (checkPangram(str)) {
            System.out.println("\"" + str + "\" is a pangram.");
        } else {
            System.out.println("\"" + str + "\" is not a pangram.");
        }
    }
}

//JavaScript program for Perform sorting of an array in descending order.
let array = []; // enter the array elements

array.sort(function(a, b) {
  return b - a;  //it compares the two numbers if the second number is greater than first number by the value..
});
console.log(array);

//JavaScript Program to Take a sentence as an input and reverse every word in that sentence. 
a. Example - This is a sunny day > shiT si a ynnus yad
function reverseSentence(sentence) {
    return sentence.split(' ').map(function(word) {
        return word.split('').reverse().join('');
    }).join(' ');
}
console.log(reverseSentence("This is a sunny day"));


// Java program for Enter a Roman Number as input and convert it to an integer. (ex IX = 9)

import java.util.*;

public class Roman  //defining the roman number with there respective values and return value. 
{
    static int value(char r) 
{
        if (r == 'I')
            return 1;
        if (r == 'V')
            return 5;
        if (r == 'X')
            return 10;
        if (r == 'L')
            return 50;
        if (r == 'C')
            return 100;
        if (r == 'D')
            return 500;
        if (r == 'M')
            return 1000;
        return -1;
    }

    static int romanToDecimal(String str) //to convert the entered roman number into Decimal number.
{
        int res = 0;

        for (int i = 0; i < str.length(); i++) {
            int s1 = value(str.charAt(i));

            if (i + 1 < str.length()) {
                int s2 = value(str.charAt(i + 1));

                if (s1 >= s2) {
                    res = res + s1;
                } else {
                    res = res + s2 - s1;
                    i++;
                }
            } else {
                res = res + s1;
                i++;
            }
        }

        return res;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //to accept the input from the user through keyboard.
        System.out.println("Enter a Roman Number:");
        String str = sc.nextLine();
        System.out.println("Integer form of Roman Numeral is " + romanToDecimal(str));
    }
}

// Create a basic calculator using HTML, CSS, and JavaScript with the functionality of add, 
subtract, multiply and divide.

<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> //This is an HTML element used to provide metadata about the HTML document. In this case, it's used for defining the viewport 
//A value of 1.0 means that the page is not zoomed in or out initially, and it appears at 100% zoom.
  <title>calculator</title>  // title of the web page 
  <link href="in-30-layout.css" rel="stylesheet" type="text/css"> // this href is used to connect our css style with html document.
</head>
<body>
  <div class="calculator">
    <form>
      <div class="display">
        <input type="text" id="display" name="display">
      </div>
      <input type="button" value="AC" onclick="document.getElementById('display').value = ''">
      <input type="button" value="9">
      <input type="button" value="8">
      <input type="button" value="7">
      <input type="button" value="+">
      <input type="button" value="4">
      <input type="button" value="5">
      <input type="button" value="6">
      <input type="button" value="-">
      <input type="button" value="D" onclick="display.value = display.value.toString().slice(0,-1)">
      <input type="button" value="1">
      <input type="button" value="2">
      <input type="button" value="3">
      <input type="button" value="%">
      <input type="button" value="/">
      <input type="button" value=".">
      <input type="button" value="0">
      <input type="button" value="*">
      <input type="button" value="00">
      <input type="button" value="=" onclick="display.value = eval(display.value)" class="equal">
    </form>
  </div>
</body>
</html>

.calc-body {
  width: 275px;
  margin: auto;
  min-height: 400px;
  box-shadow: 0 8px 50px -7px rgba(22, 114, 77, 0.7);
  background: #3A4655;
}

.calc-screen {
  padding: 3rem;
  display: flex;
  flex-direction: column;
  width: 30%;
}

.calc-container {
  width: 150px;
  margin: auto;
}

#calc-operation {
  font-size: 1.3rem;
  text-align: right;
  color: #727B86;
  padding-bottom: 0.5rem;
}

#calc-typed {
  font-size: 2rem;
  text-align: left;
  color: #fff;
}

#user-input {
  font-size: 2.5rem;
  text-align: left;
  color: #fff;
  width: 150%;
}

.calc-button-row {
  display: table;
  text-align: left;
}

.calc-button-row button {
  display: table-cell;
  width: 25%;
  background: #425062;
  color: #fff;
  height: 65px;
  font-size: 1.3rem;
  border: none;
  border-color: #3C4857;
  border-width: 1px 1px 0px 0;
  border-style: solid;
}

.calc-button-row button:nth-child(4n) {
  border-right: none;
}

.calc-button-row button:active {
  position: relative;
  top: 1px;
}

.calc-button-row button:hover {
  background: #3e4b5c;
}

.ac {
  margin-right: auto;
  padding: 10px;
  text-align: right;
  color: #ff7665;
}

.calc-button-row button.opt {
  color: #ffbc56;
}

 <script>
    document.getElementById('survey-form').addEventListener('submit', function (event) {
      event.preventDefault(); 
      
      // logic here
      var name = document.getElementById('name').value;
      var email = document.getElementById('email').value;

      if (name.trim() === '' || email.trim() === '') {
        alert('Name and Email are required fields.');
        return;
      }

      // If all validation passes, you can click on submit 
      alert('Form submitted successfully!');
    });
  </script>



