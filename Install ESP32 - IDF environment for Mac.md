# Install ESP32 - IDF environment for Mac
- Install Xcode

- Install XCode command line tools: xcode-select --install

- Install HomeBrew: /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

- sudo easy_install pip

- pip install --user pyserial

- brew install cmake ninja

- brew install ccache

- Download https://dl.espressif.com/dl/xtensa-esp32-elf-osx-1.22.0-80-g6c4433a-5.2.0.tar.gz into ~/Downloads

- mkdir -p ~/esp

- cd ~/esp

- tar -xzf ~/Downloads/xtensa-esp32-elf-osx-1.22.0-80-g6c4433a-5.2.0.tar.gz

- Open ~/.profile or ~/.bash_profile and add line:
  - export PATH=$HOME/esp/xtensa-esp32-elf/bin:$PATH

- Log off, log in back and check PATH with: printenv PATH

- cd ~/esp

- git clone --recursive https://github.com/espressif/esp-idf.git

- Open/create ~/.profile or ~/.bash_profile and add lines:
  - export IDF_PATH=~/esp/esp-idf
  - export PATH="$IDF_PATH/tools:$PATH"

- Log off, log in back and check with: printenv

- Check Python with (Must be version 2.7.x): python --version

- python -m pip install --user -r $IDF_PATH/requirements.txt

- Install failed python libs (nose, tornado) with python -m pip install --user XXX

- Install Visual Studio Code

- Install Extension C/C++ (vscode-cpptools) (Version greater than 0.22.0)
