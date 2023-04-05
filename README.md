<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

-   [Simple, fast routing engine](https://laravel.com/docs/routing).
-   [Powerful dependency injection container](https://laravel.com/docs/container).
-   Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
-   Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
-   Database agnostic [schema migrations](https://laravel.com/docs/migrations).
-   [Robust background job processing](https://laravel.com/docs/queues).
-   [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 1500 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

-   **[Vehikl](https://vehikl.com/)**
-   **[Tighten Co.](https://tighten.co)**
-   **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
-   **[64 Robots](https://64robots.com)**
-   **[Cubet Techno Labs](https://cubettech.com)**
-   **[Cyber-Duck](https://cyber-duck.co.uk)**
-   **[Many](https://www.many.co.uk)**
-   **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
-   **[DevSquad](https://devsquad.com)**
-   **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
-   **[OP.GG](https://op.gg)**
-   **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
-   **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

## Authors

-   [@jahidul2018](https://www.github.com/jahidul2018)

## 🚀 About Me

I'm a full stack developer...

My interests range from data science to machine learning.love to work as a web Developer with new technology. Currently, studying Applied statistics and Data Science at Jahangirnagar University. System Analysis is one of my favourites. Learning Project management methodology and Documentation (Technical, Analytical) help me a lot to understand Software Usability Support and Technical Support. And last but not least I am a nature lover like Albert Einstein and one of my favourite Quote is "Look deep into nature, and then you will understand everything better".

here is my linkedin profile:
https://www.linkedin.com/in/jahidulalammishuk/

## Acknowledgements

-   [ Harsukh Makwana](https://github.com/Harsukh21)
-   [ Ahmed Bouchefra](https://www.techiediaries.com/author/ahmed-bouchefra/)
-   [ Devendra Dode](https://www.tutsmake.com/author/devtutsmake-com/)

# Project Title

laravel jwt rest api

## Demo

demo you are looking for :

-   [laravelCode](https://www.laravelcode.com/post/how-to-authenticate-in-laravel-8-jwt/)
-   [techiediaries](https://www.techiediaries.com/laravel-8-rest-api-authentication-jwt-tutorial-example/)
-   [tutsmake](https://www.tutsmake.com/laravel-8-jwt-rest-api-authentication-example-tutorial/)
-   [techiediaries](https://www.techiediaries.com/laravel-8-rest-api-authentication-jwt-tutorial-example/)

## Data set

this a dummy data set

## Create project

So let's start from creating latest Laravel application.

## Step 1: Create fresh Laravel application

In the tutorial, the first step is to create new Laravel application. We will use following Composer command to create latest version of Laravel application. Open the Terminal and run the following command.

<code>
composer create-project laravel/laravel jwt --prefer-dist
</code>

After the application is created, change Terminal working directory to project.

cd jwt

## Step 2: Install and configure JWT library

In the second step, install JWT library using below Composer command.

<code>
composer require tymon/jwt-auth
</code>

Now register the library service provider to config/app.php file. Open file and add the following lines into providers array.

<code>
'providers' => [
    ....
    Tymon\JWTAuth\Providers\LaravelServiceProvider::class,
],
</code>

Publish JWT config file using vendor:command command into terminal.

<code>
php artisan vendor:publish --provider="Tymon\JWTAuth\Providers\LaravelServiceProvider"
</code>

This will copy configuration file from vendor to config/jwt.php.

We also need to generate token secret. Run the below artisan command.

<code>
php artisan jwt:secret
</code>

This will create JWT token secret to .env file.

JWT_SECRET=RGffekr......hGKasf5u

## Step 3: Configuration of database in .env file

Now we will need to configure database connection. Open .env file from the root directory and change below database credentials with your MySQL.

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=jwt
DB_USERNAME=root
DB_PASSWORD=secret
We will use default users table to authenticate API. Laravel already have users table. You can customize users table field at database/migrations directory. Lastly migrate users table into database using following command.

php artisan migrate

## Step 4: Update User model

Now we need to modify User model. Open App/Models/User.php file and implement Tymon\JWTAuth\Contracts\JWTSubject interface. We also need to add two model methods getJWTIdentifier() and getJWTCustomClaims().

<code>
<?php

namespace App\Models;
use Illuminate\Contracts\Auth\MustVerifyEmail;
use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Foundation\Auth\User as Authenticatable;
use Illuminate\Notifications\Notifiable;
use Tymon\JWTAuth\Contracts\JWTSubject;

class User extends Authenticatable implements JWTSubject
{
use HasFactory, Notifiable;

    /**
    * Get the identifier that will be stored in the subject claim of the JWT.
    *
    * @return mixed
    */
    public function getJWTIdentifier()
    {
        return $this->getKey();
    }

    /**
    * Return a key value array, containing any custom claims to be added to the JWT.
    *
    * @return array
    */
    public function getJWTCustomClaims()
    {
        return [];
    }

}

?>
</code>

## Step 5: Configure default authentication guard

The default authentication guard is web. We need to change it to api. Open config/auth.php file and change default guard to api.

<code>
<?php

return [

    'defaults' => [
        'guard' => 'api',
        'passwords' => 'users',
    ],

    'guards' => [
        'web' => [
            'driver' => 'session',
            'provider' => 'users',
        ],

        'api' => [
            'driver' => 'jwt',
            'provider' => 'users',
        ],
    ],

];

?>
</code>

## Step 6: Add Authentication routes

In this step, we need to register authentication routes into routes/api.php file. Open the file and add below routes into it.

<code>
<?php

use Illuminate\Http\Request;
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\JWTController;

Route::group(['middleware' => 'api'], function($router) {
Route::post('/register', [JWTController::class, 'register']);
Route::post('/login', [JWTController::class, 'login']);
Route::post('/logout', [JWTController::class, 'logout']);
Route::post('/refresh', [JWTController::class, 'refresh']);
Route::post('/profile', [JWTController::class, 'profile']);
});
</code>

## Step 7: Create JWTController controller class

We have defined routes for authentication so far. We need to create controller class to build application logic. The below Artisan command will generate controller class at App/Http/Controllers directory.

<code>
php artisan make:controller JWTController
</code>

In the controller class, add the methods as per routes.

<code>
<?php

namespace App\Http\Controllers;

use Auth;
use Validator;
use App\Models\User;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Hash;

class JWTController extends Controller
{
/\*\*
_ Create a new AuthController instance.
_
_ @return void
_/
public function \_\_construct()
{
$this->middleware('auth:api', ['except' => ['login', 'register']]);
}

    /**
     * Register user.
     *
     * @return \Illuminate\Http\JsonResponse
     */
    public function register(Request $request)
    {
        $validator = Validator::make($request->all(), [
            'name' => 'required|string|min:2|max:100',
            'email' => 'required|string|email|max:100|unique:users',
            'password' => 'required|string|confirmed|min:6',
        ]);

        if($validator->fails()) {
            return response()->json($validator->errors(), 400);
        }

        $user = User::create([
                'name' => $request->name,
                'email' => $request->email,
                'password' => Hash::make($request->password)
            ]);

        return response()->json([
            'message' => 'User successfully registered',
            'user' => $user
        ], 201);
    }

    /**
     * login user
     *
     * @return \Illuminate\Http\JsonResponse
     */
    public function login(Request $request)
    {
        $validator = Validator::make($request->all(), [
            'email' => 'required|email',
            'password' => 'required|string|min:6',
        ]);

        if ($validator->fails()) {
            return response()->json($validator->errors(), 422);
        }

        if (!$token = auth()->attempt($validator->validated())) {
            return response()->json(['error' => 'Unauthorized'], 401);
        }

        return $this->respondWithToken($token);
    }

    /**
     * Logout user
     *
     * @return \Illuminate\Http\JsonResponse
     */
    public function logout()
    {
        auth()->logout();

        return response()->json(['message' => 'User successfully logged out.']);
    }

    /**
     * Refresh token.
     *
     * @return \Illuminate\Http\JsonResponse
     */
    public function refresh()
    {
        return $this->respondWithToken(auth()->refresh());
    }

    /**
     * Get user profile.
     *
     * @return \Illuminate\Http\JsonResponse
     */
    public function profile()
    {
        return response()->json(auth()->user());
    }

    /**
     * Get the token array structure.
     *
     * @param  string $token
     *
     * @return \Illuminate\Http\JsonResponse
     */
    protected function respondWithToken($token)
    {
        return response()->json([
            'access_token' => $token,
            'token_type' => 'bearer',
            'expires_in' => auth()->factory()->getTTL() * 60
        ]);
    }

}
</code>

We have created methods for authenticating APIs for Login, Register, Profile, Token Refresh and Logout routes.

## Step 8: Test application in Postman

We have completed the application coding. Start the Laravel server using below Artisan command.

<code>
php artisan serve

</code>

.............................

For testing APIs, we will use Postman application. Postman is an API platform for building and using APIs. We will test all API. Lets start from register API.

<h2>Postman</h2>

## Register API

All API routes are prefixed with api namespace. In the postman
use <code> http://localhost:8000/api/register </code>

API endpoint. Pass name, email, password and password_confirmation parameters into request. You will get message and user details into response.

## Login API

Use <code> http://localhost:8000/api/login </code>

API endpoint with email password parameter with request. If the email and password matches with registered user, you will receive token json object into response.

## Profile API

All auth:api middleware routes are protected with api guard. You need to pass access_token in Header as bearer token.

## Refresh Token API

You can refresh the current token with new token using auth()->refresh() method.

## Logout API

To logout the user, you need to invalidate the current token. You can simply call auth()->logout() method to invalidate current access token. Once user, logged out, it can't access protected routes.

## Conclusion

Eventually, our tutorial is over. We have learned how to implement JWT authentication in Laravel application. In the next tutorial, we will use JWT token for REST API.

I hope, this tutorial will help on your development. If you liked this tutorial, please consider to share with your friends.

## postman file

link: laravel-jwt-rest-api.postman_collection.json

## reference:

link: https://www.laravelcode.com/post/how-to-authenticate-in-laravel-8-jwt

## resource:

link: https://github.com/jahidul2018/laravel-jwt-rest-api
