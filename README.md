GitHub Actions to delete issues and issue comments other than the specified user

```yaml
name: Protect issues and comments
on:
  issues:
    types:
      - opened
  issue_comment:
    types:
      - created
jobs:
  protect-issues:
    runs-on: ubuntu-latest
    steps:
      - uses: kimromi/protect-issues@main
        with:
          github_token: ${{ secrets.PERSONAL_ACCESS_TOKEN }}
          protected_users: "kimromi1\nkimromi2"
```
