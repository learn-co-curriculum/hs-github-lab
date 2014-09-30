---
  tags: git, kids, github 
  languages: git
  level: 1
  type: lab
---

## Github Workshop

The goal of this workshop is to add the code that we created in the last lab to [Github](https://github.com/). We use Github to store all of our code and share it with others. 

### Setting up your project on Github

* First let's set up a remote repository on Github. Go to https://github.com, and click the `+` located in the top right corner and select "new repository". 

* Fill out information about your new repository. It's a good idea to keep your repository name consistent with the directory on your computer. In this case you should name it "git_practice". 

* The description is optional, but you can fill out with something like "This is my first repository!!!".

* Chose to make your repositories public. This allows other developers to see your work and lets you create a nice history that you can potentially show off when you are applying for an internship or job. (You also have to pay for private repositories, so that's another reason to keep it public.) 

* Now click `Create Repository`.

* You should see something that starts with `git@github.com...` That's the address for our project on Github. We need to set the local version of our project to point to that `remote` address so we can upload our code to github. Copy that SSH address, go to your terminal, make sure you are in your `git_practice` directory, and enter this command (using your personal `git@github` repositories address):

`git remote add origin git@github.com:<your github username>/git_practice.git`

* Now you are ready to push up your code to Github with this command: 

`git push -u origin master`

* This is the only time we'll enter this exact command, because it's the first time we're pushing our code to the server for this particular project. `push` is saying, go on code, get on up there. The `-u` means "upstream", which is just saying to go up to the github repository. If you get a message prompting you to type in yes/no, type in yes. After this you can push code up to this same repository with just `git push`.

* Refresh the page on your github repository and check out the files you just added. Great job!