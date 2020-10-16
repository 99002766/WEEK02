# WEEK02
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration</title>
    <script>
        function validata() {

            var names=['Swarnim','Shikhar','Junnu'];

            var low = /[a-z]/g;
            var upper = /[A-Z]/g;
            var numbers = /[0-9]/g;
            var spl = /[!@#$%^&*]/g;
            if(document.getElementById("username").value.length<5 || document.getElementById("username").value.length>15) {
                alert("Username is not in the length of 5 to 15");
            }

            else if(!document.getElementById("pass").value.match(low) || !document.getElementById("pass").value.match(upper) || !document.getElementById("pass").value.match(numbers) || !document.getElementById("pass").value.match(spl)) {
                alert("Invalid password, please use all the characters.");
            }

            else if(!document.getElementById("mail").value.match(/[a-z A-Z 0-9]@[a-z].[a-z]/)) {
                alert("Email id is not valid.");
            }

            else if(document.getElementById("phone").value.length!=10) {
                alert("Contact must have 10 digits");
            }

            else if(names.indexOf(username) !== -1)
            {
                alert('user name exists');
                document.getElementById("username").focus();
            }
            
            else
            {
                document.getElementById("printhere").innerHTML="successfully registered";
            }
        }

    </script>
</head>
<body>
    <form id="adduser" >
        Name <input type="text" id="username"> <br>
        Password <input type="password" id="pass"> <br>
        Email <input type="text" id="mail"> <br>
        Contact <input type="text" id="phone"> <br>
        Submit:<input type="submit" onclick="validata()">
    </form>
    <div id="printhere"></div>
    
</body>
</html>
