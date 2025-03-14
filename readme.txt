sudo rm -rf /usr/local/go

# Download and install Go 1.22.2 for ARM64
wget https://go.dev/dl/go1.22.2.linux-arm64.tar.gz
sudo tar -C /usr/local -xzf go1.22.2.linux-arm64.tar.gz

# Add Go to PATH if not already added
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
source /home/ec2-user/.bashrc

# Verify installation
go version



go mod tidy

sudo yum install golang -y


$ redis-cli --cluster call clustercfg.test-redis-3az-3s-2r.yoh70z.usw2.cache.amazonaws.com:6379 flushall