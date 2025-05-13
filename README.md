# String-Transform-Length
Designed to handle large inputs without explicitly constructing the transformed string.

## 🧩 Problem Statement
Given a string `s` consisting of lowercase English letters and an integer `t`, perform exactly `t` transformations.

### Transformation Rules:
1. If a character is `'z'`, replace it with `"ab"` (2 characters).
2. Otherwise, replace it with the **next character** in the alphabet (`'a'` → `'b'`, `'b'` → `'c'`, ..., `'y'` → `'z'`).

Return the **length** of the resulting string after `t` transformations.

> Since the result can be very large, return the length **modulo 10⁹ + 7**.

---

## 💡 Example
```
Input: s = "abcyy", t = 2
Output: 7

Step 1: "abcyy" → "bcdzz"
Step 2: "bcdzz" → "cdeabab" → length = 7
```
### Example 2:
```
Input: s = "azbk", t = 1
Output: 5

Step 1: "azbk" → "babcl" → length = 5
```
## 🛠️ Solution Approach

- Use **dynamic programming** to track how each letter evolves over `t` transformations.
- Avoid actual string building to maintain efficiency for large values of `t` and long strings.
- Time complexity: `O(t * 26)` — efficient since 26 letters are constant.

---

## 📁 Files

- `Solution.cs`: Main implementation in C#.
- `Program.cs`: Sample usage and test cases.
- `README.md`: Problem description and usage instructions.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/String-Transform-Length.git
   cd String-Transform-Length
   dotnet run
   ```
   
