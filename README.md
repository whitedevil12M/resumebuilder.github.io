<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resume Builder</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        form {
            max-width: 600px;
            margin: auto;
        }

        label {
            display: block;
            margin-bottom: 8px;
        }

        input, textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 16px;
            box-sizing: border-box;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h2>Resume Builder</h2>
    <form id="resumeForm">
       
       <h3> RESUME </H3>
       
       <label for="fullName">Full Name:</label>
        <input type="text" id="fullName" name="fullName" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="phone">Phone:</label>
        <input type="tel" id="phone" name="phone" required>

        <label for="address">Address:</label>
        <input type="text" id="address" name="address" required>

        <label for="summary">Summary:</label>
        <textarea id="summary" name="summary" rows="4" required></textarea>

        <label for="experience">Experience:</label>
        <textarea id="experience" name="experience" rows="4" required></textarea>

        <label for="education">Education:</label>
        <textarea id="education" name="education" rows="4" required></textarea>

        <label for="Nationality">Nationality:</label>
        <textarea id="Nationality" name="Nationality"  required></textarea>
        
         <label for="language">language:</label>
        <textarea id="language" name="language"  required></textarea>

        
        <button type="button" onclick="generateResume()">Generate Resume</button>
    </form>

    <div id="resumeOutput"></div>

    <script>
        function generateResume() {
            // Retrieve form values
            var fullName = document.getElementById('fullName').value;
            var email = document.getElementById('email').value;
            var phone = document.getElementById('phone').value;
            var address = document.getElementById('address').value;
            var summary = document.getElementById('summary').value;
            var experience = document.getElementById('experience').value;
            var education = document.getElementById('education').value;
            var Nationality = document.getElementById('Nationality').value;
            var language = document.getElementById('language').value;

            // Create a simple resume format
            var resumeText = `
                <h3>${fullName}</h3>
                <p>Email: ${email}</p>
                <p>Phone: ${phone}</p>
                <p>Address: ${address}</p>

                <h4>Summary:</h4>
                <p>${summary}</p>

                <h4>Experience:</h4>
                <p>${experience}</p>

                <h4>Education:</h4>
                <p>${education}</p>
                
                 <h4>Nationality:</h4>
                <p>${Nationality}</p>
                
                <h5>language:</h5>
                <p>${language}</h5>
            `;

            // Display the generated resume
            document.getElementById('resumeOutput').innerHTML = resumeText;
        }
    </script>
</body>
</html>


