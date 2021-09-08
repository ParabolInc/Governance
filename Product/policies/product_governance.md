# Proposal: Move Product Gov To GitHub

Circle Parent: https://www.notion.so/Product-7d3424b27bd942c6be4819143748c48f
Create Time: August 16, 2021 12:30 PM
Created By: Matt Krick
Last Edited By: Matt Krick
Last Edited Time: August 16, 2021 12:58 PM
Proposal?: Yes
Purpose: Improve governance

# Tension

There is a lot of friction when it comes to proposing new governance:

- A proposal commonly includes updates to both policies & roles, but changes in notion are per-document
- The notion notifications leave something to be desired, which leaves many orphaned proposals
- Notion does not show individual line diffs
- Notion does not offer a great version control

# Pros

- GitHub has a wonderfully robust notification system. Comments are long lived on particular lines and work well across changing versions. It was literally built to do this
- A proposal (pull request) naturally includes all the proposed changes, making is easy for all reviewers to see exactly what is changing
- Proposals and merges can trigger automated workflows
- GitHub Pages turns markdown documents into HTML documents that are hosted. We can create our own GitLab-esque handbook to share with the world
- Changes are easy to see, which means the author doesn't have to write as much in the proposal. Small fixes like formatting and typos are much more likely to get fixed because you can see exactly what the change is
- The product team is already pretty technical & familiar with git
- In the future, we could turn this into a product. Murmur is trying this already, but I think they might be headed in the wrong direction.

# Cons

- Files will be written in markdown. This may look foreign to some, but Notion uses all the same markdown shortcuts. E.g. if you write `# Cons` , it will be a header in both notion & GitHub.
- Notion is a WYSIWYG and markdown files require an editor to be a WYSIWYG. Thankfully, by pressing `.` in the repo, the user gets a WYSIWYG editor!
- Tables are harder to create. However, there are conversion tools that let you copy & paste from Google Sheets or notion (e.g. [https://www.convertcsv.com/csv-to-markdown.htm](https://www.convertcsv.com/csv-to-markdown.htm))
- The nomenclature is different (e.g. a proposal would be called a pull request)

# Proposal

I propose we move to GitHub and use GitHub Pages to make the governance easier to read for non-tech folks. While extra automation is possible, it is out of scope for this initial proposal.

- Governance for the product team is moved to here: [https://github.com/ParabolInc/Governance](https://github.com/ParabolInc/Governance)
- Proposals are treated as Pull Requests. An example proposal is here: [https://github.com/ParabolInc/Governance/pull/1/files](https://github.com/ParabolInc/Governance/pull/1/files)
- GitHub Pages is used as a friendlier way to read the governance. Example here: [https://parabolinc.github.io/Governance/Product/roles/BUG_SQUASHER.html](https://parabolinc.github.io/Governance/Product/roles/BUG_SQUASHER.html)
- In the future, we can add auto-generated table of contents, just like notion
- In the future, we can add GitHub actions that can move the governance process along, similar to how the slackbot works today. It can message individuals via slack or email, change the status, etc.
