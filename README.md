# Git Flow: A Successful Branching Model

---

## What is Git Flow?
- Branching strategy for Git
- Created by Vincent Driessen
- Ideal for release-based workflows
- Provides structured approach to version control

---

## Core Branches

### Main Branch
- Production-ready code
- Contains released versions
- Never receives direct commits
- Tagged with version numbers

### Develop Branch
- Integration branch
- Source of latest development changes
- Where features come together

---

## Supporting Branches

### Feature Branches
```bash
git checkout -b feature/new-feature develop
# work on feature
git merge --no-ff feature/new-feature
```

### Release Branches
```bash
git checkout -b release-1.2 develop
# prepare release
git merge --no-ff release-1.2
```

### Hotfix Branches
```bash
git checkout -b hotfix-1.2.1 master
# fix critical bug
git merge --no-ff hotfix-1.2.1
```

---

## Branch Lifecycle

1. **Feature**
   - Start: branch from develop
   - End: merge to develop

2. **Release**
   - Start: branch from develop
   - End: merge to master & develop

3. **Hotfix**
   - Start: branch from master
   - End: merge to master & develop

---

## Best Practices

- Never commit to master directly
- Use meaningful branch names
- Delete branches after merging
- Always use `--no-ff` for merges
- Tag all releases

---

## Benefits

- Clear release cycle
- Parallel development
- Organized codebase
- Emergency fixes possible
- Supports team collaboration

---

## Questions?
Contact: [Md Sohel Mia](https://www.sohel.pro)
