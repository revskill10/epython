Upgrading


git clone https://github.com/instructure/canvas-lms canvas2
cd canvas2
cp ../canvas/config/*.yml config/
bundle install

bundle exec rake canvas:compile_assets

RAILS_ENV=production $GEM_HOME/bin/bundle exec rake db:migrate

RAILS_ENV=production $GEM_HOME/bin/bundle exec rake db:load_notifications

