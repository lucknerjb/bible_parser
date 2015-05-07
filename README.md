# BibleXML

[![Build Status](https://travis-ci.org/seven1m/bible_xml.svg?branch=master)](https://travis-ci.org/seven1m/bible_xml)

This is a Ruby library for parsing different bible XML formats.

For now, it only supports USFX and OSIS, but I hope to add support for other formats also.

## Install

When the library is ready, I'll publish the gem and you'll be able to:

```
gem install bible_xml
```

## Use

You can get the World English Bible (WEB) in USFX format [here](http://ebible.org/web/). Unzip and put the usfx.xml file somewhere.

```ruby
require 'bible_xml'

bible = BibleXML.new(File.open('web.usfx.xml'))
verse = bible.books.first.chapters.first.verses.first
# => <Genesis 1:1>
verse.text
# => "In the beginning, God created the heavens and the earth.\n"
```

## License

Copyright (c) 2015 Tim Morgan. Licensed MIT. See LICENSE file.
