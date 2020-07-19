mkdir MergeConflict
cd MergeConflict/
git init
touch README.md
echo "echo Hello" > README.md
git add .
git commit -m"first commit on master"
git checkout -b new-branch
echo "Hello World" > README.md
git add .
git commit -m"first commit on new-branch"
git checkout master
echo "Hola" > README.md
git add .
git commit -m"second commit on master"
git merge new-branch