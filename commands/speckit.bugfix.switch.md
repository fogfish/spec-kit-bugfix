---
description: "Switch to the spec for bug fixing"
---

# Switch bugfix context

Update current context into existing feature. The feature identity is define by user.

## User Input

```text
$ARGUMENTS
```

## Outline

1. **Validate feature**:
   - Check `specs/{feature}` dir exists, report an error to user if missing.

2. **Checkout feature branch**:
   - Checkout a new `{feature}` branch using git command, always use main branch as source. 

3. **Feature context update**:
   - Update `.specify/feature.json` with `specs/{feature}`  

4. **Agent context update**:
   - Update the plan reference between the `<!-- SPECKIT START -->` and `<!-- SPECKIT END -->` markers in `.github/copilot-instructions.md` to point to the feature plan file `specs/{feature}/plan.md` 
