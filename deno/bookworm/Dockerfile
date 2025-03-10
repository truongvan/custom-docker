FROM denoland/deno:debian-2.2.3

LABEL author="truongvan@live.com"

# Install ZSH
RUN <<EOF
apt-get update
apt-get install -y zsh curl
chsh -s /usr/bin/zsh
sh -c "curl -sS https://starship.rs/install.sh | sh -s -- -y"
echo 'eval "$(starship init zsh)"' >> /root/.zshrc
EOF

# Create user and group
RUN <<EOF
groupadd -g 1001 -r code
useradd -d /home/code -g code -l -r -u 1001 code -s /usr/bin/zsh
mkdir -p /home/code/.vscode-server/
mkdir -p /home/code/web/node_modules/
mkdir /deno-dir
chown -R code:code /deno-dir
chown -R code:code /home/code
echo 'eval "$(starship init zsh)"' >> /home/code/.zshrc
EOF
