## Installation Development mode

Make sure you have the following installed:
* docker compose up
* Go inside the spree-backend container and run
```
bin/rails db:prepare
bin/rails db:seed
bin/rails log:clear tmp:clear
bin/rake spree_sample:load
```
* then again restart docker
```
docker compose down
docker compose up
```
* Ruby 3.3 - [installation instructions](https://www.ruby-lang.org/en/documentation/installation/)
* Vips - [installation instructions](https://libvips.github.io/libvips/install.html)

```bash
bin/setup
```

If you want to use sample data (products, categories), you can load it using the following command:

```bash
bin/rake spree_sample:load
```

### Switching to MySQL

By default, Spree Starter uses PostgreSQL. If you want to switch to MySQL, you can do so by running the following command:

```bash
bin/rails db:system:change --to=mysql
```

