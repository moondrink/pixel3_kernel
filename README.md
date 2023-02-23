aosp：android-10.0.0_r1

kernel: android-msm-crosshatch-4.9-android10

pixe3 android10内核，解决了触屏、wifi、audio等失灵的问题
主要参考https://www.akr-developers.com/d/526-pixel3-aosp/3

参考https://zhuanlan.zhihu.com/p/581604051, 从boot.img解出boot.img-ramdisk.cpio放到kernel根目录，这样就能不依赖aosp单独进行boot.img的编译了

如果不想从kernel编译出boot，则不需要对build.config.common继续修改以及去除build.sh中对于VENDOR_RAMDISK_BINARY的拷贝。
