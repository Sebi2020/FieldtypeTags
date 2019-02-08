# Changelog
## [Unreleased]
### Added
- [19-02-08] `getAllTags()` method returning all tags and their count.
- [19-02-08] `getPagesByTag(string tagname)` method returning all pages, which have the tag `tagname`.
 ```php
 $tags = new FieldtypeTags();
  foreach($tags->getPagesByTag("mytag") as $page) {
  	echo "<li>{$page->title}</li>";
  } 
 ```

	
## [0.0.2] - 19-02-05
### Changed
- Text sanitizer to `sanitizeValue`


[Unreleased]: https://github.com/sebi2020/FieldtypeTags/compare/v0.0.2...HEAD
[0.0.2]: http://www.github.com/sebi2020/FieldtypeTags/compare/v0.0.1...v0.0.2