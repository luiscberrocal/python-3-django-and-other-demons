#Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

I you want to learn more about git I recommend [Pro Git](https://git-scm.com/book/en/v2) by Scott Chacon and Ben Straub.

##Activate git flow

SourceTree offers a way to manage branches in a coherent way. I won't detail on what git flow does.

I prefer to use a v in fron of my version tags. So I adde a v as the image shows.

![Activate git flow 1](./images/image054.png "Activate git flow 1")

##Existing Project

Already have a Git repository on your computer? Let's push it up to Bitbucket.

```
$ cd /Users/luiscberrocal/PycharmProjects/wildbills_project

$ git remote add origin git@bitbucket.org:luiscberrocal/wildbills.git

$ git push -u origin --all # pushes up the repo and its refs for the first time
```

![Existing Project 1](./images/image055.png "Existing Project 1")

![Existing Project 2](./images/image056.png "Existing Project 2")


##Troubleshooting problems with GIT

Some times you have trouble making commits. You might need to make git more verbose in order to tell you what is wrong.

```

GIT_CURL_VERBOSE=1 GIT_TRACE=1 git pull origin master

```