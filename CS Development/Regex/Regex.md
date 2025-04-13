# 🔹 **Regex Cheatsheet (Quick Reference)**
[[Software Development]]


| Syntax | Description | Example | Matches |
| --- | --- | --- | --- |
| `.` | Any character except newline | `a.b` | `acb`, `a7b`, `a@b` |
| `^` | Start of string | `^a` | `apple`, but not `banana` |
| `$` | End of string | `e$` | `bike`, `hike` |
| `*` | 0 or more times | `lo*` | `l`, `lo`, `loo`, `looo` |
| `+` | 1 or more times | `lo+` | `lo`, `loo`, `looo` |
| `?` | 0 or 1 time | `colou?r` | `color`, `colour` |
| `{n}` | Exactly n times | `a{3}` | `aaa` |
| `{n,}` | n or more times | `a{2,}` | `aa`, `aaa`, `aaaa` |
| `{n,m}` | Between n and m times | `a{2,4}` | `aa`, `aaa`, `aaaa` |
| `[...]` | Any one character from the set | `[abc]` | `a`, `b`, or `c` |
| `[^...]` | Any one character *not* in the set | `[^0-9]` | anything except digits |
| \` | \` | OR operator | \`cat |
| `()` | Grouping | `(ha)+` | `ha`, `haha`, `hahaha` |
| `\d` | Digit (0–9) | `\d{2}` | `23`, `07` |
| `\D` | Non-digit | `\D+` | `abc`, `!@#` |
| `\w` | Word character (a-z, A-Z, 0-9, \_) | `\w+` | `hello_123` |
| `\W` | Non-word character | `\W+` | `!!`, |
| `\s` | Whitespace (space, tab, newline) | `\s+` | , `\n`, `\t` |
| `\S` | Non-whitespace | `\S+` | `text` |
| `(?=...)` | Positive lookahead | `\d(?=px)` | digit followed by 'px' |
| `(?!...)` | Negative lookahead | `\d(?!px)` | digit not followed by 'px' |

---

## 📘 Beginner Regex Guide

### What is Regex?

Regex stands for **Regular Expression**, a sequence of characters that define a search pattern. It's used for **matching**, **searching**, **extracting**, and **replacing** patterns in strings.

### Where Is It Used?

- Searching in text (e.g., finding phone numbers or emails)
- Validating input (e.g., ensuring an email is in the correct format)
- Data cleaning and transformation
- Log file parsing
- Programming languages like Python, JavaScript, Java, etc.

### Example:

To find all emails in a string:

```
\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b
```

---

## 📚 Regex Learning Resources & Documentation

### 📄 Official Docs & Tools

- **MDN Regex Guide (JavaScript)**:  
	[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular\_Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
- **Python re module docs**:  
	[https://docs.python.org/3/library/re.html](https://docs.python.org/3/library/re.html)
- **Regex101 (Testing + Explanation)**:  
	[https://regex101.com/](https://regex101.com/) — Test regex with detailed explanations
- **Regexr (Practice + Community)**:  
	[https://regexr.com/](https://regexr.com/) — Has examples, cheatsheets, and user-made patterns

---

## 🎥 Video Recommendations

- **Regex in 100 Seconds (Fireship)**  
	YouTube: [https://youtu.be/rhzKDrUiJVk](https://youtu.be/rhzKDrUiJVk)
- **Regex Crash Course (freeCodeCamp)**  
	YouTube: [https://youtu.be/7DG3kCDx53c](https://youtu.be/7DG3kCDx53c) — Longer deep-dive

---

## 🧠 Tips for Learning

- Start with simple patterns like `\d` or `.` to get used to the idea of matching.
- Practice with tools like [Regex101](https://regex101.com/) and [Regexr](https://regexr.com/).
- Work on small projects like:
	- Email validator
	- Phone number extractor
	- Log file parser