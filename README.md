# A simple Create, Read, Update and Delete (CRUD) Demo in Laravel 6

It's been a while since I did any Web Dev as I've been focusing on teaching Python.

Here's some of the setup steps and gotchas in case it might help anyone.

## Getting Up and Running with Laravel on Windows 10

### Software Pre-requisites

### PHP
Installing the lastest version was a bit of a drag as previously I had it as part of AMPPs

http://kizu514.com/blog/install-php7-and-composer-on-windows-10/

### Node.js
Needed updating

Deleting node_modules when debugging run issues needed admin permission.

### Blade
Fairly straightforward syntax for views {{yay!}}


### MySQL
I had an existing installation that came with AMPPS, but ended up installing MqSQl standalone

Using version 8.something, I had access issues:  

https://github.com/laravel/framework/issues/27742#issuecomment-513257809 
Here is a fix:

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password here';`

#### Viewing DB data
Use powershell
`mysql -u root -p`

#### Artisan migrate
Don't forget to use this to set up DB

### Environment variables
System path must include
- php
- mysql
- node

and probably others that I already had.

Remember to check here if you have powershell messages like "that is not a recognised thing that we like."

### IDE 
Netbeans 11


## Using a Virtual Machine
I persisted and got Laravel runnning using Vagrant and VirtualBox, but then decided I wanted more direct control so went for running it directly on my host machine.

### Serving you project

`php artisan serve`  
`php artisan serve --host=localhost --port=80`  
`php artisan serve --host=my-site.local --port=80`  

Don't forget hosts file.


## Frontend
https://www.techiediaries.com/laravel-ui-tutorial/
`composer require laravel/ui --dev`

https://laravel.com/docs/6.x/frontend
`php artisan ui bootstrap --auth`


### PowerShell
Always open in administrator mode!!

### Notes

It takes a surprisingly long time for packages to load.

### Use/Contacts
`use App\Contact;`   
`use Illuminate\Http\Request;`  

In ContactsController the order matters!


### Links
One way to create URLs
`<a href="{{ route('contacts.index') }}">Display Contacts</a>`

