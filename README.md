# TechnohackIntern_Task2
<!DOCTYPE html>
<html>
<head>
    <title class="deva">Login Form</title>
    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
            background-image: url(https://t4.ftcdn.net/jpg/03/67/85/53/360_F_367855342_hC9tRkea0aqxsyqfOzBwjc9Tv3jiSmNz.jpg);
            background-size: contain;
        }
        .deva{
            
        }

        .container {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        label {
            font-weight: bold;
        }

        input[type="text"],
        input[type="password"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        .error {
            color: red;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Login</h2>
        <form id="loginForm">
            <div class="form-group">
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit">Login</button>
            <p id="errorMessage" class="error"></p>
        </form>
    </div>

    <script>
        document.getElementById("loginForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // You can add your authentication logic here
            if (username === "deva" && password === "Deva@123") {
                // Successful login, redirect or display a success message
                alert("Login successful!");
            } else {
                // Display an error message
                document.getElementById("errorMessage").textContent = "Invalid username or password.";
            }
        });
    </script>
</body>
</html>

<!DOCTYPE html>: This declaration specifies the document type as HTML5.

<html>: The root element of the HTML document.

<head>: Contains meta-information and links to external resources, such as stylesheets and scripts.

<title class="deva">Login Form</title>: Sets the title of the HTML page to "Login Form." It also includes a "deva" class on the <title> element, although this is not a standard practice and does not have any visible effect.

<style>: This section contains inline CSS styles for styling the page.

The body element sets the background image and specifies a fallback font-family.
.container styles define the appearance of the login form container.
.form-group adds margin below form elements.
label styles make labels bold.
input[type="text"], input[type="password"] styles text and password input fields.
button styles the login button.
button:hover styles the button when hovered over.
.error styles error messages in red.
<body>: This section contains the visible content of the HTML page.

Inside a <div> element with the class "container," there is a login form.
The form includes two form groups, one for the username and one for the password.
Each form group contains a label and an input field with specific styling.
A "Login" button is provided to submit the form.
An empty paragraph (<p>) with the ID "errorMessage" is included for displaying error messages.
<script>: JavaScript code is embedded within the HTML document.

The JavaScript code adds an event listener to the form with the ID "loginForm" to handle the form submission.
When the form is submitted, the code prevents the default form submission behavior (event.preventDefault()).
It retrieves the values entered in the username and password fields.
It checks if the username is "deva" and the password is "Deva@123."
If the credentials match, it displays a successful login alert.
If the credentials do not match, it displays an "Invalid username or password" error message in the paragraph with the ID "errorMessage."
