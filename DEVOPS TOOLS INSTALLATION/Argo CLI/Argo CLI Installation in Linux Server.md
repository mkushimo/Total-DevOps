#  Install Agro CLI in Linux Server

## Download the binary
```
curl -sLO https://github.com/argoproj/argo-workflows/releases/download/v3.2.3/argo-linux-amd64.gz
```

## Unzip the software
```
gunzip argo-linux-amd64.gz
```

## Make binary executable
```
chmod +x argo-linux-amd64
```

## Move binary to path
```
mv ./argo-linux-amd64 /usr/local/bin/argo
```

## Test installation using below command
```
argo version
```
