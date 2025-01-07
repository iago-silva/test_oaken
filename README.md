Testing [Oaken](https://github.com/kaspth/oaken).

# How does it work?

Example test 👉 [test/models/account_test.rb](https://github.com/iago-silva/test_oaken/blob/main/test/models/account_test.rb).

Where the `accounts.iago` has been created? 👉 [db/seeds/accounts/iago.rb](https://github.com/iago-silva/test_oaken/blob/main/db/seeds/accounts/iago.rb).

# Configuration

Just need to put 

```ruby
Oaken.prepare do
  seed :accounts
end
```

inside `seeds.rb` and the gem will load `db/seeds/accounts/*.rb`

# Generator

I tried to use `rails generate oaken:convert:fixtures` but it didn't work well.

This generator tries to convert everything inside `test/fixtures` to seed files.

# Development env

If you run `rails db:seed` Oaken will run all seeds defined in `Oaken.prepare`, in this case `seed :accounts`. 

The gem uses the same seed files for both test and dev environments, so the same data will populate test and dev databases.
