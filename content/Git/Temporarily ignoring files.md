There are cases where you want to temporarily ignore files, but do not want them to be untracked in general (i.e. if you and your team agreed to not check in `schema.rb` files in Pull Requests in a rails project). To achieve that, just run

```bash
git update-index --assume-unchanged <file>
```

If you later want to track this file again (i.e. when you are checking out master), run

```bash
git update-index --no-assume-unchanged <file>
```
