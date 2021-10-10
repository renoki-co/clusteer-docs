# 🚀 Installation

### Install the package

You can install the package via composer:

```bash
composer require renoki-co/clusteer
```

To customize the configuration, you may deploy the config file:

```bash
php artisan vendor:publish --provider="RenokiCo\Clusteer\ClusteerServiceProvider"
```

### Installing Node.js prerequisites

The leveraged package is written in Node.js, so Node.js 10.x+ is needed on the machine. In the project root (expecting you may be using Laravel, but it works for vanilla PHP projects too), install the following prereqs:

```bash
npm install --save \
    dotenv@^8.2.0 \
    express@^4.17.1 \
    express-healthcheck@^0.1.0 \
    puppeteer@^5.5.0 \
    puppeteer-cluster@^0.22.0 \
    random-user-agent@^1.0.0
```

### Installing Chromium

The server relies on Chromium, so you can find a simple way of getting your Chrome binary file, like [staudenmeir/dusk-updater](https://github.com/staudenmeir/dusk-updater).

Below you will find some examples to install the chromium binary:

{% tabs %}
{% tab title="Ubuntu" %}
```bash
apt-get update && apt-get install -y libnss3 chromium-browser

# check the binary
/usr/bin/chromium-browser --version
```
{% endtab %}

{% tab title="CentOS" %}
```bash
# the script is available on gist
curl https://gist.githubusercontent.com/rennokki/813867e8d5572d0ea51b1551dc27cd2a/raw/e368c5a6a12e22739247a97d9bf21ca399224da9/install_latest_chrome_binary.sh | bash

# check the binary
/usr/bin/google-chrome-stable --version
```
{% endtab %}
{% endtabs %}

Once ready, you can set up in your env the `CLUSTEER_CHROMIUM_PATH` variable to define the binary that will be used for the headless browser.
