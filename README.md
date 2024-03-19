<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Horror Game</title>
</head>
<body>
    <h1>Horror Game</h1>
    <p>Welcome to the Horror Game. Your choices will determine your fate...</p>

    <div id="story">
        <p>You find yourself standing in front of a creepy old mansion. What do you do?</p>
        <button onclick="startGame()">Enter the mansion</button>
        <button onclick="runAway()">Run away</button>
    </div>

    <script>
        function startGame() {
            document.getElementById("story").innerHTML = "<p>You enter the mansion and hear strange noises coming from the basement. What do you do?</p><button onclick='exploreBasement()'>Explore the basement</button><button onclick='ignoreNoise()'>Ignore the noise</button>";
        }

        function runAway() {
            document.getElementById("story").innerHTML = "<p>You run away from the mansion, but as you look back, you see a shadowy figure watching you from the window...</p><button onclick='restartGame()'>Restart</button>";
        }

        function exploreBasement() {
            document.getElementById("story").innerHTML = "<p>You cautiously descend into the basement and find a hidden room. Inside, you discover an old diary that reveals the mansion's dark history...</p><button onclick='readDiary()'>Read the diary</button><button onclick='leaveBasement()'>Leave the basement</button>";
        }

        function ignoreNoise() {
            document.getElementById("story").innerHTML = "<p>You ignore the noise and continue exploring the mansion. Suddenly, you hear footsteps behind you...</p><button onclick='turnAround()'>Turn around</button><button onclick='keepWalking()'>Keep walking</button>";
        }

        function readDiary() {
            document.getElementById("story").innerHTML = "<p>As you read the diary, you learn about the mansion's previous owner, who conducted twisted experiments on unsuspecting victims...</p><button onclick='continueReading()'>Continue reading</button>";
        }

        function leaveBasement() {
            document.getElementById("story").innerHTML = "<p>You decide to leave the basement and return to the main hall. Suddenly, the door slams shut behind you, trapping you inside...</p><button onclick='panic()'>Panic</button><button onclick='searchForExit()'>Search for an exit</button>";
        }

        // Additional functions and story branches can be added as needed

        function restartGame() {
            location.reload();
        }
    </script>
</body>
</html>
