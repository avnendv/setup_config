1. Cài đặt java

```
  sudo apt install default-jdk
```

2. Install required packages

```
  sudo apt install clang cmake ninja-build pkg-config libgtk-3-dev liblzma-dev
```

3. Cài đặt flutter

```
  mkdir -p $HOME/Downloads && cd "$_"
  wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.7.9-stable.tar.xz
  mkdir -p $HOME/Applications && cd "$_"
  tar xfv $HOME/Downloads/$(ls -d $HOME/Downloads/flutter*.tar.xz | xargs basename)
  export PATH="$HOME/Applications/flutter/bin:$PATH" // add to .bashrc or .zshrc
  flutter doctor
```

4. Install Android Studio

```
  mkdir -p $HOME/Downloads && cd "$_"
  wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2020.3.1.26/android-studio-2020.3.1.26-linux.tar.gz
  mkdir -p $HOME/Applications && cd "$_"
  tar xfv $(ls -1t $HOME/Downloads/android-studio-* | head -n1)
  flutter config --android-studio-dir $HOME/Applications/android-studio/
  alias android-studio=$HOME/Applications/android-studio/bin/studio.sh // add to .bashrc or .zshrc
  android-studio
```

5. Agree to Android Licenses

```
  flutter doctor --android-licenses
```
