<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <h1>My GitHub Profile</h1>
                <p>Username: <a href="https://github.com/ZikwanIsmail" target="_blank">Zikwan Ismail</a></p>
                <p>Email: YOUR_EMAIL</p>
                <p>Location: YOUR_LOCATION</p>
                <p>Website: <a href="YOUR_WEBSITE" target="_blank">YOUR_WEBSITE</a></p>
                <p>Followers: <span id="followers"></span></p>
                <p>Following: <span id="following"></span></p>
                <p>Public Repositories: <span id="public_repos"></span></p>
                <p>Bio: <span id="bio"></span></p>
            </div>
        </div>
    </div>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
        $(document).ready(function() {
            $.getJSON("https://api.github.com/users/ZikwanIsmail", function(data) {
                $("#followers").text(data.followers);
                $("#following").text(data.following);
                $("#public_repos").text(data.public_repos);
                $("#bio").text(data.bio);
            });
        });
    </script>
</body>
</html>
