Add gem to Gemfile:

gem 'active_admin'

Run `bundle`

After run the active_admin installer, and you can se tue follow output *(pay attention for some tips)*:

```
rails g active_admin:install
    invoke  devise
    generate    devise:install
      create    config/initializers/devise.rb
      create    config/locales/devise.en.yml
 

===============================================================================

Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

  4. If you are deploying on Heroku with Rails 3.2 only, you may want to set:

       config.assets.initialize_on_precompile = false

     On config/application.rb forcing your application to not access the DB
     or load models when precompiling your assets.

  5. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

===============================================================================
      invoke    active_record
      create      db/migrate/20140828203505_devise_create_admin_users.rb
      create      app/models/admin_user.rb
      invoke      test_unit
      create        test/unit/admin_user_test.rb
      create        test/fixtures/admin_users.yml
      insert      app/models/admin_user.rb
       route    devise_for :admin_users
        gsub    app/models/admin_user.rb
        gsub    config/routes.rb
      insert    db/migrate/20140828203505_devise_create_admin_users.rb
      create  config/initializers/active_admin.rb
      create  app/admin
      create  app/admin/dashboard.rb
      create  app/admin/admin_user.rb
      insert  config/routes.rb
    generate  active_admin:assets
[deprecated] I18n.enforce_available_locales will default to true in the future. If you really want to skip validation of your locale you can set I18n.enforce_available_locales = false to avoid this message.
      create  app/assets/javascripts/active_admin.js
      create  app/assets/stylesheets/active_admin.css.scss
      create  db/migrate/20140828203510_create_admin_notes.rb
      create  db/migrate/20140828203511_move_admin_notes_to_comments.rb
```
