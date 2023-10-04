# demo-auto-release

Demo of GH Actions for automatic releases.

Free free make a commit and add a release tag!

## Git Commands to Create Release

This will create a Release with "v1.0.0" as the content/description of the release. The "v1.0.0" comes from the message in the annotated tag.

```
$ git add .
$ git commit -m "blah, blah"
$ git tag -a v1.0.0 -m "v1.0.0"
$ git push origin --follow-tags

# OR, if you have set the global push.followTags settings to true
$ git push origin
```


## Alternative That Shows Commits in the Release
```
$ git add .
$ git commit -m "blah, blah"
$ git push origin
$ git tag v1.0.0
$ git push origin v1.0.0
```

## Git Configuration
If you set `push.followTags` as shown below, you don't have to use the `--follow-tags` option in the command sequence above.

```
git config --global push.followTags true
```

## How The Release Github Action Works

This repo is configured with a Github Action workflow in [.github/workflows/release.marvinpinto.yml](.github/workflows/release.marvinpinto.yml) that implements the automatic release based on tags.

It relies on the [automatic-releases](https://github.com/marketplace/actions/automatic-releases) Github Action. That Action is one of many available to create Releases. Others may be better, but the one from Marvin Pinto is simple and does what's needed.

## Change Log

### v2.1.0
- minor version

### v2.0.0
- brand new major version

### v1.0.0
- initial commit
