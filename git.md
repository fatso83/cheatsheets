# Ikke la git lokalt oppdage endringer i de angitte (innsjekkede) filene
alias g_unchanged='git update-index --assume-unchanged'

# List opp alle grener som inneholder en gitt commit
git branch --contains 284db0e

# Vis de commitene som ikke finnes i den ene eller andre grenen
git log --graph --left-right --cherry-pick --oneline master...modernizr-extensions
> 284db0e Moved feature detection and modernizr extensions from FrameworkApp into this project (Application.js).
> 5684416 Will now add a class <C2><AB>no-animations<C2><BB> to the module if the new method <C2><AB>shouldUseAnimations()

# Vis committene som kan finnes fra karma-runner, men ikke i internal
git rev-list karma-runner ^internal |xargs -n1 git  --no-pager log -n1 
 git push --delete origin karma-runner 
Note however that formally, the format is:

# Lag ny remote branch av eksisterende branch
git push <remote-name> <local-branch-name>:<remote-branch-name>

git push -u origin my-new-branch
git push origin --delete issue-4 

Vis historikk fra committen du er på og fremover i tid til f.eks. mater
 git log --reverse --ancestry-path a3194dc^..master

# Vise navnet på branch
git symbolic-ref --short HEAD

# Force update of remote branch (dangereux!)
git push origin master --force
#Eller kortversjon 
git push --force


# Søk etter filnavn i historikken
git log --all -- **/thefile.*
git log --all -- /the/path/name.txt
