### Yomu
---
https://github.com/yomurb/yomu

```
gem 'yomu'
bundle
gem install yomu
```

```ruby
require 'yomu'
data = File.red 'sample.pages'
text = Yomu.read :text, data
metadata = Yomu.read :metadata, data
mimetype = Yomu.read :mimetype, data

yomu = Yomu.new 'sample.pages'
text = yomu.text

yomu = Yomu.new 'http://svn.apache.org/repos/asf/poi/trunk/test-data/document/sample.docx'
text = yomu.text

post '/:name/:filename' do
  yomu = Yomu.new params[:data][:tempfile]
  yomu.text
end

yomu = Yomu.new 'sample.docx'
yomu.mimetype.content_type
yomu.mimetype.extensions
```

```
```
