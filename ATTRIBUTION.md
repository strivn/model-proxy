# Attribution & Third-Party Licenses

This repository (`unitalk-proxy`) does not train or own any model weights. It
**re-hosts (proxies) third-party model artifacts** as GitHub Release assets so
they can be downloaded reliably and programmatically, instead of from upstream
Google Drive / external links that are rate-limited or unstable.

Every released artifact remains the property of its original authors and is
redistributed, unmodified, under its **original upstream license**. This
repository's own [LICENSE](LICENSE) (MIT) applies only to the repository's own
content (scripts, docs, packaging), **not** to the proxied artifacts.

## Released artifacts

| Release | Asset | Upstream model | Source repository | Upstream license |
|---------|-------|----------------|-------------------|------------------|
| [`v0.0.1`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.1) | `UniTalk_TalkNet.model` | TalkNet (audio-visual active speaker detection) | [TaoRuijie/TalkNet-ASD](https://github.com/TaoRuijie/TalkNet-ASD) | MIT (© Ruijie Tao) |
| [`v0.0.2`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.2) | `dinov2small.zip` | DINOv2 ViT-S/14 | [facebookresearch/dinov2](https://github.com/facebookresearch/dinov2) | Apache-2.0 (© Meta Platforms, Inc.) |
| [`v0.0.3`](https://github.com/strivn/unitalk-proxy/releases/tag/v0.0.3) | `dinov2-base.zip` | DINOv2 ViT-B/14 | [facebookresearch/dinov2](https://github.com/facebookresearch/dinov2) | Apache-2.0 (© Meta Platforms, Inc.) |
| [`osnet-msmt17-v1`](https://github.com/strivn/unitalk-proxy/releases/tag/osnet-msmt17-v1) | `osnet-msmt17.zip` (6× `.pth`) | OSNet person-ReID (x0.25–x1.0, IBN, AIN), MSMT17 | [KaiyangZhou/deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid) | MIT (© Kaiyang Zhou) |

## Notes per source

### TalkNet-ASD (`v0.0.1`)
- Code: [TaoRuijie/TalkNet-ASD](https://github.com/TaoRuijie/TalkNet-ASD) — MIT License.
- Paper: R. Tao et al., *Is Someone Speaking? Exploring Long-term Temporal
  Features for Audio-visual Active Speaker Detection.* ACM MM 2021.
- This checkpoint is associated with the **UniTalk** dataset/benchmark
  ([plnguyen2908/UniTalk-ASD-code](https://github.com/plnguyen2908/UniTalk-ASD-code),
  [arXiv:2505.21954](https://arxiv.org/abs/2505.21954)). The UniTalk code
  repository declares **no explicit license** at time of writing; consult the
  upstream repository before redistribution or commercial use of derived work.

### DINOv2 (`v0.0.2`, `v0.0.3`)
- Source: [facebookresearch/dinov2](https://github.com/facebookresearch/dinov2) — Apache License 2.0.
- Paper: M. Oquab et al., *DINOv2: Learning Robust Visual Features without
  Supervision.* TMLR 2024. [arXiv:2304.07193](https://arxiv.org/abs/2304.07193)

### OSNet / deep-person-reid (`osnet-msmt17-v1`)
- Source: [KaiyangZhou/deep-person-reid](https://github.com/KaiyangZhou/deep-person-reid) — MIT License (© Kaiyang Zhou). Weights from the project [model zoo](https://kaiyangzhou.github.io/deep-person-reid/MODEL_ZOO.html), originally on Google Drive.
- Papers: K. Zhou et al., *Omni-Scale Feature Learning for Person
  Re-Identification* (ICCV 2019, [arXiv:1905.00953](https://arxiv.org/abs/1905.00953));
  *Learning Generalisable Omni-Scale Representations for Person
  Re-Identification* (TPAMI 2021, [arXiv:1910.06827](https://arxiv.org/abs/1910.06827), OSNet-AIN).
- Per-file original Google Drive links are listed in the
  [`osnet-msmt17-v1` release notes](https://github.com/strivn/unitalk-proxy/releases/tag/osnet-msmt17-v1).

## Removal

If you are a rights holder and want an artifact removed, open an issue on this
repository.
