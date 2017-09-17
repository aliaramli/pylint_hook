# pylint_hook
testing the https://github.com/sebdah/git-pylint-commit-hook

theres two python file being tested here. one is quiz.py and another one is problem.py

you may edit the problem.py to make the syntax wrong, function declaration wrong etc..

ensure that you already have all the dependency python module in requirements.txt

or in you virtual environment you can run 

``` pip install -r requirements.txt ```

to have the pylint configuration file setup, you need to run setup_pylint_pre_commit.sh

in pylint_tools directory

``` ./setup_pylint_pre_commit.sh ```

now you are ready to test git commit (pre-commit validation)

just make changes to problem.py

add file changes to stages

and git commit -m "<message>"

you should able to see error message..

notice that i ve disabled all other warning. this will only check against code error...


# NOTES

I have noticed that if i append changes to .pylintrc somehow sometimes git-pylint-commit-hook didnt load the configuration. so i decided to make use the command parameter directly in .git/hook/pre-commit file.
