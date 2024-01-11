Install Agro CLI in MAC Book
# Download the binary
curl -sLO https://github.com/argoproj/argo-workflows/releases/download/v3.2.3/argo-darwin-amd64.gz

# Unzip the software
gunzip argo-darwin-amd64.gz

# Make binary executable
chmod +x argo-darwin-amd64

# Move binary to path
mv ./argo-darwin-amd64 /usr/local/bin/argo

# Test installation using below command
argo version
