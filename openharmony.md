# openharmony notes

install repo tool

```
mkdir openharmony
cd openharmony
wget -O repo https://gitee.com/oschina/repo/raw/fork_flow/repo-py3
sudo mv repo /usr/local/bin/repo
sudo chmod a+x /usr/local/bin/repo
python3 -m pip install -i https://repo.huaweicloud.com/repository/pypi/simple requests
sudo apt-get install git git-lfs
```
download  openharmony source
```
repo init -u https://gitee.com/openharmony-sig/manifest.git -b master --no-repo-verify -m devboard_bearpi_hm.xml 
repo init --config-name
repo sync -c
repo forall -c 'git lfs pull'
```
download build tools
```
bash build/prebuilts_download.sh
```
configure
```
hb set
```
check
```
hb env
[OHOS INFO] root path: /home/koen/src/openharmony
[OHOS INFO] board: bearpi_hm_nano
[OHOS INFO] kernel: liteos_m
[OHOS INFO] product: bearpi_hm_nano
[OHOS INFO] product path: /home/koen/src/openharmony/vendor/bearpi/bearpi_hm_nano
[OHOS INFO] device path: /home/koen/src/openharmony/device/bearpi/bearpi_hm_nano/liteos_m

```
compile
```
hb build
```
burn with openocd

[applications](https://gitee.com/openharmony-sig/applications_sample_bearpi_hm_nano)