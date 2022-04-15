handler文件夹代表处理器的意思
acpect（切面）包用来放日志处理
interceptor包用来放过滤器
static静态的
templates可以从后台获取一些信息
@Controller 代表是一个控制器
@GetMapping() 通过get方式请求路径
@ControllerAdvice 表示拦截掉所有标注有Controller的控制器

如何让框架出现异常的情况下跳转到自己定义的error.html页面？
    需要拦截一下，没有拦截的时候，是springboot拦截的错误。它根据错误页面命名的方式去找到相对应的页面。
    所以我们需要自己拦截错误。定义一个拦截器(ControllerExceptionHandler),来拦截所有的异常。