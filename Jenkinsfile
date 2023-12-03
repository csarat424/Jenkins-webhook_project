pipeline {
    agent any

    stages {
        stage('Build and Deploy') {
            steps {
                script {
                    // Checkout the repository
                    checkout scm

                    // Create the HTML and CSS file
                    writeFile file: 'index.html', text: '''
                        <!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
    <title>Sarat - DevOps Engineer</title>
</head>
<body>
    <div class="container">
        <h1>Sarat, fueled by an unwavering passion for technology and innovation</h1>
        <p>is on a relentless journey as an aspiring DevOps engineer, weaving together expertise and enthusiasm to architect seamless and efficient software ecosystems.</p>
    </div>
</body>
</html>
                    '''

                    // Commit and push changes to GitHub
                    sh 'git add .'
                    sh 'git commit -m "Add index.html"'
                    sh 'git push origin master'
                }
            }
        }
    }
}
