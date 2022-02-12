# test
testing this out
ssh-keygen -o -a 102 -t ed25519 -f ~/.ssh/id_ed25519_github -C "amihailovich@netflix.com/Device"
cat <<EOF >> ~/.ssh/config    # append the following to ~/.ssh/config

# Github
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_ed25519_github

EOF
git config --global user.email "amihailovich@netflix.com"
git config --global user.name "Ally Mihailovich"
