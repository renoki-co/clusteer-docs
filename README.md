---
description: >-
  Clusteer is a Puppeteer wrapper written for PHP, with the super-power of
  parallelizing pages across multiple browser instances.
---

# ⚡ Introduction

![](.gitbook/assets/Clusteer\_25.png)

[![CI](https://github.com/renoki-co/clusteer/workflows/CI/badge.svg?branch=master)](https://github.com/renoki-co/clusteer/workflows/CI/badge.svg?branch=master) [![codecov](https://camo.githubusercontent.com/aa110e7130d5cfeaffe0a25ae3a3d0a7918a151bc8265683080dee93a907069f/68747470733a2f2f636f6465636f762e696f2f67682f72656e6f6b692d636f2f636c7573746565722f6272616e63682f6d61737465722f67726170682f62616467652e737667)](https://codecov.io/gh/renoki-co/clusteer/branch/master) [![StyleCI](https://camo.githubusercontent.com/a71f829458fce9d67959945a96ab050470ea50ee685c6147ead1ebe0219d6623/68747470733a2f2f6769746875622e7374796c6563692e696f2f7265706f732f3237363639313638312f736869656c643f6272616e63683d6d6173746572)](https://github.styleci.io/repos/276691681) [![Latest Stable Version](https://camo.githubusercontent.com/0ccfd6778704767f8d7bb424a355848914e5fd972f500792739a5696c81e4f72/68747470733a2f2f706f7365722e707567782e6f72672f72656e6f6b692d636f2f636c7573746565722f762f737461626c65)](https://packagist.org/packages/renoki-co/clusteer) [![Total Downloads](https://camo.githubusercontent.com/58a340aa460d83752b96861bfae512a05c60dccb8bc398b1cdfd2ea4d2c7fb25/68747470733a2f2f706f7365722e707567782e6f72672f72656e6f6b692d636f2f636c7573746565722f646f776e6c6f616473)](https://packagist.org/packages/renoki-co/clusteer) [![Monthly Downloads](https://camo.githubusercontent.com/69227b731d2838563019e0d0d03e67cd1af6c416c6bf9de3185e8ae7a3ba386b/68747470733a2f2f706f7365722e707567782e6f72672f72656e6f6b692d636f2f636c7573746565722f642f6d6f6e74686c79)](https://packagist.org/packages/renoki-co/clusteer) [![License](https://camo.githubusercontent.com/b67248fe288a35b0665c80029c317237d9b6028046d5cb6ac054d275998b509d/68747470733a2f2f706f7365722e707567782e6f72672f72656e6f6b692d636f2f636c7573746565722f6c6963656e7365)](https://packagist.org/packages/renoki-co/clusteer)

Clusteer is a Puppeteer wrapper written for PHP, with the super-power of parallelizing pages across multiple browser instances.

The package leverages [thomasdondorf/puppeteer-cluster](https://github.com/thomasdondorf/puppeteer-cluster), a Node.js module that allows you to build standby Puppeteer browsers that will open up pages, making the process of using a browser a blazing-fast experience. ⚡
