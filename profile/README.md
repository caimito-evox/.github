```console
sudo apt install -y git python-is-python3
git clone https://github.com/akhilnarang/scripts; cd scripts; sudo bash setup/android_build_env.sh; cd ..; mkdir Evolution; cd Evolution
repo init -u https://github.com/Evolution-X/manifest -b vic --git-lfs
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

git clone https://github.com/caimito-evox/.github -b vic .repo/local_manifests
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

. build/envsetup.sh; breakfast komodo; m evolution
```