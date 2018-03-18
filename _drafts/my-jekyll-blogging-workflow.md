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
$ git add _drafts/
$ git commit -m 'Write draft for "My New Post"'
[draft/my-new-post 4a31eedc] Write draft for "My New Post"
 1 file changed, 420 insertions(+)
 created mode 100644 _drafts/my-new-post.md
$ bundle exec jekyll serve --drafts
# ... post looks good ...
$ bundle exec jekyll publish _drafts/my-new-post.md
$ git add _drafts/ _posts/
$ git commit -m 'Publish "My New Post"'
$ git checkout master
$ git merge draft/my-new-post
```
