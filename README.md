这个脚本的主要框架大致如下：
导入所需的模块：这包括requests模块用于网络请求， BeautifulSoup用于解析HTML，os用于文件操作。
设置常量：这里包括用户代理、请求头、网域、URL以及图片保存的文件夹等。
定义函数：这包括请求获取页面源码的函数、解析HTML的函数以及下载和保存图片的函数。
定义主函数：主函数中，首先检查所需的图片保存文件夹是否存在，不存在就创建它。然后使用上面定义的函数获取主页源码并解析，
          寻找到所有需要访问的子页面链接。对每个子页面，都进行循环访问并下载图片，直到该子页面无更多页码（子页面可能分页）。间隔一定时间继续下一个子页面访问和图片下载。
在脚本的最后，执行主函数。
在执行过程中，主要包括了网络请求、HTML解析和图片下载三大部分的操作。此外，所有的网络请求过程中都通过try-except进行异常捕获，失败时打印提示并继续之后的操作。
