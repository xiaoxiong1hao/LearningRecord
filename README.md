# LearningRecord
每日学习/阅读记录  
姓名：David  起始日期：2025年8月12日  目标天数：90天

使用说明：
1. 每日完成学习/阅读任务后打✓ 
2. 记录实际学习/阅读时长 
3. 每天睡前完成简单反思

月度打卡表：

| 日期| 学习/阅读内容 | 计划时长 | 实际时长 | 完成情况 | 今日收获/反思 |   |
|--------------------------------------------|---------|------|------|------|---------|---|
| 25/08/12 | 1.MediaCodec API说明，流控；<br>2.浏览音视频的采集、编码、封包成 mp4 输出的流；<br>3.OpenGLES介绍和环境搭建；<br>4.Java线程间通信。|固定时长2h其他未计算 | 2h+ | ✅|  1.同步/异步编解码如何选择？媒体文件上传下载，音视频推流的具体操作？<br>2.具体的在项目代码中有需复习确认。<br>3.主要讲的GLSurfaceView的Renderer接口。<br>4.包含了synchronized与“Monitor”，interrupt()/wait()/notify()/notifyAll()/join()/yield()的用法。|   |
| 25/08/13 | 1.复习多线程合线程同步；<br>2.Android的多线程；<br>3.OpenGLES定义形状，绘制形状。|3h |3h+|✅|1.volatile提供同步性，AtomicReference提供同步性和原子性。ReentrantReadWriteLock分别管理读和写，写紧读松。线程安全围绕共享资源展开。<br>2.Handler的核心实现, HandlerThread(单线程，仅争对需要主线程操作的场景), Excutors(多线程且可覆盖所有场景),AsyncTask的内存泄露谬论, 实际上内存仍会被回收。<br> 3.OpenGLES的GLSL语言:vertex shader顶点着色器定义形状;fragment shader定义颜色和纹理; program用于绘制。shader编译和它们与program的链接属于耗时操作, 应只创建一次并缓存它们。| |
| 25/08/14 | 1.学习Java的IO,NIO和Okio；<br>2.学习泛型类型的创建；<br>3.OpenGLES:图形API以及专业名词解析;渲染流程以及固定存储着色器.|3h ||❌|| |
| 25/08/15 | 1.学习Java的IO,NIO和Okio；<br>2.学习泛型类型的创建；<br>3.OpenGLES:图形API以及专业名词解析;渲染流程以及固定存储着色器.|3h |50mins|❌|1.复习了InputStream/OutputStream，FileInputStream/FileOutputStream,Reader/Writer,BufferedInputStream/BufferedOutputStream的用法；在文件读写上,前面几个类像一根接在一根上的吸管;try(){}catch{}括号中实例化以上几个类，会在finally中自动调用文件关闭方法close()| |
| 25/08/20 | 1.学习泛型类型的创建；<br>2.泛型类型实例化的上界与下界；<br>3.泛型方法和类型推断;<br>4.泛型的本质，什么时候使用泛型;<br>5.泛型的类型擦除和限制与如何突破限制。|3.5h |3.5h|✅|1.写在类名边上尖括号中的“T”叫类型参数，实例化对象，实现接口或者其他场景传入具体的类型叫类型实参。支持传入多个类型参数。静态字段、方法不能使用类型参数。<br>2.类型参数的上界：public interface SimShop<T,C extends Sim & Cloneable & Runnable>{} <br>泛型类型实例化的上界与下界：ArrayList<? extends Fruit> fruitList 只能传入Fruit或其子类，只能get，不能再修改List。<br> List<? super Apple> appleList 只能传入Apple及其父类，不能从List中get。<br>3.泛型方法声明<E> E tradeIn(E item, float money); 调用时会根据返回值对实参item进行类型推断。存在静态泛型方法，使用static修饰。<br>4.作为方法的返回类型、放在接口的参数中等实现类去定义方法的返回值；泛型方法中通过对泛型参数的约束可以达到对返回值和实参的**类型约束**。5.类型擦除：运行时<T>被擦除,替换为Object。运行想获取到泛型信息，通过对使用泛型的类创建子类，反射拿到泛型信息。<br>List<Object> objects = new ArrayList<String>();不可行，因为泛型不支持协变。List<? super String> str = new ArrayList<Object>();通过泛型实现逆变。泛型类的数组不可用，因为不可协变性会传染。建议使用ArrayList代替泛型数组。| |
| 25/08/25 | 1.图形的位置和尺寸测量；<br>2.Xfermode的使用解析。|2.5h |2.5h|✅|1.复习canvas绘制流程;学习绘制Path的⽅向以及封闭图形的内外判断（Winding和Even_Odd）;学习PathMeasure（测量长度，切角）,PathDashPathEffect（虚线）使用方法;复习绘制弧形drawArc()，圆drawOval()，矩形drawRect()的方法;三⻆函数的计算 横向的位移是 cos，纵向的位移是 sin；canvas的translate(),save(),restore;需注意刻度表中第0个刻度的宽需要被考虑到。<br>2.使用Xfermode的目的：把多次绘制进⾏「合成」，例如蒙版效果：⽤ A 的形状和 B 的图案;Xfermode最佳实现方式:Canvs.saveLayer() 把绘制区域拉到单独的离屏缓冲⾥。| |
| 25/08/26 | 1.Camera投影，文字的测量；<br>2.canvas的裁切，变换;Metrix变换。|2.5h |2.5h|✅|1.Camera发射投影的点在Z轴-8左右;复习文字测量中的bounds，五条基线（top ascend,baseline,descend,bottom）;基线通过Paint.getFontMetrics()获取。<br>2.clipRect()、clipPath()有锯齿效果，因为强行切边;canvas几何变换后注意绘制draw...()的坐标已经发生改变。Metrix变换绘制后坐标不会改变。| |
| 25/08/27 25/08/28 | 1.属性动画，硬件加速；<br>2.Bitmap和Drawable。<br>3.AttributeSet|4h |4h|✅|1.view.animate()使用;ObjectAnimator的使用(推荐);PropertyValuesHolder使用;KeyFrame比Interpolator控制自由度更高，搭配PropertyValuesHolder使用。<br>AnimateSet的使用。TypeEvaluator可⽤于设置动画完成度到属性具体值的计算公式。硬件加速是什么？如何完成了加速？硬件加速存在兼容性问题。离屏缓冲是什么？setLayerType()针对view 和 saveLayer()针对canvas的使用，saveLayer较重，建议使用setLayerType()。<br>2.Bitmap是什么，Drawable是什么？Bitmap和Drawable互相转换;自定义drawable。<br>3.AttributeSet搭配obtainStyledAttributes()使用获取自定义View的自定义属性值。| |
| 25/09/03 | 1.测量、布局作用，原理；<br>2.自定义View;<br>3.自定义ViewGroup|2h |2h|✅|1.确定每个 View 的位置和尺⼨，作⽤：为绘制和触摸范围做⽀持。<br>2.重写 onMeasure()->计算出⾃⼰的尺⼨->⽤ resolveSize() 或者 resolveSizeAndState() 修正结果->使⽤ setMeasuredDimension(width, height) 保存结果。3.重写 onMeasure()->遍历每个⼦ View，测量⼦ View->测量出所有⼦ View 的位置和尺⼨后，计算出⾃⼰的尺⼨，并⽤setMeasuredDimension(width, height) 保存->重写 onLayout()->遍历每个⼦ View，调⽤它们的 layout() ⽅法来将位置和尺⼨传给它们.| |

