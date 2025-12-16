<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
</head>
<body>

    <h2>Register</h2>

    <form id="regForm">
        <label for="fullname">Full Name:</label><br>
        <input type="text" id="fullname" name="fullname" required><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" required><br><br>

        <label for="password">Password:</label><br>
        <input type="password" id="password" name="password" required><br><br>

        <button type="submit">Submit</button>
    </form>

    <p id="message"></p>

    <script>
        document.getElementById("regForm").addEventListener("submit", function(e) {
            e.preventDefault(); // Prevent default form submission

            const fullname = document.getElementById("fullname").value;
            const email = document.getElementById("email").value;
            const password = document.getElementById("password").value;
            const message = document.getElementById("message");

            message.innerText = ""; // Clear previous messages

            // Basic validation example
            if (password.length < 6) {
                message.innerText = "Password must be at least 6 characters long.";
                return;
            }

            // If everything is okay
            message.innerText = "Form submitted successfully!";
        });
    </script>

</body>
</html>
