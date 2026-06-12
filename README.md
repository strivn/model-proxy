# unitalk-proxy

A small **proxy repository** that re-hosts third-party ML model artifacts as
GitHub Release assets, so they can be downloaded reliably and programmatically
instead of from upstream Google Drive / external links that are rate-limited or
unstable.

This repo trains and owns nothing. Every artifact keeps its original upstream
license — see [ATTRIBUTION.md](ATTRIBUTION.md).

## Available artifacts

| Release | Asset | Model | Upstream | License |
|---------|-------|-------|----------|---------|
| [`v0.0.1`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.1) | `UniTalk_TalkNet.model` | TalkNet ASD | [TalkNet-ASD](https://github.com/TaoRuijie/TalkNet-ASD) | MIT |
| [`v0.0.2`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.2) | `dinov2small.zip` | DINOv2 ViT-S/14 | [dinov2](https://github.com/facebookresearch/dinov2) | Apache-2.0 |
| [`v0.0.3`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.3) | `dinov2-base.zip` | DINOv2 ViT-B/14 | [dinov2](https://github.com/facebookresearch/dinov2) | Apache-2.0 |
| [`osnet-msmt17-v1`](https://github.com/strivn/unitalk-proxy/releases/tag/osnet-msmt17-v1) | `osnet-msmt17.zip` | OSNet ReID ×6 (MSMT17) | [deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid) | MIT |

## Download

```bash
# whole archive
gh release download osnet-msmt17-v1 --repo strivn/unitalk-proxy --pattern 'osnet-msmt17.zip'

# or a single asset by URL
curl -L -o osnet-msmt17.zip \
  https://github.com/strivn/unitalk-proxy/releases/download/osnet-msmt17-v1/osnet-msmt17.zip
```

Verify integrity against `SHA256SUMS.txt` (attached to releases that ship it):

```bash
shasum -a 256 -c SHA256SUMS.txt
```

## License

Repository content: [MIT](LICENSE). Proxied model artifacts retain their
upstream licenses — see [ATTRIBUTION.md](ATTRIBUTION.md).
