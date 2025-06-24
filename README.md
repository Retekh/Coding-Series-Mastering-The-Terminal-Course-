# Coding Series | Mastering The Terminal (Mac)

# Episode 1: Creating A Beautiful Environment

## Removing Distractions

Now let's start setting up the environment to be visually pleasing and functional. What I like to do is remove as many distractions as I can. This is true for your computer as well as your surroundings. Try to have a clean and comfortable space free from distractions. On our computer we can hide the doc the menu bar and the desktop files. 

Lets click the apple in the top left corner. Go to system settings. Down to Desktop & Dock. Then check automatically hide & show doc. Under menu bar click the selection by automatically hide and show the menu bar. Click always. Then lets go to the terminal and paste in the command:

### defaults write com.apple.finder CreateDesktop -bool false && killall Finder

This will hide the files on the desktop. It will not delete them. To undo this you can type the command:

### defaults write com.apple.finder CreateDesktop -bool true && killall Finder
                 
Make sure to save these commands.

Now make sure your background is something you like because that’s what will make your setup look great. Go to settings, wallpaper then choose your favorite. 

## Installing Homebrew and ITerm2

Now let's download homebrew. Homebrew is a package manager for mac that will help us organize and download various files. So to download it in the terminal we will enter the command:

### /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

I like to use the iterm2 terminal. It has more functionalities and customizations than the default terminal. So we can type the command: 

### brew install --cask iterm2 

We are installing this with our package manager homebrew. 

## Customizing ITerm2 With Profiles

Now open iterm2 and lets customize it. To me it doesn’t look good or as nearly as good as it can now so lets change that. 

I have a custom profile in this github repository that you can use. Just look over (because you should never trust random people on the internet) and then:

### download the Tutorial-Profile.json file

Click iterm2 in the menubar at the top of the screen, then settings. Go to profiles and by other actions then you can import the json. Name it whatever you want then click other actions and set it to default.  

## Customizing ITerm2 With Starship

Now let's download starship. With it we can add modules to customize our terminal prompt.

First well type the command:

### brew install starship

Then let's enter our rc file to configure it. Run:

### vim ~/.zshrc

Then scroll to the end of the file and type in:

### eval "$(starship init zsh)" (if you have oh_my_zsh it needs to be after it, at the very end)

Now type the command:

### source ~/.zshrc 

This will apply the changes or you can restart the terminal. Now lets create a .toml file which is where we will add in our starship customizations. Type the command:

### mkdir -p ~/.config && touch ~/.config/starship.toml

Then you can copy this basic customization template thats in this repo:

### curl -o ~/.config/starship.toml https://raw.githubusercontent.com/Retekh/Coding-Series-Mastering-The-Terminal-Course-/main/starship.toml

And that’s it. Now your workspace looks clean, efficient and beautiful.
