# Team 8 - HW1 - CycleGAN

* Teammates

| 學號 | 姓名 |
| :--------: | :--------: | 
| 104070015     | 王妤㚬     | 
| 104011251     | 陳泓仁     | 
| 107065501     | 蘇玫如     | 

---
## Training CycleGAN
* 我們訓練一個 ==**summer2winter**== 的 CycleGAN
* epochs = 200

![](https://i.imgur.com/KbbaVP3.jpg)


---
## Inference CycleGAN in personal image
* 以下圖片來示範測試成果

    - 右圖為原圖（**summer**）
    - 左圖為結果（**winter**）

1. **TSMC Building Grassland in NTHU**

![](https://i.imgur.com/RU7gf2A.png)

2. **Baseball Field in NTHU**

![](https://i.imgur.com/QGSgoJP.png)

3. **Other landscapes downloaded from online**

![](https://i.imgur.com/oLh8ZrO.png)

![](https://i.imgur.com/2TUUTKn.png)

![](https://i.imgur.com/1YC2X6f.png)


---
## Compare with other method
* Reference: [Super fast color transfer between images](https://github.com/cvfx-2019/homework1-color-transfer)
* The `color_transfer` package is an OpenCV and Python implementation based (loosely) on [Color Transfer between Images](http://www.thegooch.org/Publications/PDFs/ColorTransfer.pdf) [Reinhard et al., 2001]
* The algorithm itself is extremely efficient (much faster than histogram based methods), requiring only the mean and standard deviation of pixel intensities for each channel in the `L*a*b` color space.
* Requirement Package

    - OpenCV
    - NumPy

* 冬天原圖

![](https://i.imgur.com/BqacPFz.jpg)

* 以下圖片為 **Color Transfer_Summer2Winter**的結果

1. **TSMC Building Grassland in NTHU**

![](https://i.imgur.com/8tgBn8z.png)

2. **Baseball Field in NTHU**

![](https://i.imgur.com/UKd6DLN.jpg)

3. **Other landscapes downloaded from online**

![](https://i.imgur.com/0y28QAu.png)

![](https://i.imgur.com/oou1vhO.jpg)

![](https://i.imgur.com/YQhFZDD.jpg)


---
