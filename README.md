# How to Host a Markdown File with GitHub Pages
This README file describes how to host a resume using Mardown and GitHub Pages. 
These steps will also be related to some general principles of technical writing, as described in Andrew Etter's book _Modern Technical Writing_. A link to purchase this book is in the "More Resources" section below.

## Prerequisites
You should have a resume prepared in Markdown that you would like to host. For those unfamiliar with Markdown, there is a link to a Markdown tutorial in the "More Resources" section below.

## Instructions

### Setting up the GitHub Repository
In order host a file with GitHub Pages, we first need to set up a GitHub Repository in the correct way. These steps are outline below.
1. **Create a new GitHub Repository**   
    From either the homepage or your profile, click the green "New" button to create a new repository.
2. **Name and Initialize the repository**   
    For GitHub pages to properly recognize the repository, it must be named in the following format:   
    `[Username].github.io`   
    Once you have entered a name, ensure the repository is set to Public. Do not add a README or gitignore, as we will only be hosting a single file.   
    Click "Create Repository" to initialize the repository.

### Setting up the Local Repository
We must now set up the repository on our local machine and link it to the GitHub repository.

3. **Create the Desired Directory**   
Create a directory in your desired location, then add your Resume file into the directory. Your resume should be named index.md, as GitHub Pages displays that file as the default.
4. **Initialize the Local Repository**   
If you are unfamiliar with or haven't installed git, there is a tutorial linked in the "More Resources" section below.  
From your bash shell, navigate to your directory and run the command `git init`
5. **Add and Commit Files**   
Run the command `git add .`   
Then run the command `git commit -m 'your message'`  
These two commands will add and commit all the files in your directory to the git repository. In this case, the only file being added should be your resume file titled index.md.
6. **Push Changes to GitHub**   
From your GitHub Repository, copy the URL provided.
Run the command `git remote add origin [URL]`   
Then run the command `git push -u origin master`  
Git will ask for your username and access token. If unfamiliar with creating access tokens, there is a link to more information in the "More Resources" section below.    
These commands will link your local and remote repositories and push the local file to the GitHub repository.

### Setting up GitHub Pages
Now that the repository has been setup, we just have to pick a theme and see the result.

7. **Pick a Theme**   
Click the settings tab in the GitHub Repository, then Pages, then Pick Theme.   
Several theme options will appear to preview. Pick one and choose select theme.   
This will generate a _config.yml file in the repository. GitHub pages uses a tool called Jekyll to generate static sites from markdown files. Jekyll uses this config file to know which theme to apply.
8. **See the Result**   
Click the settings tab in the GitHub Repository, then Pages, then click the link to your published site.   
You can also view the resulting site by typing in the given URL in the address bar. It should be of the form `https://[Username].github.io/`.
![See Result GIF](img/recording.gif)

## More Resources
[_Modern Technical Writing_ by Andrew Etter][Book Link]   
[Markdown Tutorial][Markdown Tutorial Link]   
[Git Tutorial][Git Tutorial Link]   
[Git Access Code Information][Git Access Code Link]   

## Authors and Acknowledgments   
Credit to the developers of the Hacker Jekyll Theme, the repository is linked [here][Hacker Theme Link].   
Special thanks to my group members for editing and reviewing my work.   
* Jishan Arora
* Xing Zhou
* Tanisha Turner
* Adam Donen

## Frequently Asked Questions
* Why use Markdown?   
    * Markdown has many useful qualities that make it popular among developers. For one, it is very universal and easy to use. Markdown is free and can be used in any OS or text editor. It is also compatible with many different tools, such as GitHub Pages and Jekyll, which is why I have used it here.
* Why use GitHub Pages?
    * GitHub pages is very easy to use and useful when creating static webpages, like the one in this guide. It allows the user to skip having to worry about interacting with or hosting their own server and lets them update their site in real-time. It is free to use and makes use of tools like Jekyll to automatically build out the site for the user with only a markdown or HTML file as input.
* Why can't I see anything at the URL?
    * One possibility is that your repository is not named correctly. It is important that the name of the repository follows the format of `[Username].github.io` so that GitHub recognizes that it is supposed to be a GitHub Pages repository.
* Can I change the theme for my GitHub Pages Site?
    * Yes, the theme can be changed from the same location as where you first selected it. Just go to Settings, then Pages, then Change Theme. Some previews will display and you can select whichever them you would like.



[Book Link]: https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS
[Markdown Tutorial Link]: https://www.markdowntutorial.com/
[Git Tutorial Link]: https://www.w3schools.com/git/
[Git Access Code Link]: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
[Hacker Theme Link]: https://github.com/pages-themes/hacker

