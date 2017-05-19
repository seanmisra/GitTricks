# GitTricks

<h2>Stage all changes</h2>
<code>git add .</code> 

<h2>Undo all changes</h2> 
<code>git stash -u</code>

<h2>Delete last commit pushed to GitHub</h2>
<ul>
  <li>To see last two commits: <code>git rebase -i HEAD~2</code></li>
  <li>Delete the last commit with <code>dd</code> on the second line</li>
  <li>Save the file with <code>:wq</code></li>
  <li>Force the changes to GitHub <code>git push -f origin master</code> - replace master with branch name if needed</li>
</ul>

<h2>Remove all .DS_Store files from Git repo</h2>
<ul> 
  <li><code>git rm --cached "*.DS_Store"</code></li>
  <li><code>git commit -m "Remove .DS_Store files"</code></li>
  <li>And make sure to add .DS_Store to the .gitignore file</li>
</ul>

<h2>LazyGit: add, commit, push </h2>
<p>Add the code below to .bash_profile or .bashrc. Make sure to then restart the terminal for changes to take effect.</p>

```
function lazygit() {
    git add .
    git commit -m "$1"
    git push origin master
}
```
<p>Can commit all changes and push to master branch like this: <code>lazygit "test push"</code>

<h2>Edit last commit's message</h2>
<ul>
  <li>Edit message: <code>git commit --amend -m "Better Message"</code></li>
  <li>Force push to GitHub: <code>git push -f</code></li>
</ul>

<h2>Amend prior commit</h2>
<ul> 
  <li>Stage changed files: <code>git add .</code>
  <li>Amend last commit w/o changing message: <code>git commit --amend --no-edit</code>
  <li>Force push to GitHub: <code>git push -f</code></li>
</ul>

<h2>Clean commit log</h2> 
<ul>
  <li>Enter: <code>git log --oneline</code></li>
  <li>For tags, branches, and some ASCII art use: <code>git log --oneline --graph --decorate</code></li>
</ul>

<h2>Change git status colors</h2>
<p>Add the code below to ~/.gitconfig</p>

```
[color "status"]
  added = blue bold
  changed = cyan bold
  untracked = red
```
<p>The specific colors can be customized as desired. More options here: http://misc.flogisoft.com/bash/tip_colors_and_formatting</p>

<h2>Git-Extras</h2>
<p>Download instructions are here: https://github.com/tj/git-extras/blob/master/Installation.md</p>
<p>For example, with a Mac and Homebrew you can run: <code>brew install git-extras</code></p>
<ul>
  <li>See commit count: <code>git count</code></li>
  <li>Output repo summary: <code>git summary</code></li>
  <li>Display effort stats: <code>git effort</code></li>
</ul>
<p>More commands here: https://github.com/tj/git-extras/blob/master/Commands.md</p>
