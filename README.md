# ReactJs-Logical-Test

# Answer 1
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
}```
