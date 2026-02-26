# information

This repository stores public metadata about the organization’s deployed webpages and their contributors.

It contains two JSON files:

- `pages.json`
- `contributors.json`

---

## 📄 pages.json

`pages.json` is a simple array of strings.

Each string represents a deployed webpage owned or maintained by the organization.

### Example

```json
[
	"ScheduleGenerator",
	"Exam-calendar-generator"
]
```

### Rules

- Each entry must be a valid deployed webpage URL.
- Do not add duplicate entries.
- Only organization-owned pages should be listed.

---

## 👥 contributors.json

`contributors.json` maps webpages to their contributors.

### Example

```json
[
  {
    "page": "https://example.com",
    "contributors": ["username1", "username2"]
  }
]
```

### Fields

- `page` — A string that must match an existing entry in `pages.json`.
- `contributors` — An array of GitHub usernames who have had accepted commits related to that page.

### Rules

- The `page` value must already exist in `pages.json`.
- Do not duplicate contributors.
- Do not modify unrelated entries.
- Keep the file properly formatted JSON.

---

## ➕ How to Add Yourself as a Contributor

If your commit has been **accepted into another organization repository**, you must open a Pull Request (PR) in this repository to be added.

### 1️⃣ Update `contributors.json`

Add your GitHub username under the appropriate page entry.  
If the page does not yet have an entry in `contributors.json`, create one in the correct format.

### 2️⃣ Open a Pull Request

**PR Title format:**

```
Add {username} to {repo}
```

Example:

```
Add johndoe to website
```

**PR Description format:**

```
Commit accepted {commit link}
```

The commit hash must be a clickable GitHub link to the accepted commit.

Example:

```
Commit accepted [abc123def456](https://github.com/org/repo/commit/abc123def456)
```

---

## ✅ Contribution Requirements

Your PR will only be merged if:

- The commit was accepted into the referenced repository.
- The commit link is valid and publicly accessible.
- The page exists in `pages.json`.
- JSON formatting is correct.
- No unrelated changes were made.

---

## 🚫 Do Not

- Modify other contributors unless correcting duplicates.
- Change formatting unnecessarily.
- Add pages without approval.
- Submit a PR without a valid commit link.

---

Thank you for contributing 🎉