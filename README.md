![](http://f.cl.ly/items/0M3L273P2r2l0A3L052M/avatars.png)

# avatarly

avatarly is a simple gem for creating gmail-like user avatars based on user email or any other string passed

inspired and influenced by https://github.com/johnnyhalife/avatar-generator.rb

## Installation

Avatarly requires ImageMagick to be installed.

### Gems

The gems are hosted at Rubygems.org. Make sure you're using the latest version of rubygems:

    $ gem update --system

Then you can install the gem as follows:

    $ gem install avatarly

### Bundler

Add to your Gemfile:

    gem "avatarly"

and then type:

    bundle install

## Usage

To generate image please do:

    Avatarly.generate_avatar(text, opts={})

the only required parameter is <tt>text</tt>. Other options that you can pass are:

* <tt>background_color</tt> (#AABBCC)
* <tt>font_color</tt> (#AABBCC)
* <tt>size</tt>  (default: 32)
* <tt>font</tt>  (path to font - e.g. "#{Rails.root}/your_font.ttf")
* <tt>font_size</tt> (default: size / 2)

As a result you will get an image blob - rest is up to you, do whatever you want with it.

For instance you can store avatar in directory with images:

      img = Avatarly.generate_avatar(text, opts={})
      File.open('public/images/avatar_name.png', 'wb') do |f|
        f.write img
      end

## License

MIT
