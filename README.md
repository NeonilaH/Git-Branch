1. In the local repository make branches for: Postman, Jmeter, CheckLists, Bug Reports, SQL, Charles, Mobile testing.
- `git branch Postman`
- `git branch Jmeter`
- `git branch CheckLists`
- `git branch bug_reports`
- `git branch SQL`
- `git branch Charles`
- `git branch Mobile_Testing`
2. Push all branches to an external repository
`git push origin --all`
3. In the Bag Reports branch, make a text document with the bug report structure
- `git checkout bug_reports`
- `touch bug_report.txt`
- `nano bug_report.txt`
1) Bug Number/id.
2) Bug title.
3) Priority.
4) Platform/Environment.
5) Description.
6) Steps to Reproduce.
7) Expected and Actual Result.
8) Attachments
`Ctrl+O` ---> `Enter` ---> `Ctrl+X`
4. Push the bug report structure to the external repository
- `git add bug_report.txt`
- `git commit -m "add bug report template txt file"`
- `git push --set-upstream origin bug_reports`
5. Merge the Bag Reports branch into Main
- `git checkout main`
- `git merge bug_reports`
6. Push main to external repository
- `git status`
- `git push`
7. In the CheckLists branch, outline the checklist structure.
- `git checkout CheckLists`
- `cat >> checklist_template.txt`
id
check description
check status (not run, pass, fail, skipped, blocked)
comment
- `Enter` ---> `Ctrl+C`
8. Push the structure to an external repository
- `git add checklist_template.txt`
- `git commit -m "add checklist txt file"`
- `git push --set-upstream origin CheckLists`
9. In the external repository make a Pull Request of the CheckLists branch in main Merge
- Compare and pull request
- Create pull request
- Merge pull request
- Confirm merge
- Pull request successfully merged and closed
10. Synchronize External and Local branches Main
- `git fetch`
- `git-pull`
