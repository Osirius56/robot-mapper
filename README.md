# robot-mapper
## Description
Robot-Mapper est un outil permettant de parser les fichiers RobotFramework.
Il permet de :
 * Décomposer les fichiers de suite et de keywords en objets exportable au format json.
 * Lister tout les Cas de test rédigés dans une arborescence
 * Comptabiliser les nombre de cas de tests par Tag (Couverture de ticket Jira/Xray par exemple)
 * Renommer massivement des cas de test depuis un fichier CSV (sur une nouvelle branche git dédiée)
 


## Aide en ligne
```
usage: robot-mapper.py [-h] -s SUITE [-p PATTERN] [-R] [-o OUTPUT] [-b NEW_GIT_BRANCH] [-X RENAMING_MATRIX] [-m] [-E] [-S] [-l] [--roadmap] [--count-by-tag-pattern COUNT_BY_TAG_PATTERN]

optional arguments:
  -h, --help            show this help message and exit
  -p PATTERN, --pattern PATTERN
                        Define pattern use to filter file to treat (Default '[!_]*.robot').
  -R, --recursive       Recursive mode to treat all pattern find in tree (Default 'False').
  -o OUTPUT, --output OUTPUT
                        Define output main directory for exported data (Default '~/robot-mapper/').
  -b NEW_GIT_BRANCH, --new-git-branch NEW_GIT_BRANCH
                        Define new git branch name to apply new modifications make by robot-mapper.py (Default: robot-mapper)

Mandatory arguments:
  -s SUITE, --suite SUITE
                        Give suite path to treat with robot-mapper.py

Massive treatments:
  -X RENAMING_MATRIX, --renaming-matrix RENAMING_MATRIX
                        Define path of Test Cases Renaming Matrix to use.
  -m, --init-matrix     Initialize Renaming Matrix from testCases labels existing in Test Suite .
  -E, --export-testcases
                        Boolean use to export test cases from test Suites without test Suite link in JSON format (object projection).
  -S, --export-suites   Boolean use to export test cases from test Suites by Test Suite in JSON format (object projection).
  -l, --list-of-test
  --roadmap
  --count-by-tag-pattern COUNT_BY_TAG_PATTERN
```