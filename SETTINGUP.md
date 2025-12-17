**VS Code**
First download and install Visual Studio Code:
https://code.visualstudio.com/


**Git & GitHub**
The below contains instructions to download Git and use it to remotely access GitHub files.  


**Install Git:**
1. If on Windows:  
Download and install Git: https://git-scm.com/install/windows 
Leave everything as default.  
Restart laptop.  
Type git --version in laptop terminal:  
If installed correctly, you should get output similar to below: 

 

If on Mac:  
Type git --version in terminal. [E.g., VS code] 
When you get pop up, click install and go through any necessary steps.  
Type git --version in terminal to verify installation.  

 

**Sign up to GitHub:** 
Ensure you have a GitHub account:  
https://github.com/ 
Take a note of the email you use to sign up: 
'Can view at: 
https://github.com/settings/emails 

 

**Link Git & GitHub**
[Use terminal, such as VS code terminal] 
Follow instructions exactly: 
1. Configure username and email: 
Replace your name with your name. E.g.,"Ben Newton" 
git config --global user.name "Your Name" 
Paste the above into console, change name, then press enter.  

2. Replace email with the email you used for github: 
git config --global user.email yourname@example.com 
Change default branch to main: 
git config --global init.defaultBranch main 
Copy and paste following to stop branch issues: 
git config --global pull.rebase false 
 

Verify username and email: 
git config --get user.name 
git config --get user.email 
 

For macOS Users ONLY 
In order to prevent some default Mac behaviour that we don't want:  
Copy and paste each of the following: 
echo .DS_Store >> ~/.gitignore_global 
git config --global core.excludesfile ~/.gitignore_global 
 

Step 2.3: Create an SSH key 
Check for prior SSH keys: 
ls ~/.ssh/id_ed25519.pub 
If no prior SSH key: 
ssh-keygen -t ed25519 
Press enter 3 times **don't type anything**. Leave save location, password blank. 

 

Link your SSH key with GitHub 
Paste below to console: 
cat ~/.ssh/id_ed25519.pub 
 

Highlight and copy the entire output from the command. If you followed the instructions above, the output will likely begin with ssh-ed25519 and end with your username@hostname. 

Paste to GitHub SSH keys area [new SSH key, name computer as you like, so that you can identify computer]: 

Paste key in the box provided: 
https://github.com/settings/keys 

All finished.  

 

**Test Link:**
1. Create a new GitHub repository [+ sign up GitHub]
Add a readme
2. Copy SSH link:  
In VS code terminal type git clone [your SSH link] 
 If prompted type yes 

Add an index.html file to the cloned folder:  
Copy and paste the following html code: 


<!DOCTYPE html> 

<html> 

    <head> 

        <title>Some website</title> 

    </head> 

    <body> 

        <h1>My title</h1> 

    </body> 

</html> 

Ensure you are in downloaded folder [can use CD > folder name if not], or just open folder directly.  

Now use:  
git add * 
git commit -m 'first folder' 
git push 
Your files should now appear in GitHub repository.  

Put your website online [Setting pages, change branch to main, wait several minutes]: 

 

 

 