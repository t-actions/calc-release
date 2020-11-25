# Calculate Release Information Actions

Calculate `TAG`, `REF` and etc information using for release.

> tag -> tag information
> default branch -> `latest` tag
> other branch -> `release-<branch>` tag

## Usage

```yaml
- uses: t-actions/calc-release@master
  id: param
  with:
    # Tag name for release instead of github.ref if not empty
    tag: ''

    # The tag of default branch will be latest
    # Default: master
    default_branch: ''
```

### Output

* **tag**: tag for release
* **ref**: ref for checkout to corresponding tag
* **is_branch**: 1 if release for branch, 0 if release for tag
