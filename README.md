# babel_12880_repro

See https://github.com/babel/babel/issues/12880#issuecomment-787216822 for description and the issue.

* `main` branch shows the 7.12.7 case with implied @babel/core 7.12.*
* `upgrade_broken` branch shows the 7.13.8 preset-env case with implied @babel/core 7.12.* (and breaks on reading package.json's browserlist)
* `fixed_added_babel_core` branch shows a devDependency @babel/core that fixes it
* `fixed_regenerate_package_lock` branch shows implied @babel/core but regenerate package lock (also fixes it)

For all, run `npm i; npm run build` and look at the targets found. It should say

```
Using targets:
{
  "chrome": "84"
}
```

not

```
> babel src

@babel/preset-env: `DEBUG` option

Using targets:
{}
```
