## laravel 框架学习笔记

### 数据库迁移

 1. 即便不是laravel的代码 也会生成自动生成创建和更新时间

> $table->timestamp('created_at')->default(DB::raw('CURRENT_TIMESTAMP'));
>
> $table->timestamp('updated_at')->default(DB::raw('CURRENT_TIMESTAMP on update CURRENT_TIMESTAMP'));

### 跨域问题解决

> * [Larave扩展laravel-cors](https://www.jianshu.com/p/1bae1d6a03b2)
> 
> * 注意：需要在app\Http\Kernel.php中的$routeMiddleware添加 'cors' => \Barryvdh\Cors\HandleCors::class

### 生产环境下的配置缓存

> php artisan config:cache 命令作为生产环境部署常规的一部分
>
> Artisan 命令 config:cache 将所有的配置文件缓存到单个文件中

