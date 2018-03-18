---
layout: post
title: My Jekyll Blogging Workflow
---

```shell
$ git checkout -b draft/my-new-post master
Switched to a new branch 'draft/my-new-post'
$ bundle exec jekyll draft 'My New Post'
New draft created at _drafts/my-new-post.md.
# ... write write write ...
$ git add _drafts/my-new-post.md
$ git commit -m 'Write draft for "My New Post"'
[draft/my-new-post 4a31eedc] Write draft for "My New Post"
 1 file changed, 420 insertions(+)
 created mode 100644 _drafts/my-new-post.md
$ bundle exec jekyll serve --drafts
# ... post looks good ...
$ bundle exec jekyll publish _drafts/my-new-post.md
Draft _drafts/my-new-post.md was moved to _posts/2018-03-17-my-new-post.md
$ git add _drafts/my-new-post.md _posts/2018-03-17-my-new-post.md
$ git commit -m 'Publish "My New Post"'
[draft/my-new-post 82cfbf58] Publish "My New Post"
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename _drafts/my-new-post.md => _posts/2018-03-17-my-new-post.md (100%)
$ git checkout master
Switched to branch 'master'
$ git merge draft/my-new-post
 1 file changed, 420 insertions(+)
 created mode 100644 _posts/2018-03-17-my-new-post.md
```
