# pa11y example repo

Goal of the repo is to demonstrate that pa11y-ci documentation and implementation have conflicting information.

pa11y-ci [Github page](https://github.com/pa11y/pa11y-ci) has following note: `Providing a sitemap will cause the urls property in your JSON config to be ignored.`

## Replication instructions

- Install dependencies `yarn`
- Execute `yarn test`

Terminal output might look different but the main point is the pa11.org URLs that. According to the docs, the output should only include the URLs that are in the google sitemap.

Either documentation is invalid or pa11y-ci has a bug

Example terminal output

```
$ pa11y-ci --sitemap https://www.google.com/finance/sitemap.xml
Running Pa11y on 40029 URLs:
 > https://pa11y.org/ - 0 errors
 > https://pa11y.org/contributing/ - 0 errors
 > https://consent.google.com/ml?continue=https://www.google.com/finance/&gl=FI&hl=en-US&cm=2&pc=fgc&src=1 - 2 errors
 > https://consent.google.com/ml?continue=https://www.google.com/finance/quote/.DJI:INDEXDJX&gl=FI&hl=en-US&cm=2&pc=fgc&src=1 - 2 errors
 > https://consent.google.com/ml?continue=https://www.google.com/finance/quote/.INX:INDEXSP&gl=FI&hl=en-US&cm=2&pc=fgc&src=1 - 2 errors
 ...
```
