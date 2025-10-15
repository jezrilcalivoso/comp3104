#### COMP3104 – Developer Operations

# GitHub Action Status Badge
[![CI](https://github.com/jezrilcalivoso/comp3104/actions/workflows/ci.yml/badge.svg)](https://github.com/jezrilcalivoso/comp3104/actions/workflows/ci.yml)

# Commit Msg Hook
```
#!/bin/sh
COMMIT_MSG_FILE=$1
COMMIT_MSG=$(cat $COMMIT_MSG_FILE)

if ! echo "$COMMIT_MSG" | grep -Eq "^(feat|fix|docs|style|refactor|test|chore): .+"; then
  echo "Commit message must follow the format: <type>: <description>"
  echo "Example: feat: add user authentication"
  exit 1
fi
```