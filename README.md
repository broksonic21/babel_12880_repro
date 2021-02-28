# babel_12880_repro

See https://github.com/babel/babel/issues/12880#issuecomment-787216822 for description and the issue. 

* `main` branch shows the 7.12.7 case with implied @babel/core 7.12.*
* `upgrade_broken` branch shows the 7.13.8 preset-env case with implied @babel/core 7.12.* (and breaks on reading package.json's browserlist)
