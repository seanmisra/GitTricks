# GitTricks

<h2>Stage all changes</h2>
<code>git add .</code> 

<h2>Delete a commit pushed to GitHub</h2>
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
