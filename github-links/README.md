# ![GitHub Icon](https://raw.githubusercontent.com/8rents/_/i/h1/github.png) Understanding GitHub  URLs & Links in README's 

> ***GitHub takes some liberties that could break links in standard markdown. Here is a guide to making sense of GitHub URLs and properly formatting them for backwards compatibility with README and index files.***XAZ

---

## The anatomy of a GitHub Link within a README

```bash
# A basic repository URL
https://  github.com/ 8rents / github-urls /
^		 ^           ^        ^
Protocol  Website     Username Repository
```

- **Protocol ---** Generally `http` or `https`

- **Website ---** GitHub.com obviously

- **Username** --- *after the 3rd* slash  
  The User's name on GitHub
  
-  **Repository** --- *after the 4th slash* 
  The name of the repository you are viewing

  
  
  ## Repository Internal URLs & Paths
  
  Internal URLs begin after the 5th slash(after the repository name) in the address bar. The first 2 values are **page type** and **branch**. 
  
  ### Position 1 --- Page  Type
  
  Potential Values:  **`tree`** | **`blob`**
  
  - **Tree** is a **directory list** (aka index file or on GitHub a README).
    - This will show the list of files in the folder above the README.
    - Note that you do not need to type `README.md` after `tree` it will show the index file automatically. Typing a file name will result in a 404
  - **Blob** is a **File**.
    - Blob will not show the list of files in the current folder above the README. 
    - Note that you need to type the actual file name (like `README.md`) after blob. Not typing a filename will result in a 404.
  
  ```bash
  # Tree Example
  tree / main / docs / 01-portable-setup-configs / 
  ^      ^      ^      ^
  page | branch|dir  | file 
  
  # Blob Example
  blob / main / docs / 01-portable-setup-configs / README.md
  ```
  
  Both of the above URLs will display the README.md in the `01-portable-setup-configs` folder. The blob URL will ommit the file list above the README. The tree example will show it.

---

**🤍 2023 [Brenton Holiday](https://brenton.holiday)**