# niri-matrix-bridge-k8s

## Creating configmaps

Created config maps from local files for synapse and mautrix

```bash
kubectl create secret generic synapse-signing-key --from-file=signing.key=./niri-matrix.appditto.com.signing.key -n niri-bridge
kubectl create configmap discord-registration --from-file=registration.yaml=./discord/registration.yaml -n niri-bridge
kubectl create configmap discord-config --from-file=config.yaml=./discord/config.yaml -n niri-bridge
```
