desc "deploy site to gitready.com"
task :deploy do
	require 'rubygems'
	require 'highline/import'
	require 'net/ssh'

	username = ask("Username:  ") { |q| q.echo = true }
	password = ask("Password:  ") { |q| q.echo = "*" }

	commands = <<EOF
cd gitready
git pull origin master
jekyll _new
mv _site _old
mv _new _site
rm -rf _old
EOF

	Net::SSH.start('gitready.com', username, :port => 1337, :password => password) do |ssh|
		ssh.exec commands.gsub(/\n/, "; ")
	end

end
