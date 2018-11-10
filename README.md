# Lubuntu.me Posts

This repository hosts all modern Lubuntu.me blog posts. They're written in Markdown, and using a Python wrapper, automatically created and uploaded.

Put your Wordpress credentials in user.yaml under the following format:

```
---
url:
username:
password:
```

To update a blog post, run `./update-post PATH/TO/POST/DIR` after your credentials are in the YAML file. **Please only use the parent directory as an argument.**
