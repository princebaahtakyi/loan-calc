# Starting a Python project: uv, Git and GitHub

## Part 1: Create the project with uv

1. Go to the Projects folder
   cd ~/Projects
2. Create the project (use lowercase and hyphens)
   uv init demand-notice
3. Step inside it
   cd demand-notice
4. Check Git's top level is this project, not the home folder
   git rev-parse --show-toplevel
   (If it prints /Users/curlybees, run: git init)
5. Add a library (only what the project needs)
   uv add python-docx
6. Prove it works
   uv run python -c "import docx; print('ready')"

## Part 2: Save it to GitHub

1. On github.com: plus icon, New repository
   - Name: same as the folder (demand-notice)
   - Private; README, .gitignore and licence OFF
   - Copy the web address ending in .git
2. In the Terminal, inside the project:
   git add .
   git commit -m "Start demand-notice with python-docx"
   git remote add origin PASTE-ADDRESS-HERE
   git branch -M main
   git push -u origin main
3. Refresh the GitHub page to see your files

## Later, every time you save work

   git add .
   git commit -m "What I did"
   git push

## Habits

- Run pwd first, always know which project you are in
- rm deletes permanently, check pwd before using it
- Close and reopen the terminal after installing new tools
- One project, one uv init; libraries go in only when needed


cd loan-application
git rev-parse --show-toplevel