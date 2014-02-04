# mozilla-toolkit-versioning

A node library to parse simple [node-semver](https://github.com/isaacs/node-semver/)-ish strings to generate a min and max version of Mozilla platform support using Mozilla's [toolkit version format](https://developer.mozilla.org/en-US/docs/Toolkit_version_format). For comparing versions, check out [mozilla-version-comparator](https://github.com/linagora/mozilla-version-comparator).
## API

### mozVersion.parse(s)

```javascript
var mozVersion = require('mozilla-toolkit-versioning');
var parsed = mozVersion.parse('>=3.6 <= 30.0');
parsed.min; // '3.6'
parsed.max; // '30.0a'
```

## Ranges

* `1.2.3` - A specific version
* `&gt;1.2.3` - Greater than a specific version
* `&lt;1.2.3` - Less than a specific version (does not include pre-release)
* `&gt;=1.2.3` - Greater than or equal to a specific version (does not include pre-release)
* `&lt;=1.2.3` - Less than a specific version (DOES include pre-release)
* `&gt;=1.2.3 &lt;=2.3.4` - Between or equal to the range
* `1.2.3 - 2.3.4` := `&gt;=1.2.3 &lt;=2.3.4`

