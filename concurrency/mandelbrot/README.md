**绘制 Mandelbrot set**: Mandelbrot set，描绘了函数 f(z) = z^2 + c 的轨迹是否有界。对于复平面上每一个点，求值都是完全独立的，因此对计算图的静态划分也是显然的。我们混用了 OpenMP 和我们的线程库。我们的线程库仅限于隔一段时间将当前渲染的结果显示在屏幕上，并在所有线程结束后输出渲染图。