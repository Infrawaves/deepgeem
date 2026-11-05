# RELEASE LOG DEEPGEMM

## 2026.11.05 infrawaves/dev/kimi-k3.1-day-0
- Base: sgl-deep-gemm v0.2.3.post2 (b7f3816), the version pinned by sglang kimi-k3.1-day-0
  (python/pyproject.toml, docker/k31-image/build_deepgemm.py). VERSION stays 0.2.3.post2 so the
  sglang pin and build_deepgemm.py version check still match.
- f7f496c: Fix Mega MoE task info slot release ordering (upstream DeepGEMM #441, cherry-picked from 78b6900).
  Fixed upstream in v0.2.5; v0.2.3.post2 does not have it.
- 3a9f036: [SM100] Mega MoE: use 64-bit SF buffer offsets (cherry-picked from 33ea6d2 / b9177ae).
- 512874d: [SM100] Mega MoE: use block_m 64 for decode-sized loads (sgl-project/DeepGEMM#130).
  Same as sglang's docker/k31-image/deepgemm-mega-moe-decode-block-m.patch; do not apply that patch again
  when building from this branch.
