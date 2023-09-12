
# Leader_Board_Search Project

## Hosted Link 

Click here --> [https://abhi9818-m.github.io/Js_Emoji_Project/emoji.html](https://abhi9818-m.github.io/leaderboard_Project/index.html)

### Step 1: Create a New HTML File

Create a new HTML file and save it as index.html. Add the following code to the file:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <div class="main">
            <h1>LeaderBoard</h1>
        <div id="form">
            <input type="text" id="fName" placeholder="First Name">
            <input type="text" id="lName" placeholder="Last Name">
            <input type="text" id="country" placeholder="Country Name">
            <input type="number" id="score" placeholder="score">
            <button id="AddDetailsButton">Add Player</button>
        </div>
        <div id="scoreMainContainer"></div>
    </div>
    <script src="./script.js"></script>
</body>
</html>
```

### Step 2: Create a New JS File
Create a new JS file and save it as index.js. Add the following code to the file:

```

const scoreMainContainer  = document.getElementById("scoreMainContainer")

AddDetailsButton.addEventListener("click", ()=>{
    console.log(AddDetailsButton);
    const fName = document.getElementById("fName")
    const lName = document.getElementById("lName")
    const country = document.getElementById("country")
    const score = document.getElementById("score")

    const scoreBoard = document.createElement("div");  
    scoreBoard.classList.add("scoreBoard")
    
    scoreBoard.innerHTML =  `
    <p class="playerName">${fName.value} ${lName.value}</p>
    <p class="country">${country.value}</p>
    <p class="score">${score.value}</p>
    <p class="deleteIcon">&#x1f5d1;</p>
    `;

    scoreMainContainer.appendChild(scoreBoard)
    fName.value = "";
    lName.value = "";
    country.value = "";
    score.value = "";
    deleteElement()
})

function deleteElement() {
    const deleteIcon = document.querySelectorAll(".deleteIcon")
    deleteIcon.forEach((ele)=> {
        ele.addEventListener("click" , (e) =>{
            return e.target.parentElement.remove()
        })
    })
}


```
### Step 3: Create a New css File
Create a new CSS file and save it as style.css. Add the following code to the file:

```
body{
    margin: 0;
    box-sizing: border-box;
    padding: 0;
}
.main{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
  
}
form{
    display: flex;
    gap: 50px;
}
input{
    padding: 10px;
   
    border: 2px solid rgb(81, 157, 104);
}
button{
    padding: 10px 25px;
    border: 2px solid rgb(59, 111, 75);
    background-color: rgb(81, 157, 104);
}
#scoreMainContainer{
    margin-top: 30px;
    width: 62%;
    
}
.scoreBoard{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin: 10px;
    border-radius: 2px;
    border: 2px solid rgb(59, 111, 75);
    background-color: rgb(81, 157, 104);
    box-shadow: 3px 3px 7px rgb(0, 0, 0);
}



```



