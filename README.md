# Team 8 - HW1 - CycleGAN

## Training CycleGAN
* 我們訓練一個 **summer2winter** 的 CycleGAN
* epochs = 200

![](https://i.imgur.com/KbbaVP3.jpg)


---
## Inference CycleGAN in personal image
* 以下圖片來示範測試成果

    - 右圖為原圖（**summer**）
    - 左圖為結果（**winter**）

1. **TSMC Building Grassland in NTHU**

![](https://i.imgur.com/RU7gf2A.png)
> 草地有冰霜的效果，中間的樹林部分稍微模糊

2. **Baseball Field in NTHU**

![](https://i.imgur.com/QGSgoJP.png)
> 草地極具冰霜效果，樹林也有變成冬季植物

3. **Other landscapes downloaded from online**

![](https://i.imgur.com/oLh8ZrO.png)
> 草地顏色有變灰暗

![](https://i.imgur.com/2TUUTKn.png)
> 植物有附上雪，草地跟道路都有變灰

![](https://i.imgur.com/1YC2X6f.png)
> 河流有稍微結冰，且草地面積變少


---
## Other Color Transfer Method
* Reference: [Super fast color transfer between images](https://github.com/jrosebr1/color_transfer)
* The `color_transfer` package is an OpenCV and Python implementation based (loosely) on [Color Transfer between Images](http://www.thegooch.org/Publications/PDFs/ColorTransfer.pdf) [Reinhard et al., 2001]
* The algorithm itself is extremely efficient (much faster than histogram based methods), requiring only the mean and standard deviation of pixel intensities for each channel in the `L*a*b` color space.
* Requirement Package

    - OpenCV
    - NumPy

* 冬天原圖

![](https://i.imgur.com/BqacPFz.jpg)

* 以下圖片為 **Color Transfer_Summer2Winter**的結果

    - 左圖為原圖（**summer**）
    - 右圖為結果（**winter**）

1. **TSMC Building Grassland in NTHU**

![](https://i.imgur.com/8tgBn8z.png)
> 跟 CycleGAN 相較之下，草地色調偏暗、天空顏色有部分呈淡粉紅色，看起來有點怪，反而沒冬天的感覺

2. **Baseball Field in NTHU**

![](https://i.imgur.com/UKd6DLN.jpg)
> 跟 CycleGAN 相較之下，色調明顯跑掉，呈現的很不自然，完全沒冬天的特色

3. **Other landscapes downloaded from online**

![](https://i.imgur.com/0y28QAu.png)
> 跟 CycleGAN 相較之下，這張轉換得很自然，河流看起來有點結冰、草地呈色偏暗，非常有冬天的特色
> **這張不輸給 CycleGAN 生成的照片結果**

![](https://i.imgur.com/oou1vhO.jpg)
> 跟 CycleGAN 相較之下，色調明顯跑掉，呈現的很不自然，完全沒冬天的特色

![](https://i.imgur.com/YQhFZDD.jpg)
> 跟 CycleGAN 相較之下，色調明顯跑掉，呈現的很不自然，完全沒冬天的特色


### Conclusion
* 使用 CycleGAN

    - 優點：

        - 轉換的圖片呈現冬天的特色
        - 效果比傳統方法佳

    - 缺點：

        - 某些細節景物可能模糊失焦
        - Training 時間過長

* 使用 Super fast color transfer

    - 優點：

        - 生成速度快
        - 不會失焦

    - 缺點：

        - 效果普遍比CycleGAN差
        - 色調易跑掉
        - Source需跟Target圖背景成分雷同，才會有好的轉換效果


---

