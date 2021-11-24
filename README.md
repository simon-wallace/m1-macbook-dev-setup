# Setup for Software Development on M1 MacBook Pro - Monterey
> Nov 2021 - Simon Wallace

Development environment setup instructions for M1 Macbook Pro running Monterey 12.0.1

All run natively on the Apple silicon for improved performance and battery life.

### 1. Install Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
### 2. Install node and NPM
```
brew install node
```
### 3. Install pipenv 
```
brew install pipenv 
```
### 4. Install ruby (arm64)
```
brew install ruby
```
**Fix cocoapods error on “pod install”:**
* Add path to .zshrc file and restart the terminal

```
$ nano  ~/.zshrc 
$ export PATH=/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/3.0.0/bin:$PATH 
$ source ~/.zshrc
```
(you can find your Homebrew installation directory with ```$(brew --prefix) if needed```)  
* Make sure you are using the correct ruby binary by executing ```$ which ruby``` (should be ```$(brew --prefix)/opt/ruby/bin/ruby```)
* Install CocoaPods 
```
sudo gem install cocoapods
```
* Make sure you are using the correct pod binary by executing ```$ which pod``` (should be $(brew --prefix)/lib/ruby/gems/3.0.0/bin/pod)  
* Make sure ethon is version 0.13.0 or more with ```$ gem info ethon```, otherwise run ```$ sudo gem install ethon```
* Running "pod install" should now work correctly 

### 5. Install Programs
* VS Code (universal)
* Xcode
* Android Studio

### 6. Install Git
```
brew install git
```

*Enjoy the speed!*  






