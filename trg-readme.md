# README for TRG Researchers

+ We assume `cuda 11.7` is installed by default.
+ Each step will take 10+ minutes

## Installing pytorch

```bash
conda activate trg-megatron
conda install python=3.9 "numpy<1.20" -y
conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia -y
```

## Installing apex

```bash
conda activate trg-megatron
pip install packaging

pushd ~
git clone https://github.com/NVIDIA/apex
cd apex
pip install -v --disable-pip-version-check --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./
popd
```

## Installing packages for preprocessment

```bash
pip install nltk six
```
