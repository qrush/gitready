# Git Ready

> There is only one way to *get ready* for immortality, and that is to love this life and live it as bravely and faithfully and cheerfully as we can.<br />
> ~ Henry Van Dyke

## About

This repository hosts the HTML, CSS, images, and posts for [gitready.com](http://gitready.com). Git Ready publishes (was daily, then tri-weekly, and now) weekly tips for those who want to learn more about the VCS or just get started. The blog as a whole started as a journey to learn more about Git and show others how useful it is. If you find issues with the content, just send [qrush a message on GitHub](http://github.com/qrush) or email him at [nick@quaran.to](mailto://nick@quaran.to).

## Publishing

This blog is generated with the [Jekyll](http://github.com/mojombo/jekyll) engine. Simple and easy formatting that sticks to the basics. All static HTML too, so worrying about scalability is non-existent.

## Contributing

If you have ideas about new pages, layouts, or what have you, fork away!<br /> If you want to submit tips, [please do so here](http://gitready.com/submit.html).

## Translating

If you are interested in translating posts into another language, great! Here's what to do:

* Fork the project.
* Create a branch with the ISO code for your language, so for english:

<pre>
git checkout -b en
</pre>

* Unpublish all the posts (and commit your changes):

<pre>
rake unpublish
git commit -am "Unpublishing all the posts"
</pre>

* Translate the front page headers, footers. Check out the other translated sites for an example, such as the [german one](http://de.gitready.com).
* Translate as little or as many posts as you so desire.
* Push your work back up (remember to use the right branch name!):

<pre>
git push origin en
</pre>

* Submit a pull request to qrush's repository.

Once that's done, I'll add your language's subdomain and get it published.

## Licensing

The actual content of the articles is licensed under Creative Commons. The code that this project consists of is licensed under MIT.

Basically, if you're going to redistribute a blog post, just make sure to link back. If you'd like to publish the content, that's fine too, just please keep the licensing information in.
