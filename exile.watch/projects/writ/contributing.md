---
description: '@exile-watch/writ setup & contribution guide'
---

# Contributing

## [Prerequisites](../../../development/prerequisites.md)

## Development

### 1. [Fork @exile-watch/writ repo](https://github.com/exile-watch/writ)

### 2. [Create GitHub PAT token](../../../development/generating-github-pat.md)

### 3. [Create .npmrc file](../../../development/.npmrc-file.md)&#x20;

### 4. Install dependencies

```bash
# project root
$: nvm use # uses node version that's defined in .nvmrc
$: npm i # install dependencies
```

### 5. Check changes made in [writ](./) package locally in [crucible](../crucible/) project

#### a) Create [writ](./) package link

<pre class="language-bash"><code class="lang-bash"><strong># @exile-watch/writ project
</strong># package path e.g. ~/writ/packages/writ-react
$: npm link
</code></pre>

#### b) Build [writ](./) package

<pre class="language-bash"><code class="lang-bash"><strong># @exile-watch/writ project
</strong># package path e.g. ~/writ/packages/writ-react
$: npm run build
</code></pre>

#### c) Link [writ](./) package in [crucible](../crucible/) project

<pre class="language-bash"><code class="lang-bash"><strong># @exile-watch/crucible project
</strong># root path ~/crucible
$: npm link @exile-watch/writ-react #
</code></pre>

### 6. Conclusion

Not happy with the change? \
Repeat step [#b-build-writ-package](contributing.md#b-build-writ-package "mention") and [#c-link-writ-package-in-crucible-project](contributing.md#c-link-writ-package-in-crucible-project "mention")

Happy with the change? \
Create a new pull request and don't forget to locally unlink modified package:

<pre class="language-bash"><code class="lang-bash"><strong># @exile-watch/writ project
</strong># package path e.g. ~/writ/packages/writ-react
$: npm unlink
</code></pre>

<pre class="language-bash"><code class="lang-bash"><strong># @exile-watch/crucible project
</strong># root path ~/crucible
$: npm i # this will "revert" linked module to the actual package 
</code></pre>