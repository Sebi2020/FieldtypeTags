# Description 
Provides a Tag field for [ProcessWire CMS](https://www.processwire.com) pages.


# Installation
Just clone or put this into a folder and install the module from the module admin page
of ProcessWire.

# Getting Tags in Templates
Just access this field like any other field of ProcessWire. This field returns an normal PHP Array.

## Example
```php
$tags = $page->Tags;
foreach($tags as $tag) {
	echo "Tag: " . $tag;
}
```

# Inputfields
As far as I know, there are currently no *single input* input fields that output arrays. Maybe you should consider to use the [InputfieldTagify][1] I created for this fieldtype.

[1]: https://github.com/sebi2020/InputfieldTagify