# Stable Swarm UI Docker

Containerizing [Stability AI](https://github.com/Stability-AI)'s [Stable Swarm UI](https://github.com/Stability-AI/StableSwarmUI).

## Running with Docker
0. Clone this repo and cd into it

1. Build your image

```
docker build -t stableswarmui .
```
2. Run your image

```
docker run --rm -it --gpus=all -p 7801:7801 stableswarmui StableSwarmUI.dll $@ --launch_mode none --host "*"
```
3. Use this command to exec into the container's shell for troubleshooting (or curiosity)
```
docker run --rm -it --gpus=all -p 7801:7801 --entrypoint bash stableswarmui
```

## Known Issues

Note that this currently works but the application within isn't loading on Linux.
