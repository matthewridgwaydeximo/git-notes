# git-notes

## Man command

The ```man``` command is used to display the manual pages for Unix commands and programs. It provides detailed documentation about the usage, options, and examples for a specified command. 

```
man man
```

## Concept of Git as a Distributed Version Control

### Distributed vs. Centralized Version Control

**Distributed Version Control (Git):**
- **Repository Copies:** Each developer has a full copy of the entire repository, including the project's complete history.
- **No Single Point of Failure:** Since each developer has a complete copy of the repository, the system is more resilient. If a central server fails, any copy can be used to restore it.
- **Offline Capabilities:** Developers can work offline, committing changes locally and later synchronizing with the central repository when back online.
- **Branching and Merging:** Git makes branching and merging simpler and more powerful, facilitating better workflow and collaboration.

**Centralized Version Control (e.g., SVN):**
- **Single Central Repository:** There is a single central repository that all developers interact with.
- **Single Point of Failure:** If the central server goes down, no one can commit changes or access the version history until the server is restored.
- **Limited Offline Capabilities:** Developers typically need to be online to commit changes and access the repository's history.
- **Branching and Merging:** Branching and merging are generally more complex and can be less efficient compared to distributed systems like Git.

### Git Workflow

**1. Untracked:**
- Files that are not tracked by Git and are not in the staging area.
- To track a file, use:
  ```sh
  git add <filename>
  ```

**2. Tracked:**
- Files that are already added to Git and are being tracked for changes.
- Tracked files can be in three states:
  - **Modified:** Changes have been made to the file but not yet staged.
  - **Staged:** Changes have been marked to be included in the next commit.
  - **Committed:** Changes are saved in the local repository.

**Git Workflow Steps:**

1. **Add Untracked Files:**
   - To start tracking a new file, use:
     ```sh
     git add <filename>
     ```
   - This moves the file from the untracked state to the staged state.

2. **Stage Modified Files:**
   - To stage changes in tracked files, use:
     ```sh
     git add <filename>
     ```
   - This stages the changes, preparing them to be committed.

3. **Commit Changes:**
   - To commit the staged changes to the local repository, use:
     ```sh
     git commit -m "Commit message"
     ```
   - This moves the changes from the staged state to the committed state.

4. **Synchronize with Remote Repository:**
   - To push local commits to a remote repository, use:
     ```sh
     git push origin <branch-name>
     ```
   - To pull changes from a remote repository, use:
     ```sh
     git pull origin <branch-name>
     ```
