<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Laravel docker template
## Setup a new project
### Step-by-step setup
- Update composer.json, you can change the project name / description and tags for example
- Move .env.example or .env.prod.example to .env and edit it according to your project
- Start containers with `docker compose up -d`
- Run into the php container with `docker compose exec php bash`
- Install php libs with `composer install`
- Install javascript libs with `yarn`
- Run either `yarn dev` or `yarn build`
- Generate application secret key with `php artisan key:generate`
- Enjoy :)

### Fast setup
```bash
git clone https://github.com/TheoMeunier/laravel-template.git
cd laravel-template
cp .env.example .env
docker compose up -d
docker compose exec php composer install
docker compose exec php npm install
docker compose exec php npm run dev
docker compose exec php php artisan key:generate
```
