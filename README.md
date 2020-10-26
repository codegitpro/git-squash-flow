// Make sure you are on your change branch
git checkout <JIRA-ID>

// Squash your changes into one nice commit line, starting with the Jira Issue.
// Using SourceTree or other GIT tool, figure out the number of commits to squash (X) and 
// use the first rebase command below or find the first commit hash and use the second rebase 
// command below
git rebase -i HEAD~X 
OR
git rebase -i {first-commit-hash-on-branch}

// Pick the first item, replace 'pick' with 's' for the next items. Save and quit file.
// You should be presented with a new editor with the combined commit messages.
// Create a nice Jira based message and save the file
// Make sure to push to your remote branch using git push -f

// Make sure your development branch is up to date
git checkout development
git pull origin development

// Rebase your change onto the new development
git checkout <JIRA-ID>
git rebase development

// At this point you may need to resolve any conflicts.
// Ideally, you would retest here as well.

// Merge change onto development
git checkout development
git merge <JIRA-ID>

// Share to origin
git push origin development


we are gonna make some change in the below section
for the exercise of git workflow based on squash and merge

1. dev branch
2. ticket-1 branch
3. ticket-1 branch
4. ticket-1 branch
5. dev branch
6. dev branch