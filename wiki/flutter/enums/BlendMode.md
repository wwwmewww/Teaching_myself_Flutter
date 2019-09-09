# BlendMode

0. BlendMode.clear<br>*删除源和目标图像，不留任何内容。<br>这与 Porter-Duff 的 clear 相对应。*
1. BlendMode.src<br>*删除目标图像，只绘制源图像<br>从概念上讲，首先清除目标，然后绘制源图像<br>这与 Porter-Duff 的 Copy 相对应*
2. BlendMode.dst<br>*删除源图像，只绘制目标图像<br>从概念上讲，源图像被丢弃，而目标保持不变<br>这与 Porter-Duff 的 Destination 相对应*
3. BlendMode.srcOver<br>*在目标图像上合成源图像<br>这是默认值。它代表了最直观的情况，即图形绘制在下面的上面，透明区域显示目标层<br>这与 Porter-Duff 的 Source over Destination 相对应，也称为 Painter 算法*
4. BlendMode.dstOver<br>*在目标图像下合成源图像<br>这与 srcOver 相反<br>这与 Porter-Duff 的 Destination over Source 相对应<br>当源图像应在目标图像之前绘制，但不能绘制时很有用*
5. BlendMode.srcIn<br>*显示源图像，但仅显示两个图像重叠的位置。目标图像不被渲染，只被视为一个遮罩。目标的颜色通道将被忽略，只有不透明度具有效果<br>要显示目标图像，请考虑dstIn<br>要反转遮罩的语义（只显示缺少目标的源，而不是显示目标所在的源），请考虑 srcOut<br>这与 Porter-Duff 的 Source in Destination 相对应*
6. BlendMode.dstIn<br>*显示目标图像，但仅显示两个图像的重叠位置。源图像不被渲染，它只被视为一个遮罩。源的颜色通道将被忽略，只有不透明度具有效果<br>要显示源图像，请考虑 srcIn<br>要反转遮罩语义(只显示目标所在的源，而不是不存在的源)，请考虑 dstOut<br>这与 Porter-Duff 的 Destination in Source 相对应*
7. BlendMode.srcOut<br>*显示源图像，但仅在两个图像不重叠的位置显示。目标图像不被渲染，只被视为一个遮罩。目标的颜色通道将被忽略，只有不透明度具有效果<br>要显示目标图像，请考虑 dstOut<br>要反转遮罩的语义(仅显示目标所在的源，而不是不存在的源),请考虑 srcIn<br>这与 Porter-Duff 的 Source out Destination 相对应*
8. BlendMode.dstOut<br>*显示目标图像，但仅在两个图像不重叠的位置显示。源图像不被渲染，它只被视为一个遮罩。源的颜色通道将被忽略，只有不透明度有效果。<br>要显示源图像，请考虑 srcOut<br>要反转遮罩的语义(只显示源所在的目标，而不显示源所在的目标)<br>这与 Porter-Duff 的 Destination out Source 相对应*
9. BlendMode.srcATop<br>*在目标图像上合成源图像，但仅在它与目标重叠的位置合成<br>这与 Porter-Duff 的 Source atop Destination 相对应<br>这基本上是 srcOver操作，但输出的不透明度通道被设置为目标图像的不透明度通道，而不是两个图像的不透明度通道的组合<br>有关目标在上面而不是源的变体，请参见 dstATop*
10. BlendMode.dstATop<br>*在源图像上合成目标图像，但仅在它与源图像重叠的位置<br>这与 Porter-Duff 的 Destination atop Source 相对应<br>这基本上是 dstOver 操作，但输出的不透明度通道被设置为源图像的不透明度通道，而不是两个图像的不透明度通道的组合<br>有关源在上面而不是目标的变体，参见 srcATop*
11. BlendMode.xor<br>*对源和目标图像应用位XOR运算符。这使得它们重叠的地方保持了透明度<br>这与 Porter-Duff 的 Source xor Destination 相对应*
12. BlendMode.plus<br>*对源图像和目标图像的组件进行求和<br>其中一个图像的像素中的透明度会降低该图像对相应输出像素的贡献，就好像该图像中该像素的颜色较暗一样<br>这与 Porter-Duff 的 Source plus Destination 相对应*
13. BlendMode.modulate<br>*将源图像和目标图像的颜色分量相乘<br>这只能导致相同或较暗的颜色(乘以白色,1.0,结果不变；乘以黑色,0.0,结果为黑色)<br>当合成两个不透明的图像时，这与在投影仪上重叠两个透明胶片具有相似的效果<br>有关于也将alpha通道相乘的变体，请考虑 multiply*
14. BlendMode.screen<br>*将源图像和目标图像的分量的倒数相乘，然后将结果倒数<br>反转组件意味着将完全饱和的通道（不透明白色）视为 0.0，通常将 0.0（黑色、透明）的值视为1.0<br>这基本上与 modulate 相同，但在乘法前反转颜色值，在渲染前反转结果<br>这只能产生相同或较浅的颜色（乘以黑色,1.0,结果不变；乘以白色,0.0,结果为白色）。同样，在alpha通道中，它只能产生更不透明的颜色<br>这与两台投影仪同时在同一屏幕上显示图像的效果相似*
15. BlendMode.overlay<br>*将源图像和目标图像的组件在调整后相乘，以利于目标<br>具体来说，如果目标值较小，则将其与源值相乘，而源值较小，则将源值的逆值与目标值的逆值相乘，然后反转结果<br>反转组件意味着将完全饱和的通道（不透明白色）视为 0.0，通常将 0.0（黑色、透明）的值视为 1.0*
16. BlendMode.darken<br>*通过从每个颜色通道中选择最小值来合成源图像和目标图像<br>输出图像的不透明度计算方法与 srcOver 相同*
17. BlendMode.lighten<br>*通过从每个颜色通道中选择最高值来合成源图像和目标图像<br>输出图像的不透明度计算方法与 srcOver 相同*
18. BlendMode.colorDodge<br>*将目标除以源的倒数<br>反转组件意味着完全饱和的通道(不透明的白色)被视为 0.0，通常将 0.0 的值(黑色，透明) 视为 1.0*
19. BlendMode.colorBurn<br>*将目标的倒数除以源，然后在倒数得出结果<br>反转组件意味着完全饱和的通道(不透明的白色)被视为 0.0，通常将 0.0 的值(黑色，透明) 视为 1.0*
20. BlendMode.hardLight<br>*将源图像和目标图像的组件在调整后相乘，以利于源图像<br>具体来说，如果源值较小，则将其与目标值相乘，而目标值较小，则将目标值的逆值与源值的逆值相乘，然后反转结果<br>反转组件意味着完全饱和的通道(不透明的白色)被视为 0.0，通常将 0.0 的值(黑色，透明) 视为 1.0*
21. BlendMode.softLight<br>*对低于 0.5 的源值使用 colordodge，对高于 0.5 的源值使用 colorburn<br>效果与 overlay相似，但更柔和*
22. BlendMode.difference<br>*从每个通道的较大值中减去较小的值<br>合成黑色没有效果；合成白色反转其它图像的颜色<br>输出图像的不透明度计算方法与 srcOver 相同<br>效果与 exclusion 相似，但更严重*
23. BlendMode.exclusion<br>*从两个图像的和中减去两个图像的乘积的两倍<br>合成黑色没有效果；合成白色反转其它图像的颜色<br>输出图像的不透明度计算方法与 srcOver 相同<br>效果与 difference 相似，但更柔和*
24. BlendMode.multiply<br>*将源图像和目标图像的组件相乘，包括alpha通道<br>这只能导致相同或较暗的颜色(乘以白色,1.0,结果不变；乘以黑色,0.0结果为黑色)<br>由于alpha通道也是相乘的，因此一个图像中的完全透明像素(不透明度0.0)会导致输出中的完全透明像素。这类似于 dstIn，但与颜色组合在一起<br>关于使颜色倍增但不使alpha通道倍增的变体，考虑 modulate*
25. BlendMode.hue<br>*获取源图像的色调，以及目标图像的饱和度和亮度<br>效果是用原图对目标图像着色<br>输出图像的不透明度计算方式与 srcOver 相同。源图像中完全透明的区域从目标获取色调*
26. BlendMode.saturation<br>*获取源图像的饱和度，以及目标图像的色调和亮度<br>输出图像的不透明度计算方法与 srcOver 相同。源图像中完全透明的区域从目的地获取其饱和度*
27. BlendMode.color<br>*获取源图像的色调和饱和度，以及目标图像的亮度<br>效果是用原图像对目标着色<br>输出图像的不透明度计算方法与 srcOver 相同。源图像中完全透明区域从目标图像获取色调和饱和度*
28. BlendMode.luminosity<br>*获取源图像的亮度，以及目标图像的色调与饱和度<br>输出图像的不透明度计算方法与 srcOver 相同。源图像中完全透明的区域从目标获取亮度*
