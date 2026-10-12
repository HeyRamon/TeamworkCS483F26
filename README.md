# TeamworkCS483F26
In Class Activity 8.1.

# Students must **not** commit directly to `main`.

This is a Git collaboration simulation in which students work in teams on the same project, make changes independently, review each other's work, and integrate their contributions into this shared repository. The goal is not just to learn Git commands, but to experience a realistic collaborative workflow: coordinating tasks, avoiding conflicts, reviewing code, and deciding when changes are ready to merge.

# In-class activity: Collaborating with Git and GitHub

## 1. The project: CS Student Survival Guide

Every student will join a team and contribute to build a **CS Student Survival Guide**. 

Each team creates one contribution, for example:

| Team   | Contribution                 |
| ------ | ---------------------------- |
| Team 1 | Git commands cheat sheet     |
| Team 2 | Debugging tips               |
| Team 3 | Study strategies             |
| Team 4 | Useful programming resources |
| Team 5 | Common programming mistakes  |
| Team 6 | Tips for working in teams    |

Each team should submit its contribution through a **pull request**. At the end, the class has one combined resource in the shared repository.


## 2. Team building

1. The professor will assign you to a group
2. Go around introducing your self and sharing your level of familiarity with Git.
3. Explain each other how have you used Git in the past and what do we mean by "Students must **not** commit directly to `main`." and "Each team should submit its contribution through a **pull request**".
4. Fill out the fist columns of the table on the written ICA.

## 3. Assign team roles

Each student should have a role so that everyone has a responsibility, so select one of the following roles. We will rotate the roles during the activity if time allows.

1\. Team coordinator

Organizes tasks, checks that everyone understands the plan, and helps the team communicate. 

2\. Git workflow lead

Checks branch names, verifies that teammates are working on the correct branches, and helps resolve Git problems. 

3\. Main Reviewer 

Reviews pull requests, checks quality, and verifies that contributions fit the project. 

4\. Contributors (all team members)

Implement the assigned content, commit changes, and push their branches. Peer review and approves pull requests.

Important: these are **coordination roles**, not exclusive permissions. Every student should execute Git commands themselves.



# 4. Activity timeline


## 1. Goal

Your team will collaborate on a shared GitHub repository. Each team will have its own branch, and each student will contribute an individual file to the team's work.

By the end of the activity, you should be able to:

- Clone a repository to your computer.
- Create and switch between branches.
- Create a folder and add files to a project.
- Stage and commit changes.
- Push a branch to GitHub.
- Open and review a pull request.
- Collaborate with teammates without directly overwriting their work.

## 2. Repository structure

The instructor will provide one shared repository. You will organize it into six team folders, with one main branch per team.

For example, the repository could have this structure:

### class-collaboration

Each team branch contains its team's folder and five individual contributions.

`team-1` branch
Contains the `team-1/` folder and its five students' contributions.

```
└── team-1 
    ├── README.md
    ├── student-1.md
    ├── student-2.md
    ├── student-3.md
    ├── student-4.md
    └── student-5.md
```

Each team branch will eventually contain five student files. Every student is responsible for creating and submitting their own file.

*Note: Git branches are independent versions of the repository. A folder created on one branch does not automatically appear on the other branches.*


## 3. Create your team's branch and folder

Each team must create one shared team branch. This branch will serve as the team's main working branch.

Your team branch names must follow this convention:

- `team-1`
- `team-2`
- `team-3`
- `team-4`
- `team-5`
- `team-6`

The repository will have the original `main` branch plus these six team branches.

### Instructions

1. Clone the shared repository to your computer.
2. Check the existing branches.
3. Coordinate with your team to create your team's branch from `main`. Only one team member needs to create the team branch initially.
4. Create a folder named after your team, such as `team-1/`.
5. Add a `README.md` file to the folder introducing your team and listing its members.
6. Commit and push the folder to your team's branch.
7. All team members should fetch the updated branches and switch to their team's branch.

Example commands for the team member creating the branch:

```
git clone REPOSITORY_URL
cd class-collaboration

git switch main
git pull origin main

git switch -c team-1

mkdir team-1
```

Create `team-1/README.md`, then run:

```
git add team-1/
git commit -m "Create team 1 folder"
git push -u origin team-1
```

Other team members can then access the branch:

```
git fetch origin
git switch -c team-1 --track origin/team-1
```

Replace `team-1` with your team's assigned branch name.

## 4. Make your individual contribution

Every student must create their own feature branch based on their team's branch.

For example, if you belong to Team 1, your branch could be named:

`team-1/student-1-contribution`

### Your task

Create one Markdown file inside your team's folder. Your file must include:

- Your name or assigned identifier.
- A useful tip, resource, or lesson related to the team's project.
- A short explanation of your contribution.
- At least one example, where appropriate.

For example:

```
class-collaboration/
└── team-1/
    ├── README.md
    ├── student-1.md
    ├── student-2.md
    ├── student-3.md
    ├── student-4.md
    └── student-5.md
```

### Git workflow for your individual contribution

```
# Make sure you are on your team's branch
git switch team-1
git pull origin team-1

# Create your own feature branch
git switch -c team-1/student-1-contribution

# Create and edit your individual file
# Then stage and commit your changes
git add team-1/student-1.md
git commit -m "Add student 1 contribution"

# Push your feature branch
git push -u origin team-1/student-1-contribution
```

Next, open GitHub and create a pull request.

Important: Your pull request must target `team-1`, not the repository's original `main` branch.

## 5. Review and merge your teammates' contributions

Each student must review at least one teammate's pull request.

The reviewer should check:

- Is the file in the correct team folder?
- Does the contribution follow the instructions?
- Is the content clear and useful?
- Does the change introduce unwanted modifications?

After reviewing, leave feedback and approve the pull request if it meets the requirements. Merge it into the team's branch according to the instructor's instructions.

If changes are requested, the original author should update their feature branch and push again. The same pull request will update automatically.

## 6. Keep your local repository up to date

When a teammate's pull request is merged, the new file becomes part of the team's branch. Before starting another contribution, synchronize your local copy.

```
git switch team-1
git pull origin team-1
```

This step is important because your local repository does not automatically receive changes made by other team members.

## 7. Final deliverables

By the end of class, each team should have:

- [ ] One team branch on GitHub.
- [ ] One team folder containing a README.
- [ ] *N* individual contribution files, where *N* is the number students in the team.
- [ ] Individual feature branches pushed to GitHub.
- [ ] Pull requests targeting the correct team branch.
- [ ] At least one peer review per student.
- [ ] Merged contributions visible on the team's branch.


