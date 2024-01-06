- Install zsh:
  ```
    sudo apt-get install zsh -y
  ```

- Cài đặt oh-my-zsh: 
  ```
    sudo curl -L http://install.ohmyz.sh | sh
  ```

- Sử dụng zsh làm mặc định:
  ```
    chsh -s $(which zsh)
  ```

- Cài đặt zsh-autosuggestions:
  ```
    git clone git@github.com:zsh-users/zsh-autosuggestions.git ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions

    // chỉnh sửa file ~/.zshrc:
    plugins=(git zsh-autosuggestions)
    source $ZSH/oh-my-zsh.sh
    source ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
  ```