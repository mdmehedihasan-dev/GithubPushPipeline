Step 1: ENTER into the project root folder. 

Step 2: Open Git Bash in VS Code

Step 3: Open your .bashrc file
            nano ~/.bashrc

Step 4: Add the shortcut function

        gpush() {
                    if [ -z "$1" ]; then
                        echo "Please provide a commit message."
                        echo "Usage: gpush \"your commit message\""
                        return 1
                    fi

                    git add -A
                    git commit -m "$*"
                    git push
                }

Step 4: Save and reload Bash

        CTRL + O → Enter → save
        CTRL + X → exit
    in the terminal:
        source ~/.bashrc

Step 5: Use your new command
        gpush "commit message"

