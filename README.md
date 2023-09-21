# 9
 Follow the simple step-by-step instructions, and watch as the ingredients transform into a delectable masterpiece that will tantalize your taste buds and leave you craving for more. Perfect for gatherings, family meals, or a cozy night in, this recipe is bound to become a favorite in your repertoire."
<!DOCTYPE html>
<html ng-app="myApp">
<head>
    <title>Login Page</title>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>
<style>
body{font: 12px/20px 'Lucida Grande' Tahoma, Verdana, sans-serif;
    text-align: center;
}
</style>
    <script>
        var app = angular.module('myApp', []);
        app.controller('loginCtrl', function ($scope) {
            $scope.login = function () {
                var enteredUsername = $scope.username;
                var enteredPassword = $scope.password;

                if (enteredUsername === 'Admin' && enteredPassword === 'Password@123') {
                    $scope.message = 'Login Successful';
                    $scope.messageColor = 'green';
                } else {
                    $scope.message = 'Invalid username or password';
                    $scope.messageColor = 'red';
                }
            };
        });
    </script>
</head>

<body>
    <div ng-controller="loginCtrl">
        <h1>Login Page</h1>
        <form ng-submit="login()">
            <label for="username">Username:</label>
            <input type="text" id="username" ng-model="username" required><br><br>

            <label for="password">Password:</label>
            <input type="password" id="password" ng-model="password" required><br><br>

            <button type="submit">Login</button>
        </form>
      <div ng-show="message" style="color: {{ messageColor }}">{{ message }}</div>
    </div>
    </div>
</body>

</html>
