# Mini Claim Application

Clone the repository

```bash
git clone git@github.com:sukiandi/laravel-claim.git
```

Go to the directory and application folder
```bash
cd laravel-claim/claim-mini
```

Run the app by execute:
```bash
./vendor/bin/sail up -d
```

If you get error like this
```
bash: ./vendor/bin/sail: No such file or directory
```

You have to install composer dependencies by:
```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```
You can read more details in [Laravel documentation](https://laravel.com/docs/9.x/sail#installing-composer-dependencies-for-existing-projects)

To stop the application:
```bash
./vendor/bin/sail down
```

Once the application start, run migration:
```bash
./vendor/bin/sail artisan migrate
```

Now you can visit http://localhost/ to view the application.
