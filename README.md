# Google functions

Here is the syntax for deploying functions using the gcloud commands.

Syntax:
https://source.developers.google.com/projects/{PROJECT_ID}/repos/{REPOSITORY_ID}/revisions/{REVISION_ID}/paths/{PATH} 
or 
https://source.developers.google.com/projects/{PROJECT_ID}/repos/{REPOSITORY_ID}/moveable-aliases/{BRANCH_ID}/paths/{PATH} 
or 
https://source.developers.google.com/projects/{PROJECT_ID}/repos/{REPOSITORY_ID}/fixed-aliases/{TAG_ID}/paths/{PATH}. 

Note that PROJECT_ID, REPOSITORY_ID, REVISION_ID, BRANCH_ID, and TAG_ID can not contain '/'. PATH may contain '/'.

Example:
gcloud functions deploy git-functions \
--source https://source.developers.google.com/projects/black-abode-368706/repos/github_surendrams_functions/revisions/0e98c9e/paths/git-functions/ \
--runtime nodejs16 \
--trigger-http \
--entry-point helloFromGit
