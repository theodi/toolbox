require 'yaml'

desc 'create a new compass project'
task :compassify do
  print 'Setting up compass... '
  `bundle exec compass create . -r bootstrap --using bootstrap`
  FileUtils.mv 'sass', '_sass'
  FileUtils.mv 'stylesheets/styles.css', '_sass/_bootstrap.scss'
  FileUtils.rm_r 'stylesheets'
  FileUtils.mkdir_p 'assets'
  application_css = %{---
---

@import 'styles';
}
  File.open 'assets/application.scss', 'w' do |f|
    f.write application_css
  end
  FileUtils.rm 'config.rb'
  puts 'done'
end

desc 'set up _config.yml'
task :configify do
  print 'Setting up _config.yml... '
  defaults = {
    'defaults' => [
      {
        'scope' => {
          'path' => ''
        },
        'values' => {
          'layout' => 'default'
        }
      }
    ],
    'permalink' => 'pretty'
  }

  File.open '_config.yml', 'w' do |f|
    f.write defaults.to_yaml
  end
  puts 'done'
end

layout = %{<!DOCTYPE html>
<html lang='en'>
  <head>
    <meta charset='utf-8' />
    <meta http-equiv='X-UA-Compatible' content='IE=edge' />
    <meta name='viewport' content='width=device-width, initial-scale=1' />

    <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src='https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js'></script>
      <script src='https://oss.maxcdn.com/respond/1.4.2/respond.min.js'></script>
    <![endif]-->

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src='https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js'></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src='/javascripts/bootstrap.min.js'></script>

    <link rel='stylesheet' href='/assets/application.css' type='text/css' />
    <title>{{ page.title }}</title>
  </head>

  <body>
    <div class='container'>
      {{ content }}
    </div>
  </body>
</html>}

desc 'install default layout'
task :layout do
  print 'Installing default layout... '
  FileUtils.mkdir_p '_layouts/'
  File.open '_layouts/default.html', 'w' do |f|
    f.write layout
  end
  puts 'done'
end

desc 'install .gitignore'
task :gitignore do
  print 'Installing .gitignore... '
  File.open '.gitignore', 'w' do |f|
    f.write "_site\n"
    f.write ".sass-cache\n"
  end
  puts 'done'
end

desc 'create index.md'
task :indexify do
  print 'Creating index.md... '
  index_md = %{---
---

Hold tight HTML
}
  File.open 'index.md', 'w' do |f|
    f.write index_md
  end
  puts 'done'
end

desc 'Set up Bootstrap'
task bootstrap: [
  :compassify,
  :configify,
  :gitignore,
  :layout,
  :indexify
]
