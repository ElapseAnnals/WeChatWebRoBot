<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"><span align="center">Plus</span> </p>

#### About
基于 Laravel 增加一部分软件包和进行实际业务使用功能调整

### 使用方式

```php
git clone https://github.com/ElapseAnnals/LaravelPlus.git   // clone 项目
cp -a LaravelPlus/ yourProduct/    // 复制项目至自身项目
rm composer.lock .env

cp .env.example .env    // 复制配置
php artisan key:generate    // 更新 key
php artisan storage:link // 软连接映射
composer update   // 更新软件包 （默认已安装 composer ）

 php artisan make:framework Test  // 创建分层架构
 php artisan make:framework Test --basis  // 创建基础分层架构（Service, Repository）
 php artisan make:framework Test --D // 删除分层架构 
```
[composer 国内地址](https://www.phpcomposer.com/)

### 改动内容
- 设置日志打印默认按天执行（.env::LOG_CHANNEL）
- 增加加载软件包
 
  - respect/validation
  - barryvdh/laravel-debugbar
  - barryvdh/laravel-ide-helper
  - reliese/laravel
  - overtrue/laravel-query-logger"
  
 - 增加热切换配置（config/dynamic）
 
   -  develop 开发/测试
        - stage 测试 
   -  local 本地
   -  production 生产
   
 - 增加默认图片存储目录（storage/app/public/images)
 - 扩展结构分层 [来源](https://learnku.com/articles/19452?order_by=created_at&)
  
    - 主要分层
    
        - Service 业务服务层
        - Repository 数据仓库层
    - 扩展分层
        - Presenter 固定业务中控层
        - Transformer 转化层/筛选层（筛选后在选择输出）
        - Formatter 格式化层（对于输出数据进行格式化，服务于 view 层），便于前端模版渲染与展示
          
     
   
  






#### Version
当前版本基于 5.8 改造

#### Todo
        - stage 测试 
        增加项目迁移功能
        
        
