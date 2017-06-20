# JQuery-Validation
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>jQuery Validation</title>
  <script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-3.2.1.min.js"></script>
  <script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.13.0/jquery.validate.min.js"></script>
  <!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<!-- Optional theme -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css">
<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
  <style>
  	input[type="text"]
  	{
  		background-color:#d1e8b4;
  		color:#366002;
  		margin:10px;
  	}
  	#password 
  	{
  		background-color:#d1e8b4;
  		color:#366002;
  		margin:10px;
  	}
  	#password2
  	{
  		background-color:#d1e8b4;
  		color:#366002;
  		margin:10px;
  	}
  </style>
</head>
<body>
<form id="emailForm" >
<div>
	<input name="email" placeholder="Email address" type="text">
</div>
<div>
	<input name="password" id="password" placeholder="Password" type="password">
</div>
<div>
	<input name="password2" id="password2" placeholder="re-enter" type="password">
</div>
<input class="btn btn-primary" id="submit-button" type="submit" value="Sign up">
</form>

<script>
$(document).ready(function() {
    $('#emailForm').validate({
    	rules:{
    		email:{
    			required:true,
    			email:true
    		},
    		password:"required",
    		password2:{
    			required:true,
    			equalTo:"#password"
    		}
    	},
    	messages:{
    		email:{
    			required:'Please enter an email addres',
    			email:'Please enter a <em>valid</em> email address'
    		}
    	}
    });
});
</script>
</body>
</html>
