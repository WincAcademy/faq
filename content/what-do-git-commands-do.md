+++
title = "What do git commands do?"
extra.tags = [ "git" ]
created = "2021-03-10T12:38"
+++

# What do git commands do?

First, make sure you've read: [what is git?](@/what-is-git.md). Now that you
know what git is for conceptually -- what are each of the commands for?

Think of git as an assistant that keeps track of your things for you, where
*things* are your files. One thing is very important: this assistant doesn't do
anything you don't ask them to do. Treat them like the robot that they are:

- They don't keep track of files that you haven't asked them to keep track
  of;
- They don't save changes unless you ask them to;
- They don't revert changes unless you ask them to;
- They don't communicate changes you told them about to other assistants unless
  you ask them to.

That's what all the commands are for!

## Git Init

- Command

```bash
git init
```

- Real Meaning

Initialize a git repository.

- Analogy

Hire an assistant. They have a lot of skills but they haven't done anything
yet. They are just sitting there waiting for you to give them instructions.

## Git Add

### Command

```bash
git add example_file.txt
```

### Real Meaning

Stage one or multiple files.

### Analogy

Ask the assistant to put some files on their desk.

## Git Commit

### Command

```bash
git commit -m "An example commit message"
```

### Real Meaning

Commit some changes.

### Analogy

Ask the assistant to create a record of the state of all the files that are
currently on their desk *and all the files that haven't changed* together. This
snapshot will be added to a list of snapshots the assistant holds on to,
together with the commit message (here: "An example commit message").

## Git Remote Add

### Command

```bash
git remote add origin https://github.com/example_user/example_repository.git
```

### Real Meaning

Add a remote named `origin` located at
`https://github.com/example_user/example_repository.git` to the list of
remotes.

### Analogy

Tell the assistant about *another assistant of yours* that they should prepare
to communicate with. The assistant takes note of this on a list and does
nothing else yet.

## Git Push

### Command

```bash
# The first time you need to tell git where you want to push to
# git push --set-upstream <name_of_the_remote> <name_of_the_local_branch>
git push --set-upstream origin master

# Afterwards you can just run the command without the extra info attached
git push
```

### Real Meaning

Push current branch to the linked upstream branch. 

### Analogy

Ask the assistant to send their list of all the snapshots to the other
assistant you told them about earlier with `git remote add`. After doing this,
both assistants will have the same files and administration.
