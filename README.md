## Basalt
For kitti dataset with 100hz imu.

### Source installation
```
git clone --recursive http://120.78.194.68/lokia/basalt.git
cd basalt
./scripts/install_deps.sh
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=RelWithDebInfo
make -j8
```

## Usage

* produce kitti calibration json sample:
~/ws/basalt/scripts/basalt_convert_kitti_calib.py -d ~/data/2011_10_03/2011_10_03_drive_0027_sync

* Vi/VIO set --use-imu 0/1:
~/ws/basalt/build/basalt_vio --dataset-path ~/data/2011_10_03/2011_10_03_drive_0027_sync --cam-calib ~/data/2011_10_03/basalt_calib.json --dataset-type kitti --config-path /usr/etc/basalt/kitti_config.json --show-gui 1 --use-imu 1



