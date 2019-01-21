# cmput496-assignment1-tests

# Install
If you're already using a git repo in your main assignment folder
```
echo "tests/" >> .gitignore
```
OR look into [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) if you want to be fancy.

```
cd <YOUR_ASSIGNMENT_DIR>
git clone https://github.com/tchell/cmput496-assignment1-tests tests/
```
### Note:
If you want to install the test folder somewhere other than your assignment root you will have to change 
each line in all.tst to match the relative path of wherever you call `gogui-regress` from.

# Usage

Run all the tests
```
gogui-regress -output tests/ <YOUR_GO_PROGRAM> @tests/all.tst
```
Run a single test
```
gogui-regress -output tests/ <YOUR_GO_PROGRAM> tests/<test_file>
```
*notice you only use the @ if you are running multiple tests*

If you want to select a few different tests to run then add a `#` in front of each test you'd like to omit in `all.tst`.
