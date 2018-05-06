# vscode-training
# connect to linux virtual machine in VSCode
  * on host machine, launch VS Code and install extension 'Remote VSCode'
  * on guest virtual machine, enter in terminal
    - sudo wget -O /usr/local/bin/rmate https://raw.github.com/aurora/rmate/master/rmate
    - sudo chmod a+x /usr/local/bin/rmate
  * on host machine, in VS Code, press F1 and enter 'Remote: Start Server'
  * in VS Code's integrated terminal, enter
    - ssh -R 52698:localhost:52698 username@ip_address
  * to open a file, enter in terminal
    - rmate filename.ext ( 'rmate package.json' )
  * to edit 'Remote VSCode' settings
    - open 'User Settings' (File > Preferences > Settings)
    - search for 'remote'
# share app in local dev machine to public using localtunnel
 * to install localtunnel, type in terminal
  - npm install localtunnel
 * edit package.json's scripts section
  - ( 'localtunnel': 'lt --port 3000 --subdomain your_subdomain_here' )
