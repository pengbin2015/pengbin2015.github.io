---
title: Torch package error when install LangChain
description: >-
  When I tried to use the command “poetry install -E all” for the LangChain
  project based on the web page…
date: "2023-03-22T03:29:42.302Z"
categories: []
keywords: []
slug: /@pengbintech/torch-package-error-when-install-langchain-175c00672df4
---

When I tried to use the command “poetry install -E all” for the LangChain project based on the web page ([https://github.com/hwchase17/langchain/blob/master/.github/CONTRIBUTING.md](https://github.com/hwchase17/langchain/blob/master/.github/CONTRIBUTING.md)), I received an error like this:

```
Installing torch (1.13.1): Failed

  RuntimeError

  Unable to find installation candidates for torch (1.13.1)

  at venv/lib/python3.11/site-packages/poetry/installation/chooser.py:109 in choose\_for
      105│
      106│             links.append(link)
      107│
      108│         if not links:
    → 109│             raise RuntimeError(f"Unable to find installation candidates for {package}")
      110│
      111│         \# Get the best link
      112│         chosen = max(links, key=lambda link: self.\_sort\_key(package, link))
      113│"
```

In order to solve this error, you need to check the version of python and change it to python 3.10. Then the error will be solved!
