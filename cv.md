# Dmitriy Ponomarev

## _Frontend developer_

## Contacts:

**Email** : kikkyow18@gmail.com

**Github**: https://github.com/Dima-Ponomarev

**Phone**: +7(951)215-49-70

---

## Info:

Aspiring frontend developer dedicated to building resposive and optimised websites. Learn fast and continuously.

Plan to become middle frontend developer in 2 years.

## Hard skills:

- **Technologies** : HTML5/CSS3, SASS/SCSS, JavaScript, React JS, Git

- **Paradigms** : OOP, Functional Programming

## Code example:

<details><summary>Game Contoller module for tic tac toe game</summary>
<p>

```JavaScript

const gameController = (() => {
    const playerX = Player('X');
    const playerO = Player('O');
    let round = 0;
    let gameIsOver = false;

    const playRound = (tileIndex) =>{
        const player = getCurrentPlayer();
        player.occupiedTiles.push(tileIndex);
        gameBoard.setTile(tileIndex, player.getSign());
        const winner = checkWinner(player.occupiedTiles);
        if (checkWinner(player.occupiedTiles)){
            gameIsOver = true;
            console.log('gg')
            displayController.setStatus(`Player ${player.getSign()} has won!`);
            return;
        }

        if (round === 8) {
            gameIsOver = true;
            displayController.setStatus('Players drew!')
            return;
        }
        round++;
        player.getSign() === "X" ? displayController.setStatus("Player O's turn") :
            displayController.setStatus("Player X's turn");
    }

    const getCurrentPlayer = () =>{
        return round % 2 === 1 ? playerO : playerX;
    }

    const checkWinner = (occupiedTiles) => {
        let status = false;
        winConditions =[
            [0, 1, 2],
            [3, 4, 5],
            [6, 7, 8],
            [0, 3, 6],
            [1, 4, 7],
            [2, 5, 8],
            [0, 4, 8],
            [2, 4, 6]
        ];

        winConditions.forEach(winCondition => {
            if (winCondition.every(index => occupiedTiles.includes(index))){
                status = true;
            }
        });
        return status;
    }

    const getGameIsOver = () =>{
        return gameIsOver;
    }

    const reset = () =>{
        round = 0;
        gameIsOver = false;
        playerO.reset();
        playerX.reset();
    }

    return{
        playRound,
        getGameIsOver,
        reset
    }
})();
```

</p>
</details>

## My Projects:

[Tic tac toe](https://github.com/Dima-Ponomarev/Tic-Tac-Toe)

[Coloors](https://github.com/Dima-Ponomarev/Coloors)

[Beatmaker](https://github.com/Dima-Ponomarev/Beatmaker)

[Etch-a-sketch](https://github.com/Dima-Ponomarev/Etch-a-Sketch)

[Library](https://github.com/Dima-Ponomarev/Library)

## Education:

- ISTU Institute of Informatics and Computer Engineering Senior

- [The Odin Project](https://www.theodinproject.com/) student

## English:

Upper-Intermediate
