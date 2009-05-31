desc "deploy site to gitready.com"
task :deploy do
  require 'rubygems'
  require 'highline/import'
  require 'net/ssh'

  regex = /refs\/heads\//
  branches = []
  `git ls-remote origin`.split[2..-1].each do |l|
    branches << l.gsub(regex, '') if l =~ regex
  end

  username = ask("Username:  ") { |q| q.echo = true }
  password = ask("Password:  ") { |q| q.echo = "*" }

  Net::SSH.start('gitready.com', username, :port => 1337, :password => password) do |ssh|
    commands = "cd ~/gitready/cached-copy; "
    branches.each do |branch|

      commands << <<EOF
git checkout #{branch} 
git pull origin #{branch}
git checkout -f
rm -rf _site
jekyll --no-server --no-auto
mv _site ../_#{branch}
mv ../#{branch} _old
mv ../_#{branch} ../#{branch}
rm -rf _old
EOF
    end
      commands = commands.gsub(/\n/, "; ")
      #puts commands
      ssh.exec commands
  end
end
