---
title: Branch protection
category: Best Practice
order: 1
---

### Status checks before merging

You can change the repository setting to block merge when security scan result is not passed.<br>
Go to "Settings->Branches->Branch protection rules->Add rule" and check "Require status checks to pass before merging". Then merge alert can be made when a vulnerability exists.

![](../../images/merge-block.png)

By default, the feature does not apply to the administrator.<br>
If you check "Include administrators", the administrator also applies. 

![](../../images/merge-include-admin.png)

> "Merge pull request" button will be disabled if any of the inspection items on NShiftKey have failed to pass.

![](../../images/merge-not-pass.png)
