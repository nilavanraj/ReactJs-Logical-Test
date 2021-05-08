# ReactJs-Logical-Test

# Question 1
Q1) Define an array of numbers (use any random numbers). Write a program to print only the even numbers of the array. Do not use any library functions, need to do via for loops only

ANSWER
```
function Dev() {
    var InitialArray = [1, 2, 3, 4, 5, 6, 7, 8, 9,11,22,30,17];
    var ResultArray = [];
    for (var i = 0; i < InitialArray.length; i++) {
        if (InitialArray[i] % 2 == 0) {
            ResultArray.push(InitialArray[i]);
        }
    }
    return ResultArray;
}

function App() {
  return (
    <div className="App">
    <Dev/>
    </div>
  );
}
```
# Question 2
Find the maximum consecutive 1's in an array of 0's and 1's.
Example:
a) 00110001001110 - Output :3 [Max num of consecutive 1's is 3]
b) 1000010001 - Output :1 [Max num of consecutive 1's is 1]

ANSWER
```
function Dev() {
    var InitialArray = [0,0,1,1,0,0,0,1,0,0,1,1,1,0];
    var Result = 0, highTemp = 0, temp = 0;
   
    for (var i = 0; i < InitialArray.length; i++) {
        if (InitialArray[i] == 1) {
            Result = 1;
            if (Result == 1) temp++;

        } else {
            Result = 0;
            temp = 0;
        }
        if(temp) { highTemp = temp}
    }
    return highTemp;
}

function App() {
  return (
    <div className="App">
    <Dev/>
    </div>
  );
}
```
# Question 3
Suppose you have an array of 101 integers. This array is already sorted and all numbers in this array are consecutive. Each number only occurs once in the array except one number which occurs twice. Write a js code to find the repeated number.
e.g $arr = array(0,1,2,3,4,5,6,7,7,8,9,10...................);

Answer
```
function Dev() {
    var InitialArray = [0, 1, 2,3, 4, 5, 6, 7, 7, 8, 9, 10];
    var temp = InitialArray;
    for (var i = 0; i < InitialArray.length; i++) {
        for (var j = 0; j < InitialArray.length; j++) {            
            if (InitialArray[i] == InitialArray[j]&& i!=j) {               
                temp.splice(j, 1,);
            }
        }   
    }
    return InitialArray;
}

function App() {
  return (
    <div className="App">
    <Dev/>
    </div>
  );
}

export default App;

```
# Question 4
Let’s see we an api url www.example.com/api/get/1 
Write a sample code to call this rest api and display the result.

Answer
```
export default class App extends Component {    
    constructor(props) {
        super(props);
        this.Webcapture();
        this.state = {
            input: []
        }
    }
    Webcapture = () => {
        var that = this;
        var xmlhttp = new XMLHttpRequest();
        //
        var url = "www.example.com/api/get/1";
        xmlhttp.onreadystatechange = function () {
          
            if (this.readyState == 4 && this.status == 200) {
                var myArr = JSON.parse(this.responseText);
                that.setState({ input: JSON.stringify(myArr )});               
            }
        };
        xmlhttp.open("GET", url, true);
        xmlhttp.send();
    }
    render() {
        return (
            <div>  {this.state.input}</div>     
            );
    }
}
```
# Question 5
Assume there is a object of this format 
var obj = {
 “id” : 4, “name” : “abc”,
 “id” : 10, “name” : “ab2”,
 “id” : 5, “name” : “abc3”,
 “id” : 6, “name” : “abc5”
}
It can be a dictionary or java object, as per your language of choice. But its key/value pair dictionary simply.

Write a code to sort the object by id 
I.e final output should have objected sort by id’s
Answer 
```
var result = [];
var  obj = [
 {"id" : 4, "name" : "abc"},
 {"id" : 10, "name"  : "abc2"},
  {"id" : 5, "name" : "ab5c"},
  {"id"  : 6, "name" : "ab8c"}
]

for (var item in obj) {
  result.push([item, obj[item]]);
}


 result.sort(function(a, b) {
 return a[1] - b[1];});
console.log(result);


```
