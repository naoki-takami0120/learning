# Chirper (Laravel Bootcamp)
Source: https://laravel.com/learn/getting-started-with-laravel

A Twitter-like microblogging app built while following the official Laravel tutorial.

## Progress
- [x] Lesson 2: Project setup
- [x] Lesson 3: First route & Blade layout component
- [x] Lesson 4: Deploy to Laravel Cloud
- [x] Lesson 5: MVC & first controller
- [x] Lesson 6: Database & migrations
- [x] Lesson 7: First eloquent model
- [x] Lesson 8: Seeding the database
- [x] Lesson 9: Creating and storing chirps
- [x] Lesson 10: Editing and deleting chirps
- [x] Lesson 11: User registration
- [x] Lesson 12: Login and logout

## What I learned
- Routing with the `Route` facades and Blade views
- Reusable layouts with Blade components
- MVC: moving logic from routes into a resource controller
- Passing data from controllers to views and looping with `@foreach`
- Defining tables with migrations and running `php artisan migrate`
- Eloquent models: mapping the `chirps` table to the `Chirp` class
- Seeding dummy data with `DatabaseSeeder` and `php artisan db:seed`
- Validating input with `$request->validate()` and displaying error messages
- Route model binding (`Chirp $chirp` resolves the record from the URL)
- Method spoofing with `@method('PUT')` / `@method('DELETE')` in HTML forms
- CSRF protection with `@csrf`
- Pre-filling forms with `old('message', $chirp->message)`
- Single action controllers (invokable controllers with `__invoke()`)
- Separating guest and authenticated routes with `guest` / `auth` middleware
- Hashing passwords and logging in new users with `Auth::login()`
- `$request->session()->regenerate()` issues a new session ID on login while keeping existing session data (prevents session fixation)
- `redirect()->intended('/')` sends users back to the protected page they originally tried to visit before being redirected to login
