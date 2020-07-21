## Sudoku-Solver
Solve Sudoku with AI

## Synopsis

In this project you will extend the Sudoku resolution agent developed in the classes to solve Sudoku puzzles _Diagonal_ and implement a new restriction strategy called "naked twins". A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the further limitation that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the 3x3 rows, columns and blocks) . The naked twins strategy says that if you have two or more unassigned boxes in a unit and there are only two digits that can go into those two boxes, then those two digits can be removed from the possible assignments of all the other boxes in the same unit. .


## Fast guide

** ONLY NECESSARY TO WRITE THE CODE IN `solution.py`. **

1. Follow the class instructions to install and configure the `aind` [Anaconda] environment (https://www.continuum.io/downloads) which includes several important packages that are used for the project. OS X or Unix / Linux users can activate the aind environment by doing the following (Windows users simply run `activ aind`):
    
    `$ active source aind`

2. You can run a small set of test cases using the local test set.

    `(aind) $ python -m unittest -v`

3. Copy your class code for basic research and strategies, then add diagonal units to the top of the solutions.py file and complete the `naked_twins ()` function. The pseudocode for the `naked_twins ()` function is available [here] (https://github.com/udacity/artificial-intelligence/blob/master/Projects/1_Sudoku/pseudocode.md).

4. Run the test package again to check the progress. After passing all the test cases in the local test set, you can submit the project to run more complete tests with the remote test set:

    `(aind) $ udacity submit`

5. You can run the code with display (see the last section of the Readme file for more information)

    `(aind) $ python solution.py`


### Notes

- You will not receive credit for the project until you send the zip file created by `udacity submit` to your class.

- You need to send _exactly_ the zip file created by the CLI in step 3 in the classroom; If you make changes to the file, you will receive an error message when you try to send it to the classroom.


## Instructions

You must complete the required functions in the 'solution.py' file (copy the class code where indicated and add or extend with the new code as described below). The `test_solution.py` file includes some unit tests for local tests, but the main mechanism for testing your code is the Udacity Project Assistant command line utility described in the next section.

YOU MUST WAIT TO MODIFY OR WRITE YOUR OWN TEST OF THE UNIT AS PART OF COMPLETING THIS PROJECT. It is not necessary to write test cases, but the Project Assistant test suite is not shared with students, so it may be necessary to write your own tests to find and resolve any errors that arise there.

1. Add the two new diagonal units to `unitlist` at the top of solution.py. Run the local tests again with `python -m unittest` to confirm your solution.

1. Copy your class code for `delete ()`, `only_choice ()`, `reduce_puzzle ()` and `search ()` to the corresponding functions in the `solution.py` file.

1. Implement the `naked_twins ()` function (see pseudocode [here] (https://github.com/udacity/artificial-intelligence/blob/master/Projects/1_Sudoku/pseudocode.md) for help) and update ` reduce_puzzle () `to call it (along with other existing strategies). Run the local tests again with `python -m unittest -v` to confirm your solution.

1. Run remote tests with `udacity submit` to confirm your solution. If any of the remote test cases fail, use the comments to write your own local test cases for debugging.


## Enter

To submit your code, run `udacity submit` from a terminal in the top level directory of this project. You will be asked for a username and password the first time the script is run. If you log in with Google or Facebook, visit [this link] (https://project-assistant.udacity.com/auth_tokens/jwt_login) for alternative access instructions.

The Udacity-PA CLI tool is automatically installed with the conda AIND environment provided in the classroom, but you can also install it manually by running `pip install udacity-pa`. You can submit your score code by running `udacity submit`. The project wizard server has a collection of test units that will run on the code and provide feedback on any positive or negative outcomes. All test cases must be passed in the project wizard to approve the project.

Once the project has passed all the test cases in Project Assistant, send the zip file created by the `udacity submit` command in the classroom to automatically receive credit for the project. NOTE: You will not receive personalized feedback for this project on submissions that pass all test cases, however all other projects in the term provide personalized feedback on approved and failed submissions.


## Visualizations

** Note: ** The `pygame` library is required to view your solution; however, the `pygame` module can be problematic to install and configure. It should be installed by default with the AIND conda environment, but is not reliable on all operating systems or versions. Consult the pygame documentation [here] (http://www.pygame.org/download.shtml) or discuss among your colleagues in the slow group if you need help.

Running `python solution.py` will automatically try to display your solution, but you need to use the` assign_value` function (defined in `utils.py`) to track the progress of the puzzle solution for rebuilding during display.
