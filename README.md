A database of Rust compiler versions and the git commit that they were built
from.

```
Usage:
	./commit-db.rb update [--force]
	./commit-db.rb list-valid CHANNEL
	./commit-db.rb lookup COMMIT
```

Recently, the AWS S3 client began throwing errors if no credentials were provided. To work around this issue, we can simply give it any credentials like so:

```bash 
AWS_ACCESS_KEY_ID="test" AWS_SECRET_ACCESS_KEY="test" ./commit-db.rb update --force
```

This is all scraped from [buildbot](https://buildbot.rust-lang.org/) with some
missing information added in [fixups](fixups). Note that nightly information is
not available before March 2016. PRs accepted :-p.
