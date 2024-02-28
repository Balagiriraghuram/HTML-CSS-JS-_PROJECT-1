# HTML-CSS-JS-_PROJECT-1

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       .length{
        padding: 10px 50px;
        font-size: 17px ;
        border: 2px solid black;
        margin: 30px;
        border-radius: 20px;
       
         }
         .button{
            height: 50px;
            width: 100px ;
            font-size: 25px;
            color: white;
            background-color: blue;
            border-radius: 20px;
            margin: 30px;
         }
         .body{
            background-color: pink ;
         }
         .err{
            color: soild red;
            background-color: white;
         }
    </style>
</head>
<body class = " body">
    <form id="myform" onsubmit="return error()">
        <b>Name  :  </b>
        <div>
             <input type="text" placeholder="Enter name" size="30" class="length" id="name"> <span class ="err"> </span>
        </div>
        
        <b>User Id :  </b>
        <div>
             <input type="text" placeholder="Enter UserId" size="30" class="length" id="id"> <span class ="err"> </span>
        </div>
        
        <b>Phone number : </b>
        <div>
            <input type="number" placeholder="Enter phonenumber" size="10"  class="length" id="phone" > <span class ="err"> </span>
        </div>
        <b>Gender : </b>
        <br>
        <div  >
             <input type="radio" name="gen" value="Male"  >  <b>Male</b>
            <input type="radio" name="gen" value= "Female"  >  <b>Female</b>
            <input type="radio" name="gen" value="Others"  >  <b>Others</b>
        </div>
        <br>
        <b>E-mail : </b>
        <div>
             <input type="email" placeholder="Enter emailId" size="30" class="length" id="email"> <span class ="err"> </span>
        </div>
        
        <b>Password : </b>
        <div>
             <input type="password" placeholder="Enter password" size="15" class="length" id="pass" > <span class ="err"> </span>
        </div>
        
        <b>Conform-Password : </b>
        <div>
           <input type="password" placeholder="Conform-Password" size="15" class="length" id = "cpass"><span class ="err"> </span>
        </div>
       
        <div>
           <input type="submit" class = "button">
        </div>
    </form>
    <script>
       
        function error() {
           
            let name = document.getElementById("name");
            let id = document.getElementById("id");
            let phone = document.getElementById("phone");
            let pass = document.getElementById("pass");
            let cpass = document.getElementById("cpass");
            
             let retVal = true ;

             let err = document.getElementsByClassName("err");
             for(let j = 0 ; j < err.length ; j++){
                err[j].innerHTML = " " ;
             }
           if(name.value.length <= 10){
            let elm = name.nextElementSibling ;
            elm.innerHTML = "Please enter more than 10 characters" ;
            retVal = false ;
           }
          
           if(id.value.length <= 10){
            let elm = id.nextElementSibling ;
            elm.innerHTML = "Please enter more than 10 characters" ;
            retVal = false ;
           }

           if(phone.value.length < 10 || phone.value.length > 10){
            let elm = phone.nextElementSibling ;
            elm.innerHTML = "Please enter 10 digit phone number" ;
            retVal = false ;
           }

           if(pass.value.length < 7 ){
            let elm = pass.nextElementSibling ;
            elm.innerHTML = "Please enter stong password" ;
            retVal = false ;
           }
           if(pass.value != cpass.value ){
            let elm = cpass.nextElementSibling ;
            elm.innerHTML = "Please enter same password entered above" ;
            retVal = false ;
           }

           
           return retVal ;

        }
    </script>
</body>
</html>
