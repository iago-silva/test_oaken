Example test using Oaken -> [test/models/account_test.rb](https://github.com/iago-silva/test_oaken/blob/main/test/models/account_test.rb)

Where the `accounts.iago` has been created? -> [db/seeds/accounts/iago.rb](https://github.com/iago-silva/test_oaken/blob/main/db/seeds/accounts/iago.rb).

# Configuration

Just need to put 

```ruby
Oaken.prepare do
  seed :accounts
end
```

inside `seeds.rb` and the gem will load `db/seeds/accounts/*.rb`

# Generator

I tried to use `rails generate oaken:convert:fixtures` but didn't work well.

This generator tries to convert everything inside `test/fixtures` to seed files.

# Development env

If you run `rails db:seed` Oaken will run all seeds defined in `Oaken.prepare`, in this case `seed :accounts`. 

The gem uses the same seed files for both test and dev environments, so the same data will populate the test and dev databases.
