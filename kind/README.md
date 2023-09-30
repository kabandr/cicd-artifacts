# Install Kind

```
[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.20.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
```

# Install Kubectl

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
mkdir -p ~/.local/bin
mv ./kubectl ~/.local/bin/kubectl
```

# Check Kubectl version

```
kubectl version --client --output=yaml
```

# Create Kind Cluster

```
kind create cluster --name cluster-name --config cluster-config.yml
```

# Delete Kind Cluster

```
kind delete cluster --name cluster-name        
```
