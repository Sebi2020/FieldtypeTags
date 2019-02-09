# Description 
Provides a Tag field for [ProcessWire CMS](https://www.processwire.com) pages.


# Installation
Just clone or put this into a folder and install the module from the module admin page
of ProcessWire.

# Getting Tags in Templates
Just access this field like any other field of ProcessWire. This field returns an normal PHP Array.
# Examples
## Retrieve tags related to the current page
```php
// Fetch the tag field. Here it's called "Tags'.
$tags = $page->Tags;
foreach($tags as $tag) {
	echo "Tag: " . $tag;
}
```
## Retrieve alphabetically sorted tags, frequency and related pages
```php
// Retrieve the module
$tags = $this('modules')->get("FieldtypeTags");

// Fetch all tags and their frequency.
foreach($tags->getAllTags() as $field => $count) {
	echo "<h2>Tag \"{$field}\" (used {$count} times)</h2>";
	echo "<ul>";

	// Fetch all pages for a given tag
	foreach($tags->getPagesBytag($field) as $page) {
		echo "<li><a href=\"{$page->url}\">{$page->title}</a></li>";
	}
	echo "</ul>";
}
```

# Inputfields
As far as I know, there are currently no *single input* input fields that output arrays. Maybe you should consider to use the [InputfieldTagify][1] I created for this fieldtype.

[1]: https://github.com/sebi2020/InputfieldTagify