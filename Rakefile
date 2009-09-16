desc "deploy site to gitready.com"
task :deploy do
  require 'rubygems'
  require 'highline/import'
  require 'net/ssh'

  regex = /refs\/heads\//
  branches = []
  `git ls-remote qrush`.split[2..-1].each do |l|
    branches << l.gsub(regex, '') if l =~ regex
  end

  username = ask("Username:  ") { |q| q.echo = true }
  password = ask("Password:  ") { |q| q.echo = "*" }

  Net::SSH.start('gitready.com', username, :port => 1337, :password => password) do |ssh|
    commands = "cd ~/gitready/cached-copy; git fetch;"
    branches.each do |branch|

      commands << <<EOF
git reset --hard origin/#{branch}
rm -rf ../#{branch}
jekyll --no-auto ../#{branch}
EOF
    end
      commands = commands.gsub(/\n/, "; ")
      #puts commands
      ssh.exec commands
  end
end

desc "Unpublish all posts"
task :unpublish do
  Dir["_posts/*.textile"].each do |post|
    puts "Unpublishing #{post}"
    lines = File.readlines(post)
    lines.insert(1, "published: false\n")
    File.open(post, "w") { |f| f.write lines.join }
  end
end
