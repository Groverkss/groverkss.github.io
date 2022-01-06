---
layout: post
title:  My LLVM Commit Workflow
categories: post
---

This is my workflow for commiting a patch from phabricator to LLVM git repo.

<!--more--> I started following this religously after I accidently sent 14
commited to LLVM monorepo which were supposed to go as 1 commit {% sidenote '1' '[The horror](https://reviews.llvm.org/D112867#3168270)' %} and then
proceeded to cry all night. 

```bash
arc patch D<patch-number> # Pull patch
git pull --rebase https://github.com/llvm/llvm-project.git main
git show # Ensure the patch looks correct.
ninja check-mlir # Run tests
git push https://github.com/llvm/llvm-project.git HEAD:main
```
