## Suggested Information for Code

### README and master script
All replication archives should have a README (in PDF, text, or a simple formatting language such as Markdown, like this document). The README should provide a sufficient description to understand the structure of the replication archive (directory structure, what is acquired from third parties, what is generated by scripts, how much output to expect). It should document each file or class of files that are included.

We strongly encourage the provision of a master script. The master script should run all programs necessary to provide the outputs, in the right sequence.

In some cases, the master script might also serve as a README (for instance, "README.bash", "README.py", "README.Rmd"), as long as it satisfies all conditions of the README as well (i.e., ample comments).

### Things not to do
-  We strongly discourage writing comments like
```
Run this a first time, generating column 1 of Table 3.
Then comment out line 55, then run a second time, which should
give you column 3 of Table 3.
Then uncomment line 55, change the parameter in line 67 to "5",
and run again to get column 2 of Table 3.
```
(this is only slightly paraphrased from an actual example).
-  Avoid ambiguous or imprecise instructions  like
```
Have superDynare available
```
or
```
Use the outreg55 package
```
(no URL or installation command provided)

### Things to do
-  Write code that can be run without human intervention.
-  Use functions/programs/loops/etc. to iterate through variations of an otherwise identical procedure (but ensure that the purpose of the loop is well described)
-  Identify all requirements to allow somebody to successfully run the code who has NOT been experimenting with the software and code for the past 5 years on the same laptop. This means
  -  what packages need to be installed, from where, which versions
  ```{stata}
  ssc install outreg55, from(https://myurl/to/o)
  ```
  or
  ```{r}
  install.packages(c("dplyr","devtools"))
  library(dplyr)
  library(devtools)
  install_github("myrepo/superols")
  ```