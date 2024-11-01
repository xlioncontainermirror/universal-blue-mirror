# universal-blue-mirror

**Unofficial** mirror of Universal Blue, mirror to Docker Hub.

## Get Started

### Rebase

**First**, choose whatever text editor you like.

**Second**, copy and paste following command:

```bash
rpm-ostree rebase ostree-unverified-image:registry:registry.hub.docker.com/xlioncontainermirror/
```

**Third**, [middle click me](./matrixs) to browse images you want, copy and paste folder name

**Fourth**, copy and paste following command:

```bash
:latest
```

At the end, you will get the command like this:


```bash
rpm-ostree rebase ostree-unverified-image:registry:registry.hub.docker.com/xlioncontainermirror/bluefin-dx-stable:latest
```

Copy and paste to terminal and run it. After done, reboot.

### Rebase to verified

Run same command but replace `ostree-unverified-image` to `ostree-image-signed`.

## How this repo works

Basicly, it just get the folder list in the [matrixs](./matrixs) folder and add the `Containerfile` in it to workflows, so I don't need to modify `work.yml` after I added another images, and avoid "forgot" problems.

Before start, the workflow will verify the cosign public key before proceed, so your only risk is me, ~~trust me bro~~.