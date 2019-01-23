## Description
This is a test suite for assignment 1. I tried to separate related tests into logical files so that specific functions can be tested.

If you have any problems, want to add tests, or have other improvements feel free to open an issue or implement them and open a pull request.

# Install

```
cd <YOUR_ASSIGNMENT_DIR>
```
If you're already using a git repo in your main assignment folder
```
echo "tests/" >> .gitignore
```
OR look into [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) if you want to be fancy.

```
git clone https://github.com/tchell/cmput496-assignment1-tests tests/
```
### Note:
If you want to install the test folder somewhere other than your assignment root you will have to change 
each line in all.tst to match the relative path of wherever you call `gogui-regress` from.

**Windows users likely have to edit all.tst and change the `/` to `\`.**

# Usage

Run all the tests
```
gogui-regress -output tests/ <YOUR_GO_PROGRAM> @tests/all.tst
```
Run a single test
```
gogui-regress -output tests/ <YOUR_GO_PROGRAM> tests/<test_file>
```
Then open `tests/index.html` in a browser to see the results.

*note: you only use the @ if you are running multiple tests*

If you want to select a few different tests to run then add a `#` in front of each test you'd like to omit in `all.tst`.
