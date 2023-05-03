Guess the word!
I'm thinking of a word. Can you guess what it is? Here's a clue: it's a programming language.

To make a guess, simply type your answer in the box below and click the "Guess" button.

<input type="text" id="guess-box">
<button onclick="checkGuess()">Guess</button>
<span id="result"></span>

<script>
  function checkGuess() {
    const answer = "Python";
    const guess = document.getElementById("guess-box").value;
    if (guess.toLowerCase() === answer.toLowerCase()) {
      document.getElementById("result").innerHTML = "Congratulations! You guessed the word!";
    } else {
      document.getElementById("result").innerHTML = "Sorry, that's not the word I'm thinking of. Try again!";
    }
  }
</script>

| Pattern         | Explanation                                          | Example                |
| --------------- | ---------------------------------------------------- | ---------------------- |
| `/dir/`         | Ignore a directory                                   | `/node_modules/`       |
| `*.ext`         | Ignore files with a specific extension               | `*.log`                |
| `file`          | Ignore a specific file                                | `credentials.txt`      |
| `!file`         | Do not ignore a specific file                         | `!config.json`         |
| `#`             | Add a comment                                         | `# Ignore generated files` |
| `/dir/*`        | Ignore all files in a directory                      | `/build/*`             |
| `dir/*`         | Ignore all files in a directory, except for a file   | `docs/* !docs/index.md` |
| `**/pattern/`   | Ignore a directory and its subdirectories             | `**/__pycache__/`      |
| `*/pattern/`    | Ignore a directory and its immediate subdirectories   | `*/__pycache__/`       |
| `pattern/**/other` | Ignore a specific file in a directory and its subdirectories | `build/**/*.log` |


## Gitignore Pattern Matching Game

In this game, you will be shown a pattern from the `.gitignore` cheatsheet, and you must select the correct explanation from the options provided. Let's get started!

### Round 1

Here's your first pattern:

#### /dir/


Which of the following explanations is correct?

- [ ] Ignore files with a specific extension
- [ ] Ignore a specific file
- [x] Ignore a directory
- [ ] Do not ignore a specific file
<details> <summary>Click to reveal the answer</summary>
The correct answer is Ignore a directory. This pattern tells Git to ignore the entire dir directory and everything inside it.
</details>

### Round 2

Here's your next pattern:

*.log

Which of the following explanations is correct?

- [x] Ignore files with a specific extension
- [ ] Ignore a specific file
- [ ] Ignore a directory
- [ ] Do not ignore a specific file
<details> <summary>Click to reveal the answer</summary>
The correct answer is Ignore files with a specific extension. This pattern tells Git to ignore any file that ends with .log, such as error.log or debug.log.
</details>

### Round 3

Here's your next pattern:

!config.json


Which of the following explanations is correct?

- [ ] Ignore files with a specific extension
- [ ] Ignore a specific file
- [ ] Ignore a directory
- [x] Do not ignore a specific file
<details> <summary>Click to reveal the answer</summary>
The correct answer is Do not ignore a specific file. This pattern tells Git to include config.json in the repository, even if it matches another ignore pattern. The ! symbol negates the ignore rule.
</details>

### Round 4

Here's your next pattern:

/docs/* !docs/index.md


Which of the following explanations is correct?

- [ ] Ignore files with a specific extension
- [ ] Ignore a specific file
- [ ] Ignore a directory
- [x] Ignore all files in a directory, except for a specific file
<details> <summary>Click to reveal the answer</summary>
The correct answer is Ignore all files in a directory, except for a specific file. This pattern tells Git to ignore all files in the docs directory, except for index.md. The ! symbol negates the ignore rule for that file.
</details>

### Round 5

Here's your final pattern:

**/pycache/

Which of the following explanations is correct?

- [ ] Ignore files with a specific extension
- [x] Ignore a directory and its subdirectories
- [ ] Ignore a specific file
- [ ] Do not ignore a specific file
<details> <summary>Click to reveal the answer</summary>
The correct answer is Ignore a directory and its subdirectories. This pattern tells Git to ignore any directory named pycache and any subdirectories under it. The ** symbol matches any number of directories.
</details>

Congratulations, you've completed the Gitignore Pattern Matching Game! I hope this helped you learn the `.gitignore` cheatsheet better.


Which of the following explanations is correct?

<div id="answer-5">
    <label>
        <input type="radio" name="answer-5" value="option-1"> Ignore files with a specific extension
    </label>
    <label>
        <input type="radio" name="answer-5" value="option-2"> Ignore a directory and its subdirectories
    </label>
    <label>
        <input type="radio" name="answer-5" value="option-3"> Ignore a specific file
    </label>
    <label>
        <input type="radio" name="answer-5" value="option-4"> Do not ignore a specific file
    </label>
</div>

<script>
document.getElementById('answer-5').addEventListener('change', function(event) {
    if (event.target.value === 'option-2') {
        alert('Correct! The pattern **/__pycache__/ ignores the __pycache__ directory and its subdirectories.');
    } else {
        alert('Sorry, that\'s incorrect. The correct answer is "Ignore a directory and its subdirectories."');
    }
});
</script>
