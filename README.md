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
