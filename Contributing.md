# Contribution Guidelines

When decided to contribute to this repository, please read the following and keep the repo's contribution rule. This is so that the repository content is consistent in design & its format as well as the module relevancy to help readers to browse & learn more effectively.

## Contribution Steps

Below is the direction as to how to start contributing properly using appropriate tools. Also **NOTE** that there are things that contributors have to abide by within the repository rule which will be described in the section below [Contribution & Review Request Mininum Requirements](#contribution-review-request-minimum-requirement).

#### 🚀 Clone The Repository

```bash
git clone "https://github.com/haneulab/c.git" ./c-docs
```

#### 🚀 Create Your Branch

```bash
git checkout -b <your_github_username>-branch
```

#### 🚀 Add Relevant Contents To Relevant Directory

The following content is an example demo for working in a directory in your new branch that you want to add to the repo.

The file must be extension of either `.md` or `.c` file. If you have any object files or executable please specify in the `.gitignore` so that they won't be pushed.

Each file you write must specify the name of the author, filename, file written date, and brief description about the file. For the example template, please refer to the `example_c_file.c` or `example_md_file.md` in the root directory.

#### 🚀 Clean Up Unnecessary Files Or Directories From Development Setting

If you want to ignore some specific files (which you should such as executables & any environmental directories or dot files). The root directory's `.gitignore` might not cover all the things your local environment creates. Then you can simply add a .gitinore file in this working directory and add the line that specifies the file pattern you want to ignore.

```bash
touch ./gitignore
```

```bash
# .gitignore
...
*.out
*.o
```

#### Git Commit & Push to Your Branch

**Git Add**

```bash
# for adding all files you added
git add .
# for adding a specific file (or patterned)
git *.c
```

**Git COMMIT**

```bash
git commit -m "your message about your current action (added a file/updated a file/...)"
```

**GIT PUSH**

```bash
git push --set-upstream origin your_branch_name
# SIDE NOTE
# When it asks you to authentication from github such as username & password
# you need to generate your own personal github token & replace the token that with the password (in the password section)
# TO CREATE NEW TOKEN
# 1. go to github.com
# 2. go to settings
# 3. go to developer settings in the left sticky menu
# 4. go to personal token & genereate
# 5. copy and save it somewhere only you can have access so you can use it later (it is only visible one time when it is generated)
```

#### Submit a Pull Request & Wait for Approval

---

## Contribution Review Request Minimum Requirement

1. Add New Contritutions in the sub folders listed below only.

2. Follow the convention for naming files.

3. Do NOT modify files that is not initially added by you or files that are in the root directory besides `contributors.md` where you will add your info as a contributor.

## File Creation Rule

These rules apply to the files that you create & push to the repo in your working branch.

- **nameing the file** : name the file that describes the content inside.
- **snake_style_declaration** : file names should be snake_style for a filename containing multiple words.
- **extensiion of the file** : set is to either `.c`, `.md`, `.gitignore`.

- **parent directory choice** : please put your file into the topic-relevant directory from the list below.

- If the file is NOT `.gitignore`, please do specify the author credits & brief description about the file content at the top of the file.

For example, take a look at `example.c` file I want to push

```c
/**
 * @file : example.c
 * @author : John Doe : john@doe.com
 * @brief : example c file showing the demo of the top of the file
 * @date : 06/02/2022
 * @copyright Copyright (c) 2022
 */

#include <stdio.h>

int main()
{
    return 0;
}
```

## Working Directory Options

You may contribute to the following directories for the C documentation content. Please add only the relevant contents to these directories to keep them organized.

- `/intro_to_c` : introductory concepts such as syntax, datatype, control-flow statements, ...

- `/pointers_arrays_strings` : anything relevant to pointers, arrays and strings should be worked within this directory.

- `/structs` : any content explaining the concept `struct` should be in there.

- `/linux_cli` : any content related from basic linux commands to advanced pipelining & redirection of file inputs & outputs should go in there.
